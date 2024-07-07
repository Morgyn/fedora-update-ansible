I have a number of VMs I very sparodically spin up, these can be years out of date, and require updating to the latest version of Fedora.

This automatically upgrades a server, in a max of 2 versions each step.

Reboots are handled automatically.

    ansible-playbook fedoraUpdate.yml -i <IP/HOST>,[<IP/HOST>,]...

⚠ The trailing comma in the list of hosts is **required**
