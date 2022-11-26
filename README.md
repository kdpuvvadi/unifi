# Unifi Controller Ansible playbook

Tested on Control Node Ubuntu 20.04 LTS. Ansible 2.14.0

## Setup Ansible

* Install pip `sudo apt install python3-pip -y`
* Install ansible with `pip install -r requirements.txt`

> It also installs `ansible-lint` and `yamllint`. To only install ansible `pip install ansible`

## Installed Packages

* `OpenJDK 8 Headless`
* `MongoDB`
* `curl`
* `jsvc`
* `tar`
* `ca-certificates` 
* `apt-transport-https`

## Run

* Clone the repo `git clone https://github.com/kdpuvvadi/unifi.git unifi`.
* Install requirements `ansible-galaxy collection install -r requirements.yml`.
* Inventory with `cp inventory.ini.j2 inventory.ini`.
* Setup inventory.
* Variables with `cp vars.yml.j2 vars.yml`.

## Run the playbook

* Run `ansible-playbook main.yml` append `-K`
* if you need password for `sudo` for root access on your host. `ansible-playbook main.yml -K`

## Post Install

* unifi controller will be available on `https://HOST-IP:8043/`.


## unifi Service on host

* `sudo service unifi status`     -- show the status of Controller.
* `sudo service unifi restart`     -- restart the unifi Controller.
* `sudo service unifi stop`     --stop running the unifi Controller.

## LICENSE

[MIT](./LICENSE)
