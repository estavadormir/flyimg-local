# Flyimg Docker Compose Setup
This repository provides a Docker Compose configuration for deploying [Flyimg](https://github.com/flyimg/flyimg) with Docker.

# Configuration
FLYIMG_SOURCE_TYPE: Set to local to use local storage.
FLYIMG_LOCAL_SOURCE_ROOT_PATH: Path inside the container where images are stored (/data by default).
FLYIMG_DEFAULT_IMAGE: Default image to use if none is specified in the URL.
FLYIMG_CACHE_EXPIRY: Cache expiration time in seconds.
FLYIMG_ENABLE_CACHE: Set to true to enable caching.
FLYIMG_CACHE_DRIVER: Cache driver (redis in this setup).
FLYIMG_CACHE_PREFIX: Prefix for cache keys.

# Volumes
./data: Local directory for storing images.
./flyimg_cache: Local directory for storing cache data.

# Troubleshooting
Port Conflicts: If you encounter port conflicts, make sure the ports defined in docker-compose.yml are not used by other services.
