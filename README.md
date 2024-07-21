# Ansible Fedora Automatic Upgrades

I have a number of VMs I very sparodically spin up, these can be years out of date, and require updating to the latest version of Fedora.

This automatically upgrades a server, in a max of 2 versions each step.

> [!NOTE]
> Reboots are handled automatically.

## Instructions

    ansible-playbook fedoraUpdate.yml -i <IP/HOST>,[<IP/HOST>,]... [--extra-vars "override_version=<version>"]

> [!WARNING]
>  The trailing comma in the list of hosts is **required**

If you want to upgrade to a specific version you can use the variable `override_version`

e.g:

    ansible-playbook fedoraUpdate.yml -i host.lan, --extra-vars "override_version=39"