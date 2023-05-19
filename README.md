postfix
=========

Ansible role to configure postfix with a email relay in order to send emails from the server.


Role Variables
--------------

```yaml
myhostname: "{{ ansible_hostname }}"
smtp_address: smtp.example.com
relay_port: 465
mail_relay_email: email@example.com
mail_relay_password: examplepassword
```


Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: darsh12.mail
  vars:
    smtp_address: smtp.example.com
    relay_port: 465
    mail_relay_email: exmail@example.com
    mail_relay_password: examplepassword
```
However, if you do not want to specify the email and password in the playbook you can leave those variables empty and you will be prompted for the input

```yaml
- hosts: all
  roles:
    - role: darsh12.mail
  vars:
    smtp_address: smtp.example.com
    relay_port: 465
```

License
-------

BSD

Author Information
------------------

darsh12
