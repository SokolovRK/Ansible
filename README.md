clntrl
======

Ansible role. Install openvpn client and start the service.

Requirements
------------

Ubuntu Server 16 Xenial Xerus

Variables
---------

```yaml
# Default settings
openvpn_cipher: BF-CBC          # Encryption algorithm
openvpn_comp_lzo: yes           # Enable compression
openvpn_dev: tun                # Device type
openvpn_host: 8.8.8.8           # Remote end of the tunnel
openvpn_port: 2195              # Port of the client and server
openvpn_protocol: udp           # Used protocol
openvpn_reneg_sec: 259200       # Re-authorization after a certain time

# Authentication settings
openvpn_auth_nocache: yes       # Login and password do not remain on the client side
# TLS block
openvpn_auth_tls: yes           # Use TLS key

```

Example Playbook
----------------

- hosts: all

  vars:
    openvpn_host: 8.8.8.8
    openvpn_port: 2195

  roles:
    - clntrl

  tags:
    - forclient

License
-------

MIT

Author Information
------------------

Sokolov RK
