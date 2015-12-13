# AzureEvoHome
Azure logic apps for connecting evohome to various IoT data aggregation platforms

#limitations
- Currently only handles evohome accounts where there is a single location. If your account has more than one location, only the first will be processed.

#How to use?
- First, sign up for Azure subscription (https://azure.microsoft.com/en-gb/pricing/free-trial/).
- create a new resource group and add an empty logic app.
- Ultimately, you'll probably find that you need to use one of the standard hosting tariffs as anything less doesn't support 5 minute exection granularity.
- grab the https://github.com/mnbf9rca/AzureEvoHome/blob/master/pullDataFromHoneywell.json file. This contains the core code to pull the sensor data from Honeywell. You must enter your username and password in the paramaters at the top.
- Fetch one or more of the "connector" actions - ive created them for ubidots.com, thethings.io and thingspeak.com
- add this data to pullDataFromHoneywell.json. You can add more than one action (e.g. push data to any or all 3 services if you like), just remember to put a comma between each action.
