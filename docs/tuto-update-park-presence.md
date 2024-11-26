# [WOOF! API Tutorials](overview.md#tutorials)
# Update your dog's presence at the park
The WOOF! API allows to update your dog's presence at the park in real time, so that your dog's friends can come and join you (or avoid you).
## Prerequisites 
 1. Start the json-server, as explained in [set up your environment](initial-setup.md)
 2. Open the [Postman desktop app](https://www.postman.com/downloads/).
    
## Sample request
```
PATCH http://localhost:3000/dog/4
```

## Body
In the body of the request, send the parameter `at_the_park_?` as `Y` if you are at the park (or on you way), `N` if you are about to leave.  
```json
{
       "at_the_park_?": "Y",
}
```

## Response
The WOOF! API returns a the entire dog's record with the updated `at_the_park_?` parameter. 
```json
{
    "name": "Loki",
    "photo": "../Photos/Loki.jpeg",
    "breed": "Siberian Husky",
    "size": "Large",
    "human": "Sylvana",
    "zip_code": "06040",
    "something_about_yourself": "As long as no balls are involved, I'm very mellow!",
    "at_the_park_?": "Y",
    "park_id": 1,
    "id": 4
}
```