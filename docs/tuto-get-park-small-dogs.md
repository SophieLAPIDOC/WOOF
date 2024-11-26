# [WOOF! API Tutorials](overview.md#tutorials)
# Find other small dogs in your favourite park
Whether your dog is large and boisterous, or small and timid, you might find it more comfortable to go to a park frequented by dog the same size as yours.
## Prerequisites 
 1. Start the json-server, as explained in [set up your environment](initial-setup.md)
 2. Open the [Postman desktop app](https://www.postman.com/downloads/).
## Sample request
To find out if other small dogs attend Madision Dog Park (Park ID 3) send the following request:
```
GET http://localhost:3000/dog?park_id=3&size=Small
```
To find out if any small dog is currently at Madison Dog Park CT, add an additional query parameter: `at_the_park_?` and filter on `Y`.
```
GET http://localhost:3000/dog?park_id=3&size=Small&at_the_park_?=Y
```

## Response
Little Bella is a regular attendee at Madison Dog Park and she is there right now. Time to grab the leash and head out.
```json
{
    "name": "Bella",
    "photo": "../Photos/Bella.jpeg",
    "breed": "mini pittie mix",
    "size": "Small",
    "human": "Wendy & Chris",
    "zip_code": "06417",
    "something_about_yourself": "I like dogs with good manners.",
    "at_the_park_?": "Y",
    "park_id": 3,
    "id": 1
    }
```