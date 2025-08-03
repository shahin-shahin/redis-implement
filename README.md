# Redis Master-Slave Setup Using Docker Compose

This repository demonstrates how to set up a simple Redis Master-Slave replication environment using Docker Compose.

## 📦 Services

- **redis-master**: The primary Redis instance.
- **redis-slave**: A replica of the master, configured via `--slaveof`.

## 🚀 Quick Start

1. **Clone the repository** (if applicable):

   ```bash
   git clone <repo-url>
   cd <repo-folder>

Start the containers:

    docker-compose up -d

    Verify setup:

        Master Redis is accessible on port 6379.

        Slave Redis is accessible on port 6479.

        The slave replicates from the master.

🗂 Volume Persistence

    redis_master volume: Stores data for the master at /data.

    redis_slave volume: Stores data for the slave at /data.

On the host, these volumes are located under:

/var/lib/docker/volumes/redis_master/_data
/var/lib/docker/volumes/redis_slave/_data

🧹 Cleanup

To stop and remove all resources:

docker-compose down -v


