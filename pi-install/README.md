Pi-install
=========

Installs containers on *-pi.

Requirements
------------

Docker installed. By default debian 12 for orange-pi has docker.

Role Variables
--------------

`nmtui` config for network;  
`nmtui.inf` interface;  
`nmtui.type` type of interface;
`nmtui.ip4` ip4 of pi for static ip and dns;  
`nmtui.gw4` ip4 of main router.  

`secrets` secrets;  
`secrets.sing_box` secrets for sing-box;  
`secrets.sing_box.vless_ip` ip of proxy server;  
`secrets.sing_box.vless_pbk` public key on xray;  
`secrets.sing_box.vless_sid` short id on xray;
`secrets.sing_box.vless_sni` sni on xray;  
`secrets.sing_box.vless_uuid` uuid of connection on xray.

Example Playbook
----------------

```yaml
---
- name: Setup Pi(debian 12, 6.1)
  hosts: zero3
  vars_files:
    - pi-install/vars/main.yml
    - pi-install/vars/secrets.yml
  roles:
   - pi-install
```
License
-------

None, i don't know any

Author Information
------------------

Cool a bit.