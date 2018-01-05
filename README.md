Role Name
=========

This is a role for install of Git, and any version of NodeJS for either nvm, or a production server install

Requirements
------------

It is possible you need to update the sudoers file on RedHat based systems for the following before running this role, this has to do with the OS, you may need to add /usr/local/bin to it

Defaults    secure_path = /sbin:/bin:/usr/sbin:/usr/bin:/usr/local/bin

Role Variables
--------------

vars/main.yml, change these depending on where you want things to go, or what versions you want to install.

Dependencies
------------

None

Example Playbook
----------------

```yaml

  -   hosts: servers
      become: yes # I would use no for a nvm install, but still use the -K opt in running
      vars:
          install_type: server # Also can be for a nvm install
      roles:
      -   linux_nodejs_ms_sql_webserver

```

License
-------

MIT

Author Information
------------------

### Contact Information:  e_ben_75-python@yahoo.com
### If you have any questions e-mail me

### LinkedIn: [Ben Trachtenberg](https://www.linkedin.com/in/ben-trachtenberg-3a78496)
### Docker Hub: [Ben Trachtenberg](https://hub.docker.com/r/btr1975)
### Github Hub: [Ben Trachtenberg](https://github.com/btr1975)
### Ansible Galaxy: [Ben Trachtenberg](https://galaxy.ansible.com/btr1975)
