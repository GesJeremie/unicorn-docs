
## Create a User

```shell
curl --request POST http://api.unicornfm.com/v1/users
```

```javascript
this.get('store').createRecord('user').save()
```

> The above command returns JSON structured like this:

```json
[
  jsonapi: {
    version: "1.0"
  },
  data: [
    {
      type: "user",
      id: "f066d4ef-c332-4d2b-a793-65aa88768e55",
      attributes: {
        token: "5976423a-ee35-11e3-8569-14109ff1a304",
        inserted_at: "2017-05-27 20:21:38.987925",
        updated_at: "2017-05-27 20:21:38.987925"
      }
    }
  ]  
]
```


### HTTP Request

<aside class="http">
  POST http://api.unicornfm.com/v1/users
</aside>
