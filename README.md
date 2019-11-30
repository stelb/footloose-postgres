# postgres setup with ansible

## Features

* streaming replication
* backup with pgbackrest prepared
* service ip with keepalived (WIP)
* performance monitoring with powa
* testing with [footloose](https://github.com/weaveworks/footloose )
* Support for CentOS/RHEL/Debian

## Test with footloose

Test will be done with CentOS

    $ footloose create
    ...
    $ ansible-playbook -i inventory postgres.yml

Debian Tests cannot be done with images provided by footloose, as python is missing
