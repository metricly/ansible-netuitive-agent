# ansible-netuitive-agent
ansible playbook for netuitive agent

# Usage
This playbook will install, configure, and start the agent.

Important: This integration is for using our Ansible playbook to get our
Linux agent up and running on all of your machines simultaneously, NOT
to collect performance metrics on Ansible.

1. Copy the Netuitive Agent playbook to your Ansible directory.

```bash
cd /ansible
git clone https://github.com/Netuitive/ansible-netuitive-agent.git
```
2. Run the Netuitive Agent playbook, replacing hosts-file-name with the name of your hosts file.

```bash
ansible-playbook -i hosts-file-name netuitive-agent.yml --extra-vars=netuitive_linux_api=<your api key>
```

# Contributions
Big thanks to Daniel Dusina for contributing the original script/playbook.  
