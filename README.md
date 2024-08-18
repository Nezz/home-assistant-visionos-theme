# visionOS Theme

Theme inspired by visionOS for Home Assistant with automatic dark mode support.

![Demo day](https://github.com/Nezz/homeassistant-visionos-theme/assets/431167/1b1d9e34-ac45-4a8e-a801-789441cdf06c)
![Demo night](https://github.com/Nezz/homeassistant-visionos-theme/assets/431167/b503b0f0-3371-4a55-99bc-cf6152ad1510)


## Installation

1. You can install the theme with [HACS](https://hacs.xyz/docs/setup/download):

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Nezz&repository=homeassistant-visionos-theme&category=theme)

> [!NOTE]
> **If HACS is in experimental mode, the background images will not load.**
> You can disable it from Settings > Devices & services > HACS > Configure.
> 
> The background blur effects require Home Assistant 2024.5

2. You should see the "visionos" theme appear in your list of themes.

If it's missing, try reloading your themes or adding the following code to your `configuration.yaml` file (reboot required):

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

3. (Optional) You can set this as the default theme with the following automation:
```
alias: Frontend - Change theme
trigger:
  - platform: homeassistant
    event: start
action:
  - service: frontend.set_theme
    data:
      name: visionos
```

## Remarks

Based on [Bas Nijholt's iOS Themes](https://github.com/basnijholt/lovelace-ios-themes)
