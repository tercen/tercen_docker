# General FAQ

#### Can I modify the tercen configuration?
Tercen uses docker-compose and therefore verycustomizable. There is a docker-compse configuration yaml file which defines the current settings.
There are two main mechanisms to modify the config
* modify the yaml file
* use environment variables to override any settings in the yaml file

The following are typical modifications:
* where tercen keeps the data
* integrating with a specific file system
* placing a nginx front end
* integrating with an existing user authentification system

#### Where is the data?
The volumes (i.e foldres) are indicated in the docker yaml configuration file and it can be modified to point to alternative locations.
Currently there are two volumes defined in the configuration file the `tercen-data`and `couchdb-data`

For windows, there is an extra layer, it is in the virutal hardisk of virtual PC ( on windows, the mobylinux virtual hardware is located
`C:\Users\Public\Documents\Hyper-V\Virtual hard disks\MobyLinuxVM.vhdx`

#### Can I add a nginx frontend?
Yes, tercen is using http and websocket on port 5400 or 5402 ... can be 
changed using tercen docker-compose file.

#### Can I add a LDAP directory for user?
Yes, but it requries implementation from our side, send email to `info@tercen.com`

#### How do we integrate with JuypterHub?
We are not sure yet but are will to investigate

#### How to integrate with BeeGFS?
A BeeGFS docker volume plugin is available.
https://github.com/RedCoolBeans/docker-volume-beegfs
A demo video
https://youtu.be/pUXzBqmfrdk?t=1355

In current docker-compose file Tercen is using 2 volumes one for the 
meta data and the other for data.
Can be changed using tercen docker-compose file.

#### What is the mnt point for the data?
Right now tercen compose file is using docker volumes, but can be 
changed using tercen docker-compose file, a specific folder can mounted.

#### Where is the data located?
Depends on docker-compose file configuration.

#### How to limit resources (cpu/harddisk) limitations for users?
It's done per Tercen team owner.

#### How to handle permission for users?
Not possible in current version.
Any authenticated user can access anything.

####  What rights does the r processes have
Tercen launches the R computation in a self contained docker. The R code can has only permissions inside this docker.



