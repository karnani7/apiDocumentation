
  <img src="https://thekarnani.com/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Flogo.fb2f23c3.png&w=256&q=75" alt="The Karnani" style="width: 100px; margin-right: 10px;" />
  <span style="font-size: 24px; font-weight: bold; color: #1ac5c2;">The Karnani API Documentation</span>






## Overview

This API provides detailed information about a specific room within a property, including type, category, rental details, images, and more. It is designed for use in applications requiring comprehensive data on rental properties.

## Endpoint

`GET https://thekarnani.com//api/properties`

Retrieves detailed information about rooms in a property.


### Response Format

A successful request to this endpoint returns an object containing detailed information about the room, including identifiers, room characteristics, rental terms, images, and availability dates.

#### Response Object

- `_id`: Object containing the unique identifier of the room.
  - `$oid`: String representing the ObjectId of the room in MongoDB.
- `roomNumber`: String specifying the room number within the property.
- `roomType`: String indicating the type of room (e.g., "Double").
- `roomCategory`: String describing the room's category (e.g., "Non Ensuite").
- `floor`: String specifying the floor on which the room is located.
- `propertyAddress`: String containing the full address of the property.
- `virtualTourLink`: String URL to a virtual tour of the room. (youtube)
- `bathroomCount`: Number indicating how many bathrooms are available.
- `monthlyRent`: Number representing the monthly rent price in the local currency.
- `tenantPreference`: String indicating the preferred type of tenant (e.g., "Individual Only").
- `councilTaxCode`: String specifying the council tax band.
- `councilTaxYearlyAmount`: Number indicating the yearly amount of council tax.
- `epcRating`: String representing the Energy Performance Certificate rating.
- `occupancyStatus`: String indicating the occupancy status (e.g., "OCCUPIED").
- `thumbnailImage`: String URL to the thumbnail image of the room.
- `commonAreaImages`: Array of strings containing URLs to images of common areas.
- `roomImages`: Array of strings containing URLs to images of the room.
- `totalPropertyBeds`: Number indicating the total number of beds in the property.
- `availableFrom`: Object containing the date from which the room is available.
  - `$date`: String representing the availability start date in ISO format.
- `availableUntil`: Object containing the date until which the room is available.
  - `$date`: String representing the availability end date in ISO format.

### Example Response

```json
[{
  "_id": {
    "$oid": "65c724f85e565a14566af10b"
  },
  "roomNumber": "1",
  "roomType": "Double",
  "roomCategory": "Non Ensuite",
  "floor": "Ground Floor",
  "propertyAddress": "12 Bulan Road, OX3 7HT",
  "virtualTourLink": "https://youtu.be/BsexxGfhtyo",
  "bathroomCount": 2,
  "monthlyRent": 795,
  "tenantPreference": "Individual Only",
  "councilTaxCode": "E",
  "councilTaxYearlyAmount": 2849.57,
  "epcRating": "B",
  "occupancyStatus": "OCCUPIED",
  "thumbnailImage": "",
  "commonAreaImages": [
    "https://househat.s3.ap-south-1.amazonaws.com/properties/12 Bulan Road, OX3 7HT/common/2.jpg",
    "https://househat.s3.ap-south-1.amazonaws.com/properties/12 Bulan Road, OX3 7HT/common/1.jpg",
    "https://househat.s3.ap-south-1.amazonaws.com/properties/12 Bulan Road, OX3 7HT/common/3.jpg",
    "https://househat.s3.ap-south-1.amazonaws.com/properties/12 Bulan Road, OX3 7HT/common/4.jpg"
  ],
  "roomImages": [
    "https://househat.s3.ap-south-1.amazonaws.com/properties/12 Bulan Road, OX3 7HT/Room1/1000022412.jpg",
    "https://househat.s3.ap-south-1.amazonaws.com/properties/12 Bulan Road, OX3 7HT/Room1/1000022415.jpg"
  ],
  "totalPropertyBeds": 5,
  "availableFrom": {
    "$date": "2024-07-16T05:30:00.000Z"
  },
  "availableUntil": {
    "$date": "2025-01-14T05:30:00.000Z"
  }
}
]
