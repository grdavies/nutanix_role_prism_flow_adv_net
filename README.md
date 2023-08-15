# Nutanix Role to enable Flow Advanced Networking on Prism Central

This Ansible role enables Flow Advanced Networking on Prism Central.


## Role Variables

| Variable                                          | Required | Default | Choices                   | Comments                                                                                               |
|---------------------------------------------------|----------|---------|---------------------------|--------------------------------------------------------------------------------------------------------|
| nutanix_host                                      | yes      |         |                           | The IP address or FQDN for the Prism Centra) where you want to enable the service.                     |
| nutanix_username                                  | no       | "admin" |                           | A valid username with appropriate rights to access the Nutanix API.                                    |
| nutanix_password                                  | yes      |         |                           | A valid password for the supplied username.                                                            |
| nutanix_port                                      | no       | 9440    |                           | The Prism TCP port                                                                                     |
| validate_certs                                    | no       | no      | yes / no                  | Whether to check if Prism UI certificates are valid.                                                   |
| nutanix_debug                                     | no       | no      | yes / no                  | Whether to output variable contents for debugging purposes.                                            |
| nutanix_flow_adv_net_enable                       | yes      |         | yes / no                  | Set value to 'yes' to enable Flow Advanced Networking.                                                 |


## Dependencies

None


## Example Playbook

```
- hosts: localhost
  gather_facts: false
  roles:
    - role: grdavies.nutanix_role_prism_flow_adv_net
  vars:
    nutanix_host: 10.38.179.39
    nutanix_username: admin
    nutanix_password: nx2Tech283!
    enable_flow_adv_net: yes
```


## License

See LICENSE.md

## Author Information

Ross Davies
