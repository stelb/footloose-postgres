# postgres setup with ansible

## Features

* streaming replication
* backup with pgbackrest prepared
* service ip with keepalived (WIP)
* performance monitoring with powa
* testing with [footloose](https://github.com/weaveworks/footloose )
* Support for CentOS/RHEL/Debian

## Requirements

* docker
* footloose
* ansible >2.8

## Test with footloose

Test will be done with CentOS

    $ docker network create postgres-cluster
    $ footloose create
    ...
    $ ansible-playbook postgres.yml
    $ footloose ssh root@db0

Debian Tests cannot be done with images provided by footloose, as python is missing

## pgrestbackup

    $ /usr/bin/pgbackrest backup --stanza db01live


