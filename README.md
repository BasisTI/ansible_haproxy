# Ansible Role: HAProxy


An ansible role that installs haproxy on rhel/centos/fedora and debian/ubuntu. 

![Ansible Galaxy](https://github.com/BasisTI/ansible_haproxy/workflows/Ansible%20Galaxy/badge.svg)

## Tags:
## Variables:

* `haproxy_frontend`: `''` - Set frontend specs to HAProxy

example: 


```yaml
haproxy_frontend:
   - name: http-in
     bind_address: any
     bind_port: 80
     mode: http
     default_backend: servers
```

* `haproxy_backend`: `''` - Set backend specs to HAProxy

example: 


```yaml
haproxy_backend:
   - name: servers
     mode: http
     balance_method: roundrobin
     servers:
       - name: server_one
         address: 127.0.0.1:8000
```

* `haproxy_ha_enabled`: `'true'` - Enable or disable keepalived with float IP



* `keepalived_authentication_pass`: `'P@ssw0rd'` - Keepalived password peers


## License
Mit



Documentation generated using: [Ansible-autodoc](https://github.com/AndresBott/ansible-autodoc)

