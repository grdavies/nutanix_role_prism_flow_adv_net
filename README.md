# Nutanix Role to enable Flow Advanced Networking on Prism Central

This Ansible role enables Flow Advanced Networking on Prism Central.


## Role Variables

| Variable                                          | Required | Default | Choices                   | Comments                                                                                               |
|---------------------------------------------------|----------|---------|---------------------------|--------------------------------------------------------------------------------------------------------|
| nutanix_pulse_host                                | yes      |         |                           | The IP address or FQDN for the Prism (Element or Central) where you want to configure pulse.           |
| nutanix_pulse_username                            | no       | "admin" |                           | A valid username with appropriate rights to access the Nutanix API. where you want to configure pulse. |
| nutanix_pulse_password                            | yes      |         |                           | A valid password for the supplied username.  where you want to configure pulse.                        |
| nutanix_pulse_port                                | no       | 9440    |                           | The Prism TCP port  where you want to configure pulse.                                                 |
| validate_certs                                    | no       | no      | yes / no                  | Whether to check if Prism UI certificates are valid.                                                   |
| nutanix_debug                                     | no       | no      | yes / no                  | Whether to output variable contents for debugging purposes.                                            |
| enable_flow_adv_net                               | no       | no      | yes / no                  | Set value to 'yes' to enable Flow Advanced Networking.                                                 |


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
