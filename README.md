[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)

# hass-sotima-icons

Custom icon pack designed for Home Assistant for personal use / shamelessly copied from kongo09 https://github.com/kongo09/hass-kongo09-icons

## Content

![Preview](./svg/window-shutter-group.svg) window-shutter-group<br />
![Preview](./svg/window-shutter-group-partly.svg) window-shutter-group-partly<br />
![Preview](./svg/window-shutter-group-open.svg) window-shutter-group-open<br />
![Preview](./svg/window-shutter-partly_1.svg) window-shutter-partly<br />
![Preview](./svg/window-shutter-schedule.svg) window-shutter-schedule<br />
![Preview](./svg/chip-ota.svg) chip-ota<br />


## Install

### HACS
Add `https://github.com/sotima/hass-sotima-icons` as custom-repository for a Lovelace plugin in [HACS](https://hacs.xyz/docs/faq/custom_repositories/)

### Manual
Copy the `hass-sotima-icons.js` file into `<config>/www/` where `<config>` is your home-assistant config directory (the directory where your `configuration.yaml` resides).

Add the folowing to the `frontend` section of your `configuration.yaml`

```yaml
frontend:
  extra_module_url:
    - /local/hass-sotima-icons.js
```

Or add the following to your lovelace configuration using the Raw Config editor under Configure UI or ui-lovelace.yaml if using YAML mode.

```yaml
resources:
  - type: js
    url: /local/hass-sotima-icons.js
```

Restart home-assistant.

## Using
The icons uses the prefix `custom:`.

Example:

```
type: entity
entity: fan.air_ac2729
icon: 'custom:power_button'
```

## Thanks
Thanks to @kongo09 as I have shamelessly copied his repo.
