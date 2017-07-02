## Search songs


```shell
curl http://api.unicornfm.com/songs?query=haezer+minted
```

```javascript
this.get('store').query('songs', {
  query: 'Haezer - Minted'
});
```

> The above command returns JSON structured like this:

```json
[
  jsonapi: {
    version: "1.0"
  },
  data: [
    {
      type: "song",
      id: "3839",
      attributes: {
        title: "HAEZER - Minted (Official Video) ",
        thumbnail: "https://i.ytimg.com/vi/e-NJjN2UWVs/hqdefault.jpg",
        duration: 246,
        code: "JdBZJVmQz-c",
        provider: "youtube",
        inserted-at: "2017-05-27 20:21:38.987925",
        updated-at: "2017-05-27 20:21:38.987925"
      }
    }
  ]  
]
```

### HTTP Request

<aside class="http">
  GET http://api.unicornfm.com/v1/songs
</aside>

### Data Parameters

Parameter | Description
--------- | -----------
query | Keyword(s) to find related songs
youtube_api_key <span class="type">```optional```</span> | If we don't have in cache the results for the search given we hit the youtube API with our API key. If you are **not a dick** you will provide [your api key](https://developers.google.com/youtube/registering_an_application).
