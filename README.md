macklus.os
==========

Simple Operating System tools

Role Variables
--------------

    macklus:
      os:
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


* **macklus.os.packages.latest.all:** Array of packages to install
* **macklus.os.packages.latest.debian:** Array of packages to install (Debian family specific names)
* **macklus.os.packages.latest.redhat:** Array of packages to install (RedHat family specific names)
* **macklus.os.packages.absent.all:** Array of packages to remove
* **macklus.os.packages.absent.debian:** Array of packages to remove (Debian specific names)
* **macklus.os.packages.absent.redhat:** Array of packages to remove (RedHat specific names)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      remote_user: root
      roles:
        - macklus.os/repository
        - macklus.os/packages
        - macklus.os/upgrade
        - macklus.os/reboot

License
-------

GPL-3.0-only