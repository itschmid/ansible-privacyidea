itschmid.privacyidea
====================

Ansible Role to installing and configuring [privacyIDEA](https://privacyidea.org) in a python virtualenv.
[privacyIDEA](https://privacyidea.org) is a Two Factor Authentication System which is multi-tenency- and multi-instance-capable. 

Example Playbook
----------------

Simple default install

    ---
    - hosts: all
      gather_facts: yes

      roles:
        - role: itschmid.apache_wsgi
          tags: install
        - role: itschmid.mariadb
          tags: install
        - itschmid.privacyidea

      vars:
        mariadb: privacyidea
        PI_PACKAGE_VERSION: v2.23.3
        PI_ADMIN_PASSWORD: admin


