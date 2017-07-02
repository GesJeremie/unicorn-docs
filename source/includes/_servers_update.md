## Update a Server

```javascript
this.get('store').findRecord('server', '13cdd8b1-f3d4-449c-ab61-ff78fed187cb').then(function(server) {
  // Required
  server.set('user-token', 'ad0700ce-b579-40eb-8201-c502611dc9e0');

  // Optional
  server.set('name', 'beautiful-unicorn');
  server.set('user-id', 'bfe48bff-f6ed-4091-a876-a36b7d9a146a');
  server.set('current-track', 'da306b85-2247-44c3-aba0-bd4871482672');
  server.save(); 
});
```

### HTTP Request

<aside class="http">
  PATCH http://api.unicornfm.com/v1/servers/:id
</aside>

### Data Parameters

Parameter | Description
--------- | -----------
user-token <span class="type required">```Required```</span>| The token of the owner (current user id). If the token provided doesn't match the token of the server's user-id, the API will reject your call.
name <span class="type">```Optional```</span> | The name of the server. Be aware we suglify the input which allow only **alpha-numeric characters** and **dashes**. If the name provided is **not unique**, the API will **reject** the call.
user-id <span class="type">```Optional```</span> | The owner of the server. If the user-id doesn't exist, the API will **reject** the call.
current-track <span class="type">```Optional```</span> | Current track playing on the server. If the track doesn't exist, the API will **reject** the call.
