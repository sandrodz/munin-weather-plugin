Munin weather plugin written in Ruby
====================

This is an asterisk **plugin weather_*** that collects environmental weather data.

API provided by http://worldweatheronline.com  
Get your free API key http://developer.worldweatheronline.com/  
Plugin demo: http://amindi.idev.ge

#### Data collected
1. cloudcover.value
2. humidity.value
3. precipMM.value
4. pressure.value
5. temp_C.value or temp_F.value
6. visibility.value
7. windspeed Kmph or Miles

#### Configuration example
Add configuration to the end of this file **/etc/munin/plugin-conf.d/munin-node**
```
[weather_*]
env.api_key cn5tkxfnwtkjtaccdccpu3ew
env.temperature_unit C # or F
env.speed_unit Kmph # or Miles
```

#### Dependencies
gem install json
