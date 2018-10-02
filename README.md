Run Tercen using Docker.

# Setup
Install [docker-compose](https://docs.docker.com/compose/install/).for Linux or Wondows or Mac.


Clone the following repository
```bash
git clone https://github.com/tercen/tercen_docker.git
cd tercen_docker
```

Activate shared drives (Windows and Mac only)
* right click on the running docker service and select "settings">"shared drives"
* share the folder tercen_docker 

Then start tercen ...

```bash
docker-compose pull
docker-compose up
```

Go to [http://127.0.0.1:5402](http://127.0.0.1:5402)

