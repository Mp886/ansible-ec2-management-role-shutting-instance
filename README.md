# Role Name
=========
This role is used to shut down EC2 instances where the `os_family` is `debian`.

## Requirements
------------
Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

- Ansible 2.9 or higher
- AWS credentials configured
- `boto3` and `botocore` packages installed

## Role Variables
--------------
A description of the settable variables for this role should go here, including any variables that are in `defaults/main.yml`, `vars/main.yml`, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (i.e., hostvars, group vars, etc.) should be mentioned here as well.

### defaults/main.yml
```yaml
# EC2 instances to shut down
ec2_instances_to_shutdown: 
  - instance_id: "i-0123456789abcdef0"
    os_family: "debian"

## Dependencies
   ------------

Dependencies
A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

# Example Playbook
  ----------------

- hosts: localhost
  gather_facts: yes
  roles:
    - role: username.rolename
      when: ansible_facts['os_family'] == "Debian"

