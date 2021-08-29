<h1 align="center">Upcoming media card modification</h1>

<p align="center">
  A new render for <a href="https://github.com/custom-cards/upcoming-media-card">Upcoming Media Card</a> using <a href="https://github.com/thomasloven/lovelace-card-mod">Lovelace Card Mod</a>.
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/dylandoamaral/upcoming-media-card-modification/main/images/movie.png" alt="Movie Example" />
</p>

-----

## Installation 🏠

Use HACS to install:
- [Trakt Integration](https://github.com/dylandoamaral/trakt-integration) The integration creating a sensor with your own watching list using trakt
- [Upcoming Media Card](https://github.com/custom-cards/upcoming-media-card#installation) The card displaying upcoming movie/show
- [Lovelace Card Mod](https://github.com/thomasloven/lovelace-card-mod#installing) The integration allowing us to modify existing cards

Create a new upcoming card and modify its YAML:

```yaml
type: custom:upcoming-media-card
entity: sensor.trakt_upcoming_calendar
image_style: fanart
box_shadows: false
max: 3
clock: 24
date: mmdd
title_size: medium
line1_size: little
title_text: $title
line1_text: Released on $date
line2_text: " "
line3_text: " "
line4_text: " "
card_mod:
  style: |
    .type-custom-upcoming-media-card {
      background: none !important;
      box-shadow: none !important;
    }

    .type-custom-upcoming-media-card > div {
      padding: 0px !important;
    }

    .trak_fanart {
      background-size: cover !important;
      background-position: 50% 10% !important;
      border-radius: var(--ha-card-border-radius, 4px);
      background-color: rgb(100, 100, 100);
      background-blend-mode: multiply;
      height: 80px;
    }

    .trak_fan_fanart {
      background: none !important;
      box-shadow: none !important;
    }

```
