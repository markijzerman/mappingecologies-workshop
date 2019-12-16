# API calls

## Breezometer
Breezometer offers live free air quality data:
https://breezometer.com/air-quality-map

But we want to be able to use this within our project. Maybe something like this also exists for water quality?)
Some organisations offer API's: a gateway to the data that they offer, so you can use it somewhere else. In our case, we want to use it in TD or Max.
Most of the time you will need to sign up for a so-called "API Key", which gives you a personalized entrance to that data. From there you can then access that data to use in your project. Often the free version is limited to a X number of API calls per day- keep that into account.

Best idea is to sign up with a temporary e-mail address, so you can just make another account after your trial. It doesn't always work, but try signing up for a free e-mail at https://temp-mail.org.

With Breezometer, you can sign up for a free account here:
https://developers.breezometer.com/signup

Once you've got an API Key, we can look into how to get the data into TD or Max.

First try it in the browser:
https://api.breezometer.com/air-quality/v2/current-conditions?lat=48.857456&lon=2.354611&key=YOUR_API_KEY&features=breezometer_aqi,local_aqi,health_recommendations,sources_and_effects,pollutants_concentrations,pollutants_aqi_information

This will return a long list of information about that latitude/longitude.

## How to get the data into Touchdesigner
Touchdesigner mainly works by connecting nodes, but can easily be expanded with DAT-nodes which can also run Python. So it's a matter of finding a Python example of the API key we want to read out!

In the .toe examples you can find how to read out air quality data.
