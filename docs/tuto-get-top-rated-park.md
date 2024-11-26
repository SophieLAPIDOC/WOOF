# [WOOF! API Tutorials](overview.md#tutorials)
# Find the best parks (user-rated) in your city
When nothing but the best will do, you can trust the community of WOOF! users to tell it like it is. 
## Prerequisites 
 1. Start the json-server, as explained in [set up your environment](initial-setup.md)
 2. Open the [Postman desktop app](https://www.postman.com/downloads/).
## Sample request
Send the following request to retrieve a list of parks in Madison CT with tghe maximum rating of 5 stars. This request combines two query parameters: `town`: `Madison` and `rating`: `5`.
```
GET http://localhost:3000/park?town=Madison&rating=5
```

## Response
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