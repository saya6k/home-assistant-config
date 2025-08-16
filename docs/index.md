---
title: Welcome to my Home Assistant Config!
---

=== "Home"

    ![Home](https://github.com/saya6k/home-assistant-config/blob/main/www/lovelace/overview.png?raw=true)

=== "Thread Network Map"

    ![Living Room](https://github.com/saya6k/home-assistant-config/blob/main/www/thread-map.png?raw=true){: loading=lazy }

=== "Monitoring"

    ![Monitoring](https://github.com/saya6k/home-assistant-config/blob/main/www/monitoring.png?raw=true){: loading=lazy }

=== "Energy"

    ![Energy](https://github.com/saya6k/home-assistant-config/blob/main/www/energy.png?raw=true){: loading=lazy }

[![GitHub Workflow Status][github-img]][github-url]
[![Last Commit][last-commit-img]][github-url]
[![Commit Activity][commit-activity-img]][github-url]
[![License][license-img]][license-url]
[![GitHub Stars][stars-img]][github-url]
[![Twitter Followers][twitter-img]][twitter-url]

This is my personal Home Assistant configuration, awakening my home with automations. I hope this will help you inspire to start your home automation journey.

<!-- prettier-ignore -->
!!!attention "Beware of changes"
    I constantly improve my home. It evolves as I add new devices and services. It's changing as my daily routines are changing.

    Please, keep in mind **this documentation might be outdated** in covering some details. However, I'll try my best to keep this updated.

The best way to discover new ideas and inspire is by [reading the code][github-url], copying-pasting parts of my configuration and adjusting it to your needs.

Read this documentation to see the bigger picture:

[Hardware](./hardware){: .md-button }
[Configuration](./config){: .md-button }
[Services](./services){: .md-button }
[Retired](./retired){: .md-button }
[Inspiration](./resources){: .md-button }

## What's inside?

My home setup for those who are too lazy to read everything:

- [Home Assistant](https://home-assistant.io) OS running on [Raspberry Pi 5 8GB](https://www.raspberrypi.com/products/raspberry-pi-5/).
- Various addons, such as [OpenThead Border Router](https://openthread.io/guides/border-router/), [Matter Server](https://csa-iot.org/all-solutions/matter/) and [xknx](https://xknx.io/home_assistant) for devices.
- Reverse proxy using [Nginx Proxy Manager](https://nginxproxymanager.com/) with [CloudFlare](https://www.cloudflare.com/).
- HomeLab services running as HA add-on.

## Motivation

I write this documentation for two main reasons:

1. **To keep track of growing my smart home.** To maintain an understanding of how things are working.
2. **To help other enthusiasts inspire.** People often ask about my smart home setup. Now I can give them a link to this documentation, instead of explaining everything once again.

## Limitations

I'm renting my apartment. My landlord handles fixing stuff in my home, covering all the expenses. The only downside is that I can't change anything in my home.

I can't disassemble anything and use custom switches or sockets. It means I can change only easily accessible parts, like bulbs.

## Future Plans

I have a [public kanban board][kanban-board] with ideas and tasks for my smart home. You can follow and comment my plans there.

[See future plans][kanban-board]{: .md-button }

## License

[MIT][license-url] © [saya6k][saya6k]

<!-- References -->

[kanban-board]: https://github.com/users/saya6k/projects/3
[github-url]: https://github.com/saya6k/home-assistant-config
[github-img]: https://img.shields.io/github/actions/workflow/status/saya6k/home-assistant-config/release.yml?style=flat-square
[last-commit-img]: https://img.shields.io/github/last-commit/saya6k/home-assistant-config?style=flat-square
[commit-activity-img]: https://img.shields.io/github/commit-activity/m/saya6k/home-assistant-config?style=flat-square
[license-url]: https://github.com/saya6k/home-assistant-config/blob/main/LICENSE.md
[license-img]: https://img.shields.io/github/license/saya6k/home-assistant-config?style=flat-square
[twitter-url]: https://twitter.com/saya6k
[twitter-img]: https://img.shields.io/twitter/follow/saya6k?label=Follow
[stars-img]: https://img.shields.io/github/stars/saya6k/home-assistant-config?style=social
[saya6k]: https://lyz.kr
