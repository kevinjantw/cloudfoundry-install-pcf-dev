# Installation-PCF-Dev
A installation guide of Pivotal Cloud Foundry dev environment

## Install cf-cli
https://github.com/cloudfoundry/cli/releases  

## Check pcfdev version
```shell=
cf dev version
```
## Download ovf file
https://network.pivotal.io/products/pcfdev#/releases/1622

## Import ovf
```shell=
cf dev import ~/pcfdev-v0.xxx.0.ova
```
## Install pcfdev vm
```shell=
cf dev start
```
[Note] virtualbox host-only 192.168.11.1 is created automatically; pcfdev vm default occupies 192.168.11.11
       
## cf login
```shell=
cf login -a https://api.local.pcfdev.io --skip-ssl-validation -u admin -p admin
```
## pcf_dev snapshot
```shell=
cf dev suspend
cf dev resume
```

## Source
https://docs.pivotal.io/pcf-dev/install-windows-legacy.html
https://docs.pivotal.io/pcf-dev/import-ova.html
