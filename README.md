# CRITs-install-script

This script make you installation CRITs very easy.

# Script tested on:

* Ubuntu 20.04.5 LTS (Focal Fossa) Desktop
* Ubuntu 20.04.5 LTS (Focal Fossa) Server
* Debian 10 buster

## If Debian 10 buster!!!

You need install and configure "sudo".

# How use it

## STEP 1

Clone this repository:
``` bash

git clone https://github.com/krys3331/CRITs-install-script
```

Give executable mod for all files
``` bash

cd CRITs-install-script

chmod +x ./*

```

## STEP 2

In directory with repository run "install_script":
``` bash

./install_crits
````
After script completion in directory "/data" added directory "crits".
```bash

/data/crits
```


## STEP 3

Change dir to crits directory
```bash

cd /data/crits
```
Create new admin:
```bash

python2 ./manage.py users -a -u admin -e "Your email" -R UberAdmin
```

Run server:
```bash

./script/server'
```

# Installing services

## STEP 1

In directory with repository run command
```bash

./install_service
```
## STEP 2

In directory with CRITs use command
```bash

python2 manage.py setconfig service_dirs /data/crits_services
```
**----------------------------------**

# ATTENTION

After every restarting your system, you must start mongodb

```bash

/data/crits/contrib/mongo/mongod_start.sh
```
