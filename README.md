
## Ansible tutorial.
### According to this video series: 
https://www.youtube.com/playlist?list=PLT98CRl2KxKEUHie1m24-wkyHpEsa4Y70

1. Adding a new host.
Changes to be made:
- add changes to `/inventory` file
- add file to `/host_vars` directory
- if needed, add a new sshd template to `/roles/base/templates` directory

2. Creating `simone` user with sudo privileges without password.
- in `/ansible-2.cfg` file change `remote_user` variable with the current sudo user
- run `ansible-playbook --ask-become-pass bootstrap.yml`
- in `/ansible-2.cfg` file change `remote_user` variable to `simone`

3. Running the main playbook.
- run `ansible-playbook site.yml`