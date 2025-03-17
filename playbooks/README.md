# Playbooks

## Running Playbooks

Bootstrap Notes:

 1. If the system has been reimaged you need to clear out the local known_hosts entry
   -  `ssh-keygen -f /root/.ssh/known_hosts -R node04`
 2. You need to run ssha to start the SSH agent, as the key is encrypted
 3. Run bootstrap playbooks as root
   - cd /local/ansible
   - ansible-playbook playbooks/bootstrap-nodes.yml
   - ansible-playbook playbooks/update-nodes.yml


## Old 

Login to each node (node04) to accept SSH key. The ansible.cfg now should auto
accept these, so this is no longer necessary. 


The old way to create a password. But this is no longer needed because Ansible
can do this internally. 

`mkpasswd --method=SHA-512 --rounds=500000`
