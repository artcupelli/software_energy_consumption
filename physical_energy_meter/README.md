# Measuring Energy Consumption using a Physical Device

In this subfolder I condensed all the experiments with a physical device meter.

## The Device
We used the Hiking DDS238-2 Smart Wi-Fi Energy Meter, which can easily be connected to the local network by the Smart Life app (for [iOS](https://apps.apple.com/br/app/smart-life-smart-living/id1115101477) and [Android](https://play.google.com/store/apps/details?id=com.tuya.smartlife&hl=pt_BR&gl=US&pli=1)).

_TODO: Add info on the circuit._


## Connecting with the Device Programmatically
Although it's not hard to see the instant data in the mobile app, we wanted a dinamic way to store a log of measurements refering to a specific timeframe.

The device is [Tuya compatible](https://developer.tuya.com/en/), so we managed to create an developer account and register our project. The plataform generated an access key to collect the desired information. 

An existing Python lib ([`tinytuya`](https://github.com/jasonacox/tinytuya)) already does the work to connect with a Wi-Fi device, given the access permission mentioned. Also, they explain in details on how to do all the process to create a Tuya developer account, registering the project, etc (see ther repository in the section "Setup Wizard - Getting Local Keys").


## Collecting the Data
Using `tinytuna`, we created a script that requests periodically measurements from the device.  

_TODO: Add info on the collected examples._
