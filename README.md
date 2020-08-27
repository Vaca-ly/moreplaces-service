## Server API

### Get Property info
  * GET `/property/{propertyId}`

**Path Parameters:**
  * `{propertyId}` property id

**Success Status Code:** `200`

**Returns:** JSON

```json
    {
      "propertyId": "Number",
      "imageUrl": "String",
      "isSuperhost": "Boolean",
      "propertyType": "String",
      "numOfRooms": "String",
      "rating": "Number",
      "numOfRatings": "Number",
      "description": "String",
      "price": "Number"
    }
```

### Add a property
  * POST `/property/{propertyId}`

**Success Status Code:** `201`

**Request Body**: Expects JSON with the following keys.

```json
    {
      "propertyId": "Number",
      "imageUrl": "String",
      "isSuperhost": "Boolean",
      "propertyType": "String",
      "numOfRooms": "String",
      "rating": "Number",
      "numOfRatings": "Number",
      "description": "String"
    }
```

### Update Property
  * PATCH `/property/{property_id}`

**Path Parameters:**
  * `{property_id}` property id

**Success Status Code:** `204`

**Request Body**: Expects JSON with any of the following keys (include only keys to be updated)

```json
    {
      "imageUrl": "String",
      "isSuperhost": "Boolean",
      "propertyType": "String",
      "numOfRooms": "String",
      "rating": "Number",
      "numOfRatings": "Number",
      "description": "String"
    }
```

### Delete property
  * DELETE `/property/{property_id}`

**Path Parameters:**
  * `{property_id}` list id

**Success Status Code:** `204`