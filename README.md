Sample node.js app deployment with Ansible
===

Install ansible: [Ansible](http://docs.ansible.com/intro_installation.html)


Deploying app
--
```
cd deploy
ansible-playbook deploy.yml -i demo -u root -e env=demo
```

VM Import Service Role
--
aws iam create-role --role-name vmimport --assume-role-policy-document file://trust-policy.json

aws iam put-role-policy --role-name vmimport --policy-name vmimport --policy-document file://role-policy.json
