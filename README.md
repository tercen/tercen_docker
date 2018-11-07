Run Tercen using Docker.

# Setup
Install [docker-compose](https://docs.docker.com/compose/install/) for Linux or Windows or Mac.


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
docker-compose up
```

Go to [http://127.0.0.1:5402](http://127.0.0.1:5402)


To update tercen

```bash
git pull
docker-compose down
docker-compose up
```

To uninstall

```bash
docker-compose down
# check tercen docker volumes names
docker volume ls
# delete tercen docker volumes
docker volume rm tercendocker_couchdb-data
docker volume rm tercendocker_tercen-data
```