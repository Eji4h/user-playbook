# user-playbook
Ansible playbook for normally manage user.

## Notation
Make sure [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html) is already installed.

## Create user

```console
$ ansible-playbook add-user.yml
```
This command wll show promt ask user name, password, groups.

Options:
-k, --ask-pass              ask for connection password (if you don't login with ssh-key).
-K, --ask-become-pass       ask for privilege escalation password (if you' don't login with root).
--become-user=BECOME_USER   run operations as this user (default=root)

Sample:
```console
$ ansible-playbook add-user.yml -k -K
```

## Coming soon
Modify user, Remove user.
