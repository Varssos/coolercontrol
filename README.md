# coolercontrol

Ansible role to install and configure [CoolerControl](https://gitlab.com/coolercontrol/coolercontrol) fan and pump control software on Debian/Ubuntu systems.

## Requirements

- Debian or Ubuntu host
- `become: true` privileges (sudo)
- `curl` available on the target host

## Role Variables

| Variable | Default | Description |
|---|---|---|
| `coolercontrol_package_name` | `coolercontrol` | Package name to install via apt |
| `coolercontrol_service_name` | `coolercontrold` | Systemd service to enable and start |
| `coolercontrol_setup_script_url` | `https://dl.cloudsmith.io/public/coolercontrol/coolercontrol/setup.deb.sh` | URL of the repository setup script |

## Example Playbook

```yaml
- hosts: all
  become: true
  roles:
    - role: coolercontrol
```

## License

MIT

## Author

Varssos