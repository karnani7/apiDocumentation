
  <img src="https://thekarnani.com/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Flogo.fb2f23c3.png&w=256&q=75" alt="The Karnani" style="width: 100px; margin-right: 10px;" />
  <span style="font-size: 24px; font-weight: bold; color: #1ac5c2;">The Karnani API Documentation</span>






# The Karnani API Documentation

## Overview

This API provides detailed information about rooms within a property, including type, category, rental details, images, and availability. It is designed for use in applications requiring comprehensive data on rental properties.

## Endpoint

`GET https://thekarnani.com/api/properties`

Retrieves detailed information about rooms in a property.

## Response Format

A successful request to this endpoint returns an object containing an array of rooms within the property, along with additional property details.

### Response Object

- `rooms`: An array containing objects representing individual rooms within the property.
  - `_id`: String containing the unique identifier of the room.
  - `roomNumber`: String specifying the room number within the property.
  - `roomType`: String indicating the type of room (e.g., "Double").
  - `roomCategory`: String describing the room's category (e.g., "Non Ensuite").
  - `floor`: String specifying the floor on which the room is located.
  - `propertyAddress`: String containing the full address of the property.
  - `virtualTourLink`: String URL to a virtual tour of the room (YouTube).
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
  - `availableFrom`: Date and time representing the availability start date.
  - `availableUntil`: Date and time representing the availability end date.

- `propertyAddress`: String containing the full address of the property.
- `lowestMonthlyRateOfARoom`: Number representing the lowest monthly rent price among all rooms in the property.
- `thumbnailImage`: String URL to the thumbnail image of the property.

## Example Response

```json
[{
  "rooms": [
    {
      "_id": "65c630586b4f92c2c6e624c0",
      "roomNumber": "3",
      "roomType": "Single",
      "roomCategory": "Non Ensuite",
      "floor": "First Floor",
      "propertyAddress": "10 Harcourt Terrace, OX3 7QF",
      "virtualTourLink": "https://youtu.be/RtsoTDXscfU",
      "bathroomCount": 2,
      "monthlyRent": 800,
      "tenantPreference": "Individual Only",
      "councilTaxCode": "C",
      "councilTaxYearlyAmount": 2098.02,
      "epcRating": "",
      "occupancyStatus": "OCCUPIED",
      "thumbnailImage": "",
      "commonAreaImages": [
        "https://househat.s3.ap-south-1.amazonaws.com/properties/10 Harcourt Terrace, OX3 7QF/common/1.png",
        "https://househat.s3.ap-south-1.amazonaws.com/properties/10 Harcourt Terrace, OX3 7QF/common/2.png",
        "https://househat.s3.ap-south-1.amazonaws.com/properties/10 Harcourt Terrace, OX3 7QF/common/4.png"
      ],
      "roomImages": [
        "https://househat.s3.ap-south-1.amazonaws.com/properties/10 Harcourt Terrace, OX3 7QF/Room3/8.png"
      ],
      "totalPropertyBeds": 6,
      "availableFrom": "2024-06-03T05:30:00.000Z",
      "availableUntil": "2025-08-20T05:30:00.000Z"
    }
    
  ],
  "propertyAddress": "10 Harcourt Terrace, OX3 7QF",
  "lowestMonthlyRateOfARoom": 795,
  "thumbnailImage": "https://househat.s3.ap-south-1.amazonaws.com/properties/10 Harcourt Terrace, OX3 7QF/common/1.png"
}]
