
# Users 

If you played with [unicornfm.com](http://www.unicornfm.com) you should know you are able to create, join a server, push songs without registration. This is possible thanks to our concept of **anonymous users**. In fact when you browse our app you are automatically "connected" as an anonymous user.
Thus we are able to know who is the owner of a server, who pushed a song, etc.

<aside class="notice">
  Most of the endpoints of the API will ask for an user token.
</aside>

## The User Object

### Attributes

Attribute | Description
--------- | -----------
token <span class="type">```String```</span> | Auto generated token which will be often asked as a required parameter by other endpoints
role <span class="type">```String```</span> | The role of the user, currently the only available role is:<br/> ```anonymous```
inserted_date <span class="type">```Timestamp```</span> | Time at which the user was created
updated_date <span class="type">```Timestamp```</span> | Time at which the user was updated

<aside class="warning">
  The token is returned only at the creation of the user.
</aside>

## Create an User

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
      id: "193",
      attributes: {
        token: "5976423a-ee35-11e3-8569-14109ff1a304",
        role: "anonymous",
        inserted_at: "2017-05-27 20:21:38.987925",
        updated_at: "2017-05-27 20:21:38.987925"
      }
    }
  ]  
]
```


### HTTP Request

`POST http://api.unicornfm.com/v1/users`
