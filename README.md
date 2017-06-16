# ansible-puppetagent

Ansible role for setting up puppet-agent. The main use-case is nodes which won't
be added to Ansible inventory.

# Usage

To setup puppet-agent on nodes that won't be managed by Ansible use a simple 
playbook such as "setup_puppetagent.yml":

    ---
    - name: install and configure puppet agent on a host
    hosts: all
    roles:
        - puppetagent

Then run ansible-playbook thusly:

    $ ansible-playbook -i <hostname>, server=<puppetserver-address> setup_puppetagent.yml

Notice the "," after the hostname - it is important when running the playbook on
just one node that is not in the inventory.
