## CRITs-install-script

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

https://github.com/krys3331/CRITs-install-script
```

Give executable mod for all files
``` bash

cd CRITs-install-script

chmod +x ./*

```

## STEP 2

In directory with repository run "start": f. e.
``` bash

./start
````
If console print:
``` bash

"Do you want to start 'mongod' now? [yn] " yn

```
press "y" and "Enter".


After script completion in your home directory added directory "crits".
```bash

/home/"Your user"/crits
```


## STEP 3

Change dir to crits directory
```bash

cd /home/"Your user"/crits/crits
```
Run mongodb:
```bash

./contrib/mongo/mongod_start.sh
```

Create new admin:
```bash

python2 ./manage.py users -a -u admin -e "Your email" -R UberAdmin
```

Run server:
```bash

./script/server
```

**----------------------------------**
