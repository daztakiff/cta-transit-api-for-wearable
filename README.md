# CTA Backend Api
A lightweight backend API for serving CTA train station and bus stop proximity data, optimized for Garmin Connect IQ and other low-bandwidth clients.
Goals:
- Stores CTA stop metadata locally
- Computes nearby stops efficiently
- Returns only stop IDs for minimal payloads

#Tech Stack

Node.js
Fastify
TypeScript
In-memory data storage (for now)

# getStopbyId
GET /v1/stops/:id

{
  "id": "40380",
  "name": "Clark/Lake",
  "lat": 41.8857,
  "lon": -87.6301,
  "type": "train"
}

# getNearbyTrainStations
GET /v1/trains/nearby?lat=41.88&lon=-87.63&limit=3

{
  "stations": ["40380", "40260", "41490"]
}


# getNearbyBusStops
GET /v1/buses/nearby?lat=41.88&lon=-87.63&limit=5

{
  "stops": ["1234", "5678", "9012"]
}

