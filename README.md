# ansible-fadecandy
Ansible role for installing a [Fadecandy](https://github.com/scanlime/fadecandy/) server and configuration.

## Configuration via host vars
The fcserver.json is generated from Ansible variables.  For example:

```yaml
fadecandy_config:
    listen: ["0.0.0.0", 7890]
    verbose: true
    color:
        gamma: 2.5
        whitepoint: [1.0, 1.0, 1.0]
    devices:
      -
        type: fadecandy
        map: [
          # [ OPC Channel, First OPC Pixel, First output pixel, Pixel count  ]
          [ 0, 0, 0, 50 ],
          # [ OPC Channel, First OPC Pixel, First output pixel, Pixel count, Color channels  ]
          [ 0, 50, 64, 12, 'grb' ]
        ]
```
