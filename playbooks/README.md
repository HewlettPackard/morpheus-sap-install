
# Ansible Collection Playbooks

The playbooks in this directory can be directly integrated into HPE Morpheus enterprise.

## Usage of playbooks

### Integrate repository into HPE Morpheus Enterprise

Clone or fork this repository to a personal repository. This provides the possibility to change default parameter settings.

In the HPE Morpheus Enterprise software navigate to Library > Integrations and select + New Integration and select the integration type "ansible". Provide all necessary information to the personal repository.

Several input parameter have to be created in HPE Morpheus Enterpise.
Some parameter are set to default values. They are set either in the variables file that is integrated into a playbook or in the defaults/main.yml of a role.

Input parameter are passed on in the HPE Morpheus Enterprise task of the respective playbook. 


#### Example: 

For the SAP HANA installation playbook sap-hana-install.yml, the input parameter are passed on as extra variables:

--user root --extra-vars '{"ansible_python_interpreter":"<%= customOptions.ansible_python_interpreter %>","sap_hana_install_master_password":"<%= customOptions.sap_hana_install_master_password %>","sap_hana_install_software_extract_directory":"<%= customOptions.sap_hana_install_software_extract_directory %>","sap_hana_install_software_directory":"<%= customOptions.sap_hana_install_software_extract_directory %>","sap_hana_install_sid":"<%= customOptions.sap_hana_install_sid %>","sap_hana_install_instance_number":"<%= customOptions.sap_hana_install_instance_number %>"}'
