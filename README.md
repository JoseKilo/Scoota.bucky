# Scoota Bucky Role

[![Build Status](https://travis-ci.org/rockabox/Scoota.bucky.svg?branch=master)](https://travis-ci.org/rockabox/Scoota.bucky)

This is an Ansible role for installing [Bucky](https://github.com/trbs/bucky)
and start receiving your stats.

## Role variables:

    bucky_enabled: yes                 # Enable the role
    bucky_home: /opt/bucky             # Where to install

    bucky_port: 8125                   # Bucky listening port
    bucky_graphite_host: 127.0.0.1     # Hostname or IP of Graphite server
    bucky_graphite_port: 2003          # Line Receiver port of Graphite (Carbon)
    bucky_address: 0.0.0.0             # address to listen on over UDP

    bucky_additional_options: {}       # Setup additional options

## Testing

    virtualenv .venv
    . .venv/bin/activate
    pip install -r requirements/test.txt
    vagrant up --no-provision
    ansible-playbook tests/test.yml -i vagrant-inventory --private-key .vagrant/machines/scoota/virtualbox/private_key

See [vagrant docs](https://docs.vagrantup.com/v2/) for getting setup with
vagrant.
