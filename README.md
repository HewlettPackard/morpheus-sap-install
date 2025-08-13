# Ansible SAP installation playbooks for HPE Morpheus Enterprise


## Description

This Ansible Collection executes various SAP Software installations and configuration tasks for various SAP solutions and deployment scenarios on supported Linux operating systems.
This set of roles and playbooks was tested for the use in HPE Morpheus Enterprise.
The roles and playbooks from https://github.com/sap-linuxlab/community.sap_install were used and slightly modified. Only tested roles and playbooks are part of this repository.

Included roles cover range of tasks:
- Installation of SAP Database
- Installation of SAP Products, like SAP S4HANA and SAP BW4HANA.

## Requirements

### Control Nodes
Operating system:
- Any operating system with required Python and Ansible versions.

Python: 3.11 or higher

Ansible: 9.9.x

Ansible-core: 2.16.x

**NOTE: Ansible 10 and ansible-core 2.17.x are not supported, because of breaking changes requiring higher Python version on managed nodes.**

### Managed Nodes
Operating system:
- Red Hat Enterprise Linux for SAP Solutions 8.x 9.x (RHEL4SAP)

**NOTE: Operating system needs to have access to required package repositories either directly or via subscription registration.**


Python: 3.6 or higher


## Installation Instructions

### Installation
For the use of the Ansible playbooks in HPE Morpheus Enterprise, a github repository can be directly integrated into the software.

## Use Cases

### Example Scenarios
- Installation of SAP HANA
- Installation of SAP S4HANA or other SAP products, including SAP system copy

More deployment scenarios are available in [ansible.playbooks_for_sap](https://github.com/sap-linuxlab/ansible.playbooks_for_sap) repository. However, the integration was not tested with HPE Morpheus Enterprise.

### Ansible Roles
All included roles can be executed independently.

| Name | Summary |
| :--- | :--- |
| [sap_hana_install](https://github.hpe.com/sonja-thumm/morpheus.sap_install/blob/main/roles/sap_hana_install/) | Install SAP HANA via HDBLCM |
| [sap_swpm](https://github.hpe.com/sonja-thumm/morpheus.sap_install/blob/main/roles/sap_swpm) | Install SAP Software via SWPM |


## Testing
This Ansible Collection was tested across different Operating Systems versions, SAP products and scenarios. You can find examples of some of them below.

Operating systems:
- Red Hat Enterprise Linux for SAP Solutions 8.x 9.x (RHEL4SAP)

SAP Products:
- SAP S/4HANA AnyPremise (1809, 1909, 2020, 2021, 2022, 2023) with setup as Standard, Distributed or Restore System Copy
- SAP BW/4HANA (2021, 2023) with setup as Standard, Distributed or Restore System Copy
- SAP HANA 2.0 (SPS04+) with setup as Scale-Up

**NOTE: It is not possible to test every Operating System and SAP Product combination with every release. Testing is regularly done for common scenarios: SAP HANA, SAP HANA HA, SAP S4HANA Distributed HA**

## Contributing to the sap-linuxlab community playbooks
You can find more information about ways you can contribute at [sap-linuxlab website](https://sap-linuxlab.github.io/initiative_contributions/).


## Support
You can report any issues with this set of playbooks and roles using the [Issues] section.


## Further Information

### Variable Precedence Rules
Please follow [Ansible Precedence guidelines](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_variables.html#variable-precedence-where-should-i-put-a-variable) on how to pass variables when using this collection.

### Getting Started
More information on how to execute Ansible playbooks is in [Getting started guide](https://github.hpe.com/sonja-thumm/morpheus.sap_install/blob/main/docs/getting_started/README.md).


## License
[Apache 2.0](https://github.hpe.com/sonja-thumm/morpheus.sap_install/blob/main/LICENSE) 
