ansible-role-sshd-host-keys
===========================

A simple role that just copies sshd host keys, certs and
ssh_known_hosts from a specified location.

Requirements
------------

It's expected that you use another role such as
https://github.com/CSC-IT-Center-for-Science/ansible-role-sshd-host-keys
to generate the keys, and yet another role such as
https://github.com/willshersystems/ansible-sshd to actually configure
sshd.

Role Variables
--------------

ssh_host_keys_dir specifies the root of the directory where the keys
are located. The keys are then in the subdirectory "{{
inventory_hostname }}/ssh".

The ssh_host_key_files variable specifies a list of private key names
to copy. The name of the corresponding public key and certificate is
automatically generated from that name.

    ssh_host_keys_dir: Directory where to copy the host keys from.
	ssh_host_key_files:
	 - ssh_host_ed25519_key
	   

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

GPLv3

Author Information
------------------

https://github.com/jabl

