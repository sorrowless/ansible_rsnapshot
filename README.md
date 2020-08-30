sbog/rsnapshot
==============

Role to install and configure rsnapshot.

#### Requirements

Ansible 2.4

#### Role Variables

```yaml
rsnapshot:
  backup_user: backuper
  create_backup_users: false
  create_ssh_keys: false
  master: false
  snapshot_root: /var/cache/rsnapshot/
  retain_daily: 7
  retain_weekly: 2
  logfile: /var/log/rsnapshot.log
  pid_directory: /var/run/rsnapshot
  rsync_ssh_port: 909
  link_dest: 1
  backups: []
  dailytimer: "05:30"
  weeklytimer: "Monday *-*-* 04:30:00"
  on_failure: False
```

#### Dependencies

None

#### Example Playbook

```yaml
- name: Install and configure Rsnapshot
  hosts: localhost
  remote_user: root
  roles:
    - rsnapshot
```

#### License

Apache 2.0

#### Author Information

Stanislaw Bogatkin (https://sbog.ru)
