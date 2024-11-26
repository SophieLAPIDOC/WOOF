# [WOOF! API Tutorials](overview.md#tutorials)
# Find who goes to your favourite park
WOOF! connects people, dogs and parks. Before making a park your favourite hang out, check who is also a regular there. 
## Prerequisites 
 1. Start the json-server, as explained in [set up your environment](initial-setup.md)
 2. Open the [Postman desktop app](https://www.postman.com/downloads/).

 ## Sample request
 First let's find a list of parks in Madison CT.

Send the following request with the parameter `town`: `Madison`.
```
http://localhost:3000/park?town=Madison
```

## Response
The request returns a single park with `id`: `3`.
```json
{
    "park_name": "Madison Dog Park",
    "town": "Madison",
    "coordinates": "41.272346, -72.549974",
    "hours": "until sunset",
     "amenities": "poop bags, hand sanitizer, water bowls",
    "comments": "Near the beach",
    "rating": "5",
    "id": 3
    }
```
 ## Sample request
 Let's find who is a regular attendee at park with `id`: `3` and check if they would make suitable playmates.
```
GET http://localhost:3000/dog?park_id=3
```

## Response
The request returns the details of two dogs: Bella and Mr. Henry Sullivan.
```json
[
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
    },
    {
        "name": "Mr. Henry Sullivan",
        "photo": "../Photos/HenrySullivan.jpeg",
        "breed": "Treeing Walker Coonhound",
        "size": "Large",
        "human": "Wendy & Chris",
        "zip_code": "06417",
        "something_about_yourself": "I love to play chase!",
        "at_the_park_?": "Y",
        "park_id": 3,
        "id": 2
    }
]
```