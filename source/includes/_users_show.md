
## Retrieve a User

```shell
curl http://api.unicornfm.com/users/v1/f066d4ef-c332-4d2b-a793-65aa88768e55
```

```javascript
this.get('store').findRecord('user', 'f066d4ef-c332-4d2b-a793-65aa88768e55');
```

> The above command returns JSON structured like this:

```json
[
  jsonapi: {
    version: "1.0"
  },
  data: {
      type: "user",
      id: "f066d4ef-c332-4d2b-a793-65aa88768e55",
      attributes: {
        inserted_at: "2017-05-27 20:21:38.987925",
        updated_at: "2017-05-27 20:21:38.987925"
      }
    }
]
```

### HTTP Request

<aside class="http">
  GET http://api.unicornfm.com/v1/users/:id
</aside>

### Segment Parameters

Parameter | Description
--------- | -----------
id | The id of the user to retrieve
