# Songs

We don't store any physical songs on our servers, in fact we retrieve our songs from Youtube. Think of **songs** like a wrapper of the youtube API.

<aside class="notice">
  We are thinking to use multiple providers in the future such as VIMEO and Soundcloud.
</aside>

API with digest results.

## The Song Object

### Attributes

Attributes | Description
--------- | -----------
title <span class="type">```String```</span> | Title of the song
thumbnail <span class="type">```String```</span> | Thumbnail url
duration <span class="type">```String```</span> | The total duration of the song in seconds
provider <span class="type">```String```</span> | The service provider, currently only ```youtube```
inserted-date <span class="type">```Timestamp```</span> | Timestamp when the server was created
updated-date <span class="type">```Timestamp```</span> | Timestamp when the server was updated


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
        duration: "246",
        provider: "youtube",
        inserted-at: "2017-05-27 20:21:38.987925",
        updated-at: "2017-05-27 20:21:38.987925"
      }
    }
  ]  
]
```

### HTTP Request

`GET http://api.unicornfm.com/v1/songs`

### Data Parameters

Parameter | Description
--------- | -----------
query | Keyword(s) to find related songs
youtube_api_key <span class="type">```optional```</span> | If we don't have in cache the results for the search given we hit the youtube API with our API key. If you are **not a dick** you will provide [your api key](https://developers.google.com/youtube/registering_an_application).
