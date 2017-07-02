
## Retrieve a Server

```shell
curl "http://api.unicornfm.com/v1/server/idiot-parrot-678"
```

```javascript
this.get('store').findRecord('server', 'idiot-parrot-678');
```

> The above command returns JSON structured like this:

```json
[
  jsonapi: {
    version: "1.0"
  },
  data: [
    {
      type: "server",
      id: "idiot-parrot-678",
      attributes: {
        name: "idiot-parrot-678",
        user-id: 20,
        current-track: 130,
        inserted-at: "2017-05-27 20:21:38.987925",
        updated-at: "2017-05-27 20:21:38.987925"
      }
    }
  ]  
]
```

This endpoint retrieves the data of a specific server.

### HTTP Request

<aside class="http">
  GET http://api.unicornfm.com/v1/server/:id
</aside>

### Segment Parameters

Parameter | Description
--------- | -----------
id | The server id you want to retrieve.
