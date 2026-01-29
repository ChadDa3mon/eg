# Playbooks

Base Playbook Examples
    ansible-playbook -i inventory.yml ubuntu-base-playbook.yaml -K
    ansible-playbook -i inventory.ini lab-eg.yaml
    ansible-playbook -i ~/scripts/ansible/inventory.ini ~/scripts/ansible/caddy.yaml

# Ad-Hoc commands
Simple command
    ansible -i ~/scripts/ansible/inventory.ini k3 -m shell -a "ls"

Run with "Become"
    ansible -i ~/scripts/ansible/inventory.ini k3 -m shell -a "ls" -b

Run with "Become" and prompt for sudo password
    ansible -i ~/scripts/ansible/inventory.ini k3 -m shell -a "ls" -b -K
