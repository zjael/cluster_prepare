# Cluster prepare

Prepares node for cluster setup by:
- Disabling swap
- Enables promiscuous mode on specified interface - issue at https://github.com/danderson/metallb/issues/253

## Role Variables

```yaml
---
# Interface to enable promisc mode on
promisc_interface: 'wlan0'
```

## Example Playbook

```yaml
---
- hosts: all
  become: true

  vars:
    promisc_interface: 'wlan0'

  roles:
    - zjael.cluster_prepare
```

## License

MIT