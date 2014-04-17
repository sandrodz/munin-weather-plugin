Munin weather plugin written in Ruby
====================

This is an asterisk plugin that collects environmental weather data.

Api provided by worldweatheronline.com
Plugin demo: amindi.idev.ge

Data collected:
cloudcover.value
humidity.value
precipMM.value
pressure.value
temp_C.value or temp_F.value
visibility.value
windspeed Kmph or Miles

Configuration example:
[weather_*]
env.api_key cn5tkqfnutkjyaccducpu3ew
env.temperature_unit C # or F
env.speed_unit Kmph # or Miles

Dependencies:
gem install json
