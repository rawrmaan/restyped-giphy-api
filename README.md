<p align="center">
  <img src="/example.gif" />
</p>

## RESTyped typings for the Giphy API

Quickly and easily use the wonderful Giphy API in TypeScript with end-to-end typing!

## How to use it

`npm install restyped-giphy-api`

Then use a REST client that supports <a href="https://github.com/rawrmaan/restyped">RESTyped</a>, like <a href="https://github.com/rawrmaan/restyped-axios">`restyped-axios`</a>.

## Example

```typescript
import axios from 'restyped-axios'
import { GiphyAPI } from 'restyped-giphy-api'

const client = axios.create<GiphyAPI>({baseURL: 'http://api.giphy.com/v1'})

client.request({
  url: '/gifs/search',
  params: {
    api_key: 'abc123',
    q: 'zero effort'
  }
}).then((res) => {
  return res.data.data[0].images.fixed_height.url
})
```
