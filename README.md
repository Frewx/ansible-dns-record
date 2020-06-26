# ansible-dns-record

Ansible playbook for creating or removing a dns record from a Windows Dns Server.

Supported Operating Systems;

* Windows Server 2003 or later

## USAGE

ansible-playbook apply-record.yml -vvv -e "action= record_name= record_type= record_value= record_zone="

- action: Create/create or Remove/remove
- record_name: Name of the record
- record_type: A/AAAA/CNAME/PTR
- record_Value: This will be required when creating records.
- record_zone: The zone of the record

# A Few Dry Run Examples 
 
- When creating: 

ansible-playbook apply-record.yml -vvv -e "action=Create record_name=ansible record_type=A record_value=192.168.1.10 record_zone=ansible.test"

- When removing:

ansible-playbook apply-record.yml -vvv -e "action=remove record_name=ansible record_type=A record_zone=ansible.test"
