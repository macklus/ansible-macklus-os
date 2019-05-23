macklus.so
==========

Simple Operating System tools

Role Variables
--------------

    macklus:
      so:
        repository:
          install: true
          country: 'fr'
        packages:
          latest:
            all: []
            debian: []
            redhat: []
          absent:
            all: []
            debian: []
            redhat: []
        reboot: 'always|only_if_necessary'


* **macklus.so.packages.latest.all:** Array of packages to install
* **macklus.so.packages.latest.debian:** Array of packages to install (Debian family specific names)
* **macklus.so.packages.latest.redhat:** Array of packages to install (RedHat family specific names)
* **macklus.so.packages.absent.all:** Array of packages to remove
* **macklus.so.packages.absent.debian:** Array of packages to remove (Debian specific names)
* **macklus.so.packages.absent.redhat:** Array of packages to remove (RedHat specific names)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      remote_user: root
      roles:
        - macklus.so/repository
        - macklus.so/packages
        - macklus.so/upgrade
        - macklus.so/reboot

License
-------

GPL-3.0-only