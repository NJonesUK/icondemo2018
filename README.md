### Repeatable Kali Linux Builds

This is a set of ansible playbooks and the associated roles that can be used to provision new penetration testing VMs. To use:

- Create kali vm
- Run `pip install ansible` inside the VM
- Clone this repository into the VM
- In the repository root, run `ansible-playbook -i hosts -K playbooks/[PLAYBOOK]`

Current playbooks:

- `kali.yml` - General kali VM bootstrapping and installation of a bunch of common tools
- `git-repos.yml` - Cloning a large number of tools, useful documentation sets and so on
- `mobile.yml` - Installs a few common mobile app testing tools
- `docker.yml` - Installs docker and docker-compose
- `docugen.yml` - Generates documentation from any git repositories cloned into the directory defined by the `tools_dir` variable. Best run after the `git-repos.yml` playbook.

