mc_overviewer
=========

Installs Minecraft Overviewer that generates a webpage to display your minecraft world as an interactive map using Leaflet.

Requirements
------------

- A minecraft world safe file
- A webserver to host the generated webpage 

Role Variables
--------------



Example Playbook
----------------

```yaml
  - hosts: servers
    roles:
      - role: mc_overviewer
        vars:
          worlds:
            - { name: "Your worldname", path: "yuour path", title: "world title",render: "rendermode" }
          outputdir: "path to place generated webpage"
``` 

License
-------

MIT License

Author Information
------------------

Maximiliaan Muylaert
[Github](https://github.com/MaximiliaanM)
[Website](https://maximiliaanmuylaert.be/)
