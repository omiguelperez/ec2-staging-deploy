omiguelperez.ansible_role_fzacademy_staging_deploy
=========

With this role we can deploy FZ academia platform to staging machines.


Role Variables
--------------

AWS config vars:
```yml
region: sa-east-1
```

Github repos vars:
```yml
deploy_repo: fzacademy-deploy
backend_repo: fzacademy-api
client_repo: fzacademy-ssr
```

Docker services config vars:

```yml
docker_network: fzacademy_network
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
         - { role: omiguelperez.ansible_role_fzacademy_staging_deploy }
```

License
-------

BSD

Author Information
------------------

[Oscar Pérez](https://github.com/omiguelperez)
