
## Get a specific song

```shell
curl http://api.unicornfm.com/songs/25
```

```javascript
this.get('store').findRecord('song', 25);
```

> The above command returns JSON structured like this:

```json
[
  jsonapi: {
    version: "1.0"
  },
  data: {
      type: "song",
      id: 25,
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
```

### HTTP Request

`GET http://api.unicornfm.com/v1/songs/:id`

### Segment Parameters

Parameter | Description
--------- | -----------
id | The id of the song to retireve
