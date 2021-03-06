# user-playbook
Ansible playbook for normally manage user all of host in you control.

## Notation
Make sure [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html) and [Passlib](https://passlib.readthedocs.io/en/stable/install.html) is already installed.

## Create user

```console
$ ansible-playbook add-user.yml
```
This command wll show promt ask user name, password, groups, authorized key file path. <br />

_**`groups need use [ ] cover, if you have more than one group to add.`**_ <br />
Sample:
```console
What is user groups? []: [ "sudo", "docker" ]
```
<br />

Options: <br />
-k, --ask-pass
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
ask for connection password (if you don't login with ssh-key). <br />
-K, --ask-become-pass
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
ask for privilege escalation password (if you' don't login with root). <br />
--become-user=BECOME_USER
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
run operations as this user (default=root). <br />

Sample:
```console
$ ansible-playbook add-user.yml -k -K
```

## Remove user

```console
$ ansible-playbook remove-user.yml
```
This command wll show promt ask user name want to remove.
