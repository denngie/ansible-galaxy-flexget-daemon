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
flexget_daemon_irc_nickname: The IRC nickname you want
flexget_daemon_rsskey: Your RSS key on the tracker
flexget_daemon_trakt_account: Your trakt account name
```

Default variables:
```yaml
flexget_daemon_content_path: Base path for your torrents, media files and scripts
flexget_daemon_venv_path: Flexget virtualenv installation path
flexget_daemon_trakt_hdr_list: Trakt list name for HDR series
flexget_daemon_trakt_sdr_list: Trakt list name for SDR series
```

Dependencies
------------

Not a dependency but this role is intended to be used with my other role denngie.qbittorrent_nox

Example Playbook
----------------

```yaml
---
- name: Apply flexget_daemon role
  hosts: flexget-server
  roles:
    - role: denngie.flexget_daemon
      vars:
        flexget_daemon_irc_nickname: galaxy_bot
        flexget_daemon_rsskey: abcdefghij0123456789
        flexget_daemon_trakt_account: galaxy_trakt
```

License
-------

MIT
