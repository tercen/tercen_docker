Run Tercen using Docker.

# Linux Setup
Install [docker-compose](https://docs.docker.com/compose/).

Clone the following repository
```bash
git clone https://github.com/tercen/tercen_docker.git
cd tercen_docker
```

Then start tercen ...

```bash
docker-compose pull
docker-compose up
```

Go to [http://127.0.0.1:5402](http://127.0.0.1:5402)

# Windows Setup
1. install docker
    - create a docker account (i.e. docker id) 
    - download windowsCE for docker
    - run the windows install
    -logout and login to windows
2. activate one drive to be shared
    - Right click docker service
    - Choose settings
    - Go to shared drive
    - Activate one drive
3. clone tercen_docker  (git clone tercen_docker)
4. change to tercen_docker directory
5. open command promt and type "docker-compose up"
6. leave the command prompt open
7. tercen is now running

Go to [http://127.0.0.1:5402](http://127.0.0.1:5402)
