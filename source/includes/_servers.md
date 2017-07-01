
# Servers

## The Server Object

### Attributes

Attributes | Description
--------- | -----------
name <span class="type">```String```</span> | The name of the server
user-id <span class="type">```Integer```</span> | The owner of the server
push-type <span class="type">```String```</span>| When a track is pushed to the server should it played instantly ```[instant]``` or added to the current playlist ```[playlist]```
online <span class="type">```Boolean```</span> | Flag to know if the server is currently listening events (socket opened)
inserted-date <span class="type">```Timestamp```</span> | Timestamp when the server was created
updated-date <span class="type">```Timestamp```</span> | Timestamp when the server was updated



## Create a Server


```shell
curl http://api.unicornfm.com/v1/servers \
  -d '{"server":{"user_token":"5976423a-ee35-11e3-8569-14109ff1a304"}}' 
```

```javascript
this.get('store').create('server', {
  userToken: '5976423a-ee35-11e3-8569-14109ff1a304'
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
      type: "server",
      id: "idiot-parrot-678",
      attributes: {
        name: "idiot-parrot-678",
        user-id: 20,
        push-type: "instant",
        online: false,
        inserted-at: "2017-05-27 20:21:38.987925",
        updated-at: "2017-05-27 20:21:38.987925"
      }
    }
  ]  
]
```

### HTTP Request

`POST http://api.unicornfm.com/v1/servers`

### Data Parameters

Parameter | Description
--------- | -----------
user_token | The token of the user


## Get a Specific Server

```shell
curl "http://api.unicornfm.com/v1/server/idiot-parrot-678"
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
        push-type: "instant",
        online: false,
        inserted-at: "2017-05-27 20:21:38.987925",
        updated-at: "2017-05-27 20:21:38.987925"
      }
    }
  ]  
]
```

This endpoint retrieves the data of a specific server.

### HTTP Request

`GET http://api.unicornfm.com/v1/server/:id`

### Segment Parameters

Parameter | Description
--------- | -----------
id | The server id you want to retrieve.

### Return Attributes

Attributes | Description
--------- | -----------
name | The name of the server
push_type | When a track is pushed to the server, should it played instantly ```[instant]``` or added to the current playlist ```[playlist]```
inserted_date | Timestamp when the server was created
updated_date | Timestamp when the server was updated
