Munin weather_* plugin written in Ruby
====================

This is an asterisk plugin that collects environmental weather data.

API provided by http://worldweatheronline.com  

![Screenshot, day](https://raw.githubusercontent.com/wearede/munin-weather-plugin/screenshots/weather_tbilisi-day.png "Screenshot, day")
![Screenshot, Week](https://raw.githubusercontent.com/wearede/munin-weather-plugin/screenshots/weather_tbilisi-week.png "Screenshot, Week")

#### Data collected
1. cloudcover.value
2. humidity.value
3. precipMM.value
4. pressure.value
5. temp_C.value or temp_F.value
6. visibility.value
7. windspeed Kmph or Miles

#### Dependencies
```
gem install json
```

#### Configuration example
Add configuration to the end of this file **/etc/munin/plugin-conf.d/munin-node**
```
[weather_*]
env.api_key cn5tkxfnwtkjtaccdccpu3ew
env.temperature_unit C # or F
env.speed_unit Kmph # or Miles
```
Get your free API key here: http://developer.worldweatheronline.com/

#### Possible problems
```
/usr/bin/env: ruby: No such file or directory
```
Quick fix:
```
which ruby
/usr/local/rvm/rubies/ruby-2.1.1/bin/ruby
vi weather_
```

replace first line **#!/usr/bin/env ruby** with **#!/usr/local/rvm/rubies/ruby-2.1.1/bin/ruby** (result of which ruby command)

