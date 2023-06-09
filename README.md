[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/hacs/integration)

# hass-aqi-icons

AQI Custom icon pack designed for Home Assistant.

## Generic content

![Preview](./svg/very-good.svg) Very Good<br />
![Preview](./svg/good.svg) Good<br />
![Preview](./svg/fair.svg) Fair<br />
![Preview](./svg/poor.svg) Poor<br />
![Preview](./svg/very-poor.svg) Very Poor<br />
![Preview](./svg/hazardous.svg) Hazardous<br />
## Install

### HACS
Add this repo via HACS as a plugin and install.  See the [HACS install guide](./HACS_INSTALL.md) for step by step instructions.

### Manual
Copy the `hass-aqi-icons.js` file into `<config>/www/` where `<config>` is your home-assistant config directory (the directory where your `configuration.yaml` resides).

Add the folowing to the `frontend` section of your `configuration.yaml`

```yaml
frontend:
  extra_module_url:
    - /local/hass-aqi-icons.js
```

Or add the following to your lovelace configuration using the Raw Config editor under Configure UI or ui-lovelace.yaml if using YAML mode.

```yaml
resources:
  - type: js
    url: /local/hass-aqi-icons.js
```

Restart home-assistant.

## Using
The icons uses the prefix `aqi:`.

Example:

```
entities:
  - entity: light.floor_lamp
    icon: 'aqi:fair
    name: floor-lamp
show_header_toggle: false
title: hass-aqi-icons
type: entities
```

## FAQ
Q: The icon ain't showing, it's just white space where it should be. What's up with that?

A: Probably related to cache. Try opening your instance in a incognito/private Window and see if your icon shows then. If yes, it's cache related. If not, spellcheck.

## Thanks
Thanks to @thomasloven, as I used his hass-fontawesome as a template for this pack

Thanks to @prairiesnpr, @kmlucy, @GeorgeSG, @shbatm, @clemalex824 and @rautesamtr for their contributiuons
