
## The User Object

```json
{
  type: "user",
  id: "f066d4ef-c332-4d2b-a793-65aa88768e55",
  attributes: {
    token: "5976423a-ee35-11e3-8569-14109ff1a304",
    inserted-at: "2017-05-27 20:21:38.987925",
    updated-at: "2017-05-27 20:21:38.987925"
  }
}
```


### Attributes

Attribute | Description
--------- | -----------
token <span class="type">```String```</span> | Auto generated token which will be often asked as a required parameter by other endpoints
inserted-date <span class="type">```Timestamp```</span> | Time at which the user was created
updated-date <span class="type">```Timestamp```</span> | Time at which the user was updated

<aside class="warning">
  The token is returned only at the creation of the user.
</aside>