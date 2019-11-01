# ansible-role-prometheus-node-exporter-legacy
Install Prometheus Node Exporter on older init.d-based systems


## Requirements

Designed for RedHat/CentOS 6; should work on any system that uses init.d and chkconfig.


## Role Variables

`node_exporter_version`: Defaults to '0.18.1'. Change it if you need a newer version.

See defaults/main.yml for other customizations.


## Dependencies

None


## Example Playbook
```yaml
- hosts: rhel-6-servers
  gather_facts: true
  become: true
  roles:
   - name: Install prometheus node exporter
     role: acromedia.node-exporter-legacy
     node_exporter_version: '0.18.1'
     tags:
       - prometheus
```


## License

GPLv3

## Author Information

Acro Media Inc.
