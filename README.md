```markdown
# miksible                      

miksible is a word i that i created for combinig MikroTik and Ansible, with miksible, configuring mikrotik devices is not boring anymore :0

## Requirements

- Ansible (obviously) 
- `community.routeros` collection installed
- A MikroTik device

## Inventory

The playbook is intended to run against MikroTik routers defined in an Ansible inventory file. An example of a basic inventory (`inventory.yml`):

```yaml
[mikros]
mikrotik1 ansible_host=192.168.1.2
mikrotik2 ansible_host=192.168.1.3
mikrotik3 ansible_host=192.168.1.4
```

## Variables

The following variables can be customized in the playbook:

- `network1`: Network for the first LAN (default: `172.16.100.0/24`)
- `network1_interface`: IP address for the first LAN interface (default: `172.16.100.254`)
- `network1_pool`: DHCP address pool for the first LAN (default: `172.16.100.20-172.16.100.200`)
- `network2`: Network for the second LAN (default: `172.16.101.0/24`)
- `network2_interface`: IP address for the second LAN interface (default: `172.16.101.254`)
- `network2_pool`: DHCP address pool for the second LAN (default: `172.16.101.20-172.16.101.200`)
- `network3`: Network for the third LAN (default: `172.16.102.0/24`)
- `network3_interface`: IP address for the third LAN interface (default: `172.16.102.254`)
- `network3_pool`: DHCP address pool for the third LAN (default: `172.16.102.20-172.16.102.200`)
- `dns_servers`: DNS servers to be used by DHCP (default: `8.8.8.8,8.8.4.4`)

## Usage

Run the playbook using the following command:

```bash
ansible-playbook -i inventory.yml miksible.yml
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Author

Abolfazl Pahlavanian
```

You can modify the content as needed to fit your style or any specific instructions for using your playbook. Let me know if you need further assistance!
