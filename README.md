omiguelperez.ec2_staging_deploy
=========

With this role we can deploy FZ academia platform to staging machines.


Role Variables
--------------

Global vars:
```yml
github_org_name: your_org_name
project_domain: yourdomain.com
```


AWS config vars:
```yml
region: sa-east-1
```

Github repos vars:
```yml
deploy_repo: org-deploy
backend_repo: org-backend
client_repo: org-web
```

Docker services config vars:

```yml
docker_network: project_network
services:
  - 3.web
  - 2.backend
  - 1.lb
```

Keys vars:
```yml
github_ssh_keys:
  - id_rsa.pub
  - id_rsa
```


Example Playbook
----------------

```yml
    - hosts: servers
      roles:
         - { role: omiguelperez.ec2_staging_deploy }
```

License
-------

BSD

Author Information
------------------

[Oscar Pérez](https://github.com/omiguelperez)
