el7_cockpit
=========

A role to install and configure Cockpit (https://cockpit-project.org/) on an EL7 host, including optional configuration of non-standard port,

Requirements
------------

- libselinux-python: must be installed to support changing selinux context for custom port

Role Variables
--------------

cockpit_packages:  The following packages are configured to be installed as default
- cockpit-dashboard
- cockpit-pcp
- cockpit-shell
- cockpit-storaged
- cockpit-system
- cockpit-packagekit

cockpit_port: If not set set, cockpit will use the default TCP\9090.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: dotmjs.el7_cockpit, cockpit_port: 9091 }

License
-------

BSD
