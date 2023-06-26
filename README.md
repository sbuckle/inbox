The following parameters need to be specified when running the Ansible playbook:
* hostname - the name of the server
* domain - the domain to receive email for

Here's an example of how to run the playbook: 
```shell
ansible-playbook -i mail.hlsbook.net, -u mailer -e domain=hlsbook.net -e hostname=mail.hlsbook.net playbook.yml
```
