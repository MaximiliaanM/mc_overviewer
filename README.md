mc_overviewer
=========

Installs Minecraft Overviewer that generates a webpage to display your minecraft world as an interactive map using Leaflet.

Requirements
------------

- A minecraft world save file
- A webserver to host the generated webpage (recommended)

Role Variables
--------------

| Variable    | Choices                                                                                                       | Comment                                                                                                                                                                                                    |
| :---------- | :------------------------------------------------------------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `name`      |                                                                                                               | Specifies which world this render corresponds to.                                                                                                                                                          |
| `path`      |                                                                                                               |        Path where your minecraft world save file is located                                                                                                                                                                                                    |
| `title`     |                                                                                                               | This is the display name used in the user interface. Set this to whatever you want to see displayed in the Map Type control (the buttons in the upper- right).                                             |
| `dimension` | overworld, nether, end                                                                                        | Specified which dimension of the world should be rendered. Each Minecraft world has by default 3 dimensions: The Overworld, The Nether, and The End.                                                       |
| `render`    | normal, lighting, smooth_lighting, night, smooth_night, nether, nether_lighting, nether_smooth_lighting, cave | This is which rendermode to use for this render. There are many rendermodes to choose from. This can either be a rendermode object, or a string, in which case the rendermode object by that name is used. |
| `outputdir` |                                                                                                               | This is the path to the output directory where the rendered tiles will be saved.                                                                                                                           |

Example Playbook
----------------

```yaml
  - hosts: servers
    roles:
      - role: mc_overviewer
        vars:
          worlds:
            - { name: "My  world", path: "/home/username/server/world", title: "Normal Render of my World", dimension: "overworld", render: "normalrender" }
          outputdir: "/home/username/mcmap"
``` 

License
-------

MIT License

Author Information
------------------

Maximiliaan Muylaert
[Github](https://github.com/MaximiliaanM)
[Website](https://maximiliaanmuylaert.be/)
