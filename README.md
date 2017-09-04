Ansible Role : ImmPort Galaxy
=========

Installs and configures [ImmPort Galaxy](https://github.com/ImmPortDB/immport-galaxy)

WIP
---
this role is a work-in-progress and is part of an as-yet unfinished experiment. for (a little) more information, see the [containing project](https://github.com/dheles/immport-galaxy-ansible)

Requirements
------------

Python 2.7

Role Variables
--------------

ansible user used for deployment:

    login_user:                     "deploy"

minimum python version (though this may be the *only* version supported, IDK)

    immport_minimum_python_version: "2.7"

port of the http server. note: currently only using to check success in ansible, if you were to override it, it wouldn't actually propagate to the galaxy configuration; it'd just break the playbook

    immport_webserver_port:         8080

other, self-explanatory defaults:

    immport_repo:                   "https://github.com/ImmPortDB/immport-galaxy"
    immport_app_name:               "immport-galaxy"
    immport_server_dir:           "/home/{{ login_user }}/{{ immport_app_name }}"

Dependencies
------------

none

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: immport-galaxy }

License
-------

[CC0](https://creativecommons.org/publicdomain/zero/1.0/) - this role

AFL - [ImmPort Galaxy](https://raw.githubusercontent.com/ImmPortDB/immport-galaxy/master/LICENSE.txt) & [The Galaxy Project](https://raw.githubusercontent.com/galaxyproject/galaxy/dev/LICENSE.txt)
