# Oprek Bareng
Learn Nomad, Consul, Ansible by Hashicorp

## Requirements Install

1. Install Visual Studio Code (menyesuaikan OS)

1. Install Remote SSH Extension (https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh)

## Starting the lab

1. Generate SSH Config from vagrant

```
vagrant ssh-config > ssh_config
```

# Consul (Hashicorp)

minimal 3 'consul server'
node lain sebagain 'consul client'

- 1 master
- 2 node


1. Service discovery

    Fungsinya adalah mendiscover service di data center

    ex: app butuh database, dari pada ip ne database di taruh di app manual, bisa lewat consul. otomatis update kalau ip ne database berubah

    consul-template

    ```
    db_host=database.service.consul
    db_user={{ key 'foo/db_user' }}
    ```

2. Distributed key value store

