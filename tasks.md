cta-backend-api — Task List
Repository & Project Setup

[x] Create new Git repository
[x] Initialize Node.js project (npm init)
[ ] Add .gitignore (node, dist, env)
[x] Add README.md
[ ] Choose license and add LICENSE file

Tooling & Dependencies

[x] Install Fastify
[x] Install TypeScript
[x] Install ts-node / tsx for local dev
[x] Install @types/node
[x] Add build scripts (dev, build, start)
[x] Add tsconfig.json
[x] Configure ESLint (optional)
[x] Configure Prettier (optional)

Fastify Server Bootstrap

[x] Create src/ directory
[x] Create Fastify server entry point
[x] Add basic server start logic
[x] Add ping check endpoint (GET /ping Return pong)
[x] Verify server starts and responds

Configuration & Environment

[ ] Add environment variable support
[ ] Define default limits (train, bus)
[ ] Validate required config on startup

Data Ingestion — Train Stations

[ ] Download CTA L station dataset
[ ] Write ingestion script for train stations
[ ] Normalize station fields (id, lat, lon, name, lines)
[ ] Store station data in memory on startup
[ ] Verify station count and data integrity

Data Ingestion — Bus Stops

[ ] Download CTA bus stop dataset
[ ] Write ingestion script for bus stops
[ ] Normalize stop fields (id, lat, lon, routes)
[ ] Compute geohash for each bus stop
[ ] Bucket bus stops by geohash
[ ] Store bus stop data in memory on startup

Shared Geo Utilities

[ ] Implement Haversine distance function
[ ] Add geohash encoding utility
[ ] Add geohash neighbor lookup utility

Spatial Query Logic

[ ] Implement nearby train station lookup (linear scan)
[ ] Implement configurable limit for train stations
[ ] Implement nearby bus stop lookup (geohash + distance)
[ ] Implement configurable limit for bus stops
[ ] Add distance sorting and trimming

Core API Endpoints (v1)

[ ] Add API versioning (/v1)
[ ] Implement GET /v1/stops/:id
[ ] Implement GET /v1/trains/nearby
[ ] Implement GET /v1/buses/nearby
[ ] Validate lat/lon query parameters
[ ] Validate limit parameter

Caching Layer

[ ] Add in-memory cache for nearby train lookups
[ ] Add in-memory cache for nearby bus lookups
[ ] Add TTL configuration for caches

Error Handling & Validation

[ ] Add centralized error handler
[ ] Handle invalid coordinates gracefully
[ ] Handle unknown stop IDs
[ ] Return watch-friendly error responses

Performance & Hardening

[ ] Add basic rate limiting
[ ] Ensure all datasets load only once
[ ] Verify memory usage stays bounded
[ ] Measure average response times

Testing

[ ] Add unit tests for geo utilities
[ ] Add tests for spatial queries
[ ] Add endpoint integration tests
[ ] Test edge cases (no stops nearby, invalid input)

Documentation

[ ] Finalize README
[ ] Document endpoint contracts
[ ] Document data refresh process
[ ] Document local development workflow

Future Enhancements

[ ] Integrate CTA Train Tracker arrivals
[ ] Integrate CTA Bus Tracker arrivals
[ ] Add arrival-time caching
[ ] Add direction-aware filtering
[ ] Add favorites support
[ ] Add API authentication
[ ] Add metrics and logging
