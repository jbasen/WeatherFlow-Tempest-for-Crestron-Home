# WeatherFlow-Tempest-for-Crestron-Home

This driver allows a WeatherFlow Tempest Weather System to be integrated with a 4-
Series Crestron Home processor. Data from the WeatherFlow Tempest will be displayed
in the driver’s UI in the Crestron Home app or on a touch panel connected to the Crestron
home processor. In addition the driver can be configured to trigger events for rain,
lightening, high wind, high temperature, and low temperature to drive other actions on
the Crestron Home processor

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

https://sdkcon78221.crestron.com/sdk/Crestron_Certified_Drivers_SDK/Content/Topics/CH-Testing.htm#Side

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

VERY IMPORTANT - Please be aware that you have to be very careful if you need to uninstall
the driver.  First, you need to use the Crestron Home Setup App to remove the driver from 
the room you installed it in. Then you need to back your way out of the room the driver was 
in, back out of the home setup app in general, wait two minutes, and reboot the processor 
to try and make sure that your system has fully synchronized with the change.

At that point you can use the Toolbox File Manager tool to delete the driver package from your 
Crestron Home system. It is all too easy to screw this up or rush the process, and then the driver 
can get stuck in the room. If this happens, then you will have to fully reset your Crestron 
Home system to get things straightened out.

