[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)

# hass-pap-icons

Custom icon pack designed for Home Assistant containing icons for Philips Air Purifier.

## Content

![Preview](./svg/ceiling-fan.svg) ceiling-fan<br />
![Preview](./svg/ceiling-fan-light.svg) ceiling-fan-light<br />
![Preview](./svg/ceiling-lamp.svg) ceiling-lamp<br />
![Preview](./svg/ceiling-lamp-plafond.svg) ceiling-lamp-plafond<br />
![Preview](./svg/ceiling-lamp-round.svg) ceiling-lamp-round<br />
![Preview](./svg/chandelier.svg) chandelier<br />
![Preview](./svg/dome-light.svg) dome-light<br />
![Preview](./svg/floor-lamp.svg) floor-lamp<br />
![Preview](./svg/floor-lamp-dual.svg) floor-lamp-dual<br />
![Preview](./svg/led-strip.svg) led-strip<br />
![Preview](./svg/light-string.svg) light-string<br />
![Preview](./svg/outdoor-lamp.svg) outdoor-lamp<br />
![Preview](./svg/outdoor-lamp-solo.svg) outdoor-lamp-solo<br />
![Preview](./svg/outdoor-lamp-variant.svg) outdoor-lamp-variant<br />
![Preview](./svg/mirror-lamp.svg) mirror-lamp<br />
![Preview](./svg/path-light.svg) path-light<br />
![Preview](./svg/roborock.svg) roborock<br />
![Preview](./svg/smoke-detector.svg) smoke-detector<br />
![Preview](./svg/stairs.svg) stairs<br />
![Preview](./svg/table-lamp-variant.svg) table-lamp-variant<br />
![Preview](./svg/thermostat.svg) thermostat<br />
![Preview](./svg/xmas-candle-bridge.svg) xmas-candle-bridge<br />
![Preview](./svg/xmas-star.svg) xmas-star<br />


## Install

### HACS
Add this repo via HACS as a plugin and install.  See the [HACS install guide](./HACS_INSTALL.md) for step by step instructions.

### Manual
Copy the `hass-pap-icons.js` file into `<config>/www/` where `<config>` is your home-assistant config directory (the directory where your `configuration.yaml` resides).

Add the folowing to the `frontend` section of your `configuration.yaml`

```yaml
frontend:
  extra_module_url:
    - /local/hass-pap-icons.js
```

Or add the following to your lovelace configuration using the Raw Config editor under Configure UI or ui-lovelace.yaml if using YAML mode.

```yaml
resources:
  - type: js
    url: /local/hass-pap-icons.js
```

Restart home-assistant.

## Using
The icons uses the prefix `pap:`.

Example:

```
entities:
  - entity: light.floor_lamp
    icon: 'bha:floor-lamp'
    name: floor-lamp
  - entity: light.floor_lamp_dual
    icon: 'bha:floor-lamp-dual'
    name: floor-lamp-dual
  - entity: light.led_strip
    icon: 'bha:led-strip'
    name: led-strip
  - entity: light.outdoor_lamp_north
    icon: 'bha:outdoor-lamp'
    name: outdoor-lamp
  - entity: light.outdoor_lamp_west
    icon: 'bha:outdoor-lamp-variant'
    name: outdoor-lamp-variant
show_header_toggle: false
title: hass-bha-icons
type: entities
```

## FAQ
Q: The icon ain't showing, it's just white space where it should be. What's up with that?

A: Probably related to cache. Try opening your instance in a incognito/private Window and see if your icon shows then. If yes, it's cache related. If not, spellcheck.

## Thanks
Thanks to @hulkhaugen, as I used his hass-bha-icons based on hass-fontawesome from @thomasloven as a template for this pack
