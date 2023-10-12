```markdown
# Automating Package Installation with Ansible Playbooks

In Ansible, you can automate the process of installing packages on remote hosts using playbook files. For example, in the following playbook named `ansible-playbook.yml`, we'll install Python 3 on a target host machine.

```yaml
---
- name: Install Python3 on Ubuntu
  hosts: farm-app    
# you can pass directly the ip 50.22.70.12
# also if it is multiple then 
# hosts: 
#   - 23.50.18.21
#   - 52.30.80.12
  become: yes

  tasks:
    - name: Install Python3
      command: apt install python3 -y
```

This playbook has a single task to install Python 3 on the target machine.

## How to Execute the Playbook

To successfully execute this task, follow these steps:

1. Make sure you have Ansible installed on your system, as explained in the previous section.

2. Create an inventory file, `ansible-inventory`, with the necessary host information.

3. Run the Ansible playbook using the following command:

```shell
ansible-playbook -i ansible-inventory ansible-playbook.yml
```

This command will execute the playbook and install Python 3 on the specified target host (`farm-app`).

By using Ansible playbooks, you can easily automate the installation of packages, manage configurations, and perform various system administration tasks across multiple hosts, making your IT operations more efficient and streamlined.
