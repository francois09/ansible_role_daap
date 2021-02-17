DAAP Ansible role
==================

Role to manage DAAP.

Requirements
------------

No requirements

Role Variables
--------------

```
daap__install: Install or not (default: False)
daap__configure: Configure or not  (default: False)

daap__default_packages: # Package list
  - forked-daapd

daap__uid: <user running daemon> # eg: "daapd"
daap__logfile: <Full path of logfile> # eg: "/var/log/forked-daapd.log"
daap__loglevel: <log level> # eg: "log"

daap__friend_name: <Friendly name displayed on clients> # eg: "My music server"
daap__music_directories: <list of music dirs> # default to []

daap__music_password: <Password for music> # default to "", seems not working
daap__admin_password: <Password for admin> # default to ""

daap__port: <server port for music> # default null, should be 3689
daap__webport: <webadmin port> # default null
daap__mpd_port: <mpd port> # default null
```

Dependencies
------------

None

Example Playbooks
-----------------

```
- hosts: all
  name: Setup DAAP
  roles:
    - role: daap
```


License
-------

GPL V3

Author Information
------------------

François TOURDE
