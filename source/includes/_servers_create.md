
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
      id: "740d712c-de24-4131-8ae4-b674a320e228",
      attributes: {
        name: "idiot-parrot-678",
        user-id: "af3c79c7-8300-4c9f-8e02-ed0257a2ab12",
        current-track: null,
        inserted-at: "2017-05-27 20:21:38.987925",
        updated-at: "2017-05-27 20:41:38.987925"
      }
    }
  ]  
]
```

### HTTP Request

<aside class="http">
  POST http://api.unicornfm.com/v1/servers
</aside>

### Data Parameters

Parameter | Description
--------- | -----------
user-token <span class="type required">```Required```</span> | The token of the user
name <span class="type">```Optional```</span>| The name to give to the server. If not provided, we auto generate one. Be aware we suglify the input which allow only <strong>alpha-numeric characters</strong> and <strong>dashes</strong>. Keep in mind we only accept <strong>unique names</strong>.

