ansible-role-sshd-host-keys
===========================

A simple role that just contacts a ssh host CA providing the host
public key, and gets back a signed certificate which is
installed. Modifies sshd_config and ssh_config appropriate to work in
a CA environment.

Requirements
------------

It's expected that you use another role such as
https://github.com/jabl/ansible-role-ssh-hostca-srv
to setup the host CA signing service that this role depends on.

Role Variables
--------------

See defaults/main.yml

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-sshd-host-keys-client  }

License
-------

MPL 2.0

Author Information
------------------

https://github.com/jabl

