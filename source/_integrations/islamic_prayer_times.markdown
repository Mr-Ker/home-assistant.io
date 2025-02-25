---
title: Islamic Prayer Times
description: Instructions on how to integrate the Islamic Prayer Times integration within Home Assistant.
ha_category:
  - Sensor
ha_iot_class: Cloud Polling
ha_release: 0.85
ha_config_flow: true
ha_domain: islamic_prayer_times
ha_codeowners:
  - '@engrbm87'
ha_platforms:
  - sensor
ha_integration_type: integration
---

The Islamic Prayer Times (`islamic_prayer_times`) integration displays the various prayer times for Muslims as sensors.

This platform calculates prayer times using the following calculation methods:

- Shia Ithna-Ansari
- Islamic Society of North America
- University of Islamic Sciences, Karachi
- Muslim World League
- Umm Al-Qura University, Makkah
- Egyptian General Authority of Survey
- Institute of Geophysics, University of Tehran
- Gulf Region
- Kuwait
- Qatar
- Majlis Ugama Islam Singapura, Singapore
- Union Organization islamic de France
- Diyanet İşleri Başkanlığı, Turkiye
- Spiritual Administration of Muslims of Russia
- Moonsighting Committee Worldwide

{% include integrations/config_flow.md %}

## Integration Sensors

The following sensors are added by the integration:

sensors:
  - fajr: Show the fajr prayer time for today.
  - sunrise: Show the sunrise for today which is the end of fajr prayer. This is a calculated field and may not necessarily be the same as the astronomical sunrise.
  - dhuhr: Show the dhuhr prayer time for today.
  - asr: Show the asr prayer time for today.
  - maghrib: Show the maghrib prayer time for today.
  - isha: Show the isha prayer time for today.
  - midnight: Show the midnight for today which is the end of isha prayer. This is a calculated field and is not the same as 12AM.
