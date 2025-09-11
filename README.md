# IPC Firmware

Firmware dumps from different IP cameras.

## Why?

That's how we learn: we break things and then use the knowledge gained to make better things.

## How to contribute

1. Dump the camera's flash.
2. Name the dump according to the naming convention.
3. Create a pull request.

### Naming convention

Dash-separated names of the following format:

```
[camera_model]-[soc]-[sensor]-[wifi_module]-[tag].bin
```

- **camera_model** is underscored Camera Brand and Model
- **soc** is System-on-Chip variant
- **sensor** is Image Sensor model
- **wifi_module** is Wi-Fi Module Chip
- **tag**:
  - _virgin_ for a dump taken from an unpowered camera
  - _stock_ for a previously powered camera

### Why tag is important?

Many cameras provision themselves when they are first powered on, adding initial configuration to the flash. Therefore, it is important to know whether the dump was taken from a virgin camera or not.

## How to dump a flash

I recommend to use a modded [CH341A Programmer](https://github.com/themactep/thingino-firmware/wiki/CH341A-Programmer) and [scriba](https://github.com/themactep/scriba) for dumping the flash. That is the most reliable way to get a correct dump.

Open the camera, locate the flash chip and dump it using the flash programmer. Make two readings back to back, then compare their hashes. If they are the same, you have a good dump. If not, repeat the process until you get a good dump. Scriba has a built-in hash comparison feature, which makes the whole process easier.

## Support

If you have any questions, feel free to ask them on the [Discord server](https://discord.gg/bw8AVjS4ZZ) or in the [Telegram group](https://t.me/thingino).

If you like this project, consider [saying thank you](https://github.com/sponsors/themactep).

## License

No license.
No strings attached, no responsibility taken.
I just want to see you smart.

