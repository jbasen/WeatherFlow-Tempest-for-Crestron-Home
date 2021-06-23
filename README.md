# WeatherFlow-Tempest-for-Crestron-Home

This driver allows a WeatherFlow Tempest Weather System to be integrated with a 4-
Series Crestron Home processor. Data from the WeatherFlow Tempest will be displayed
in the driver’s UI in the Crestron Home app or on a touch panel connected to the Crestron
home processor. In addition the driver can be configured to trigger events for rain,
lightening, high wind, high temperature, and low temperature to drive other actions on
the Crestron Home processor

This driver is released as shareware. It is free for Crestron programmers to use in their
own homes or dealers to use in demo systems in their show rooms. However, if this
driver is used in customer systems, where the dealer or programmer will profit from it,
then I ask for a simple, one time payment of $100. That gives the dealer or programmer
the right to use this driver on as many customer systems as they want. Please contact me
at jay.m.basen@gmail.com to arrange for payment.
When the WeatherFlow driver is installed, you will be prompted for the serial number of
the Tempest weather station in the format ST-XXXXXXXX. The driver monitors the
UDP broadcast traffic produced by the Tempest weather system on the homeowner’s
network. In the event, for whatever reason, there is more than one Tempest weather
system on the network, the driver will use the serial number to differentiate the traffic and
only act on the UDP messages from the desired Tempest weather system. If the serial
number is not entered correctly the driver will not accept the messages from the
homeowner’s weather station.

The driver can be installed on a 4-Series Crestron Home processor through side loading.
The process of side loading a driver is described here:

https://sdkcon78221.crestron.com/sdk/Crestron_Certified_Drivers_SDK/Content/Topics/
CH-Testing.htm#Side

IMPORTANT – The UI for driver settings in Crestron Home is very slow. You need to
be very patient and give Crestron Home several seconds after changing a field in the
settings. Even with patience the UI can crash.

In addition to displaying the current weather conditions, the driver can be configured to
trigger events for rain, lightening, high wind, high temperature, and low temperature to
drive other actions on the Crestron Home processor. To configure these events press the
settings button on the driver’s UI. On the settings page a series of checkboxes for
enabling/disabling events is displayed along with text entry fields for entering limits;
such as the temperature below which will generate a low temperature event. Again, be
very patient, typing slowly and waiting several seconds before moving between fields to
avoid crashing the Crestron Home App.

When you have completed the configuration of the events, press the save button. 

Be aware that events will be triggered each time the Crestron Home processor receives a
UDP message from the Tempest weather station that meets the specified criteria. 
