flexget_daemon
=========

Installs flexget on your Ubuntu server in daemon mode, using IRC as input with a tracker included as an example.

Requirements
------------

TBD

Role Variables
--------------

Mandatory variables:
```yaml
flexget_nickname: The IRC nickname you want
flexget_rsskey: Your RSS key on the tracker
trakt_account: Your trakt account name
```

Default variables:
```yaml
content_path: Base path for your torrents, media files and scripts
flexget_path: Flexget virtualenv installation path
trakt_hdr_list: Trakt list name for HDR series
trakt_sdr_list: Trakt list name for SDR series
```

Dependencies
------------

Not a dependency but this role is intended to be used with my other role qbittorrent-nox

Example Playbook
----------------

```yaml
---
- name: Apply flexget_daemon role
  hosts: flexget-server
  roles:
    - role: denngie.flexget_daemon
      vars:
        flexget_nickname: galaxy_bot
        flexget_rsskey: abcdefghij0123456789
        trakt_account: galaxy_trakt
```

License
-------

MIT
