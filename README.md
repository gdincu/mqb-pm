# Performance Monitor for Hyundai Elantra CN7

This is an adapted version of [this](https://github.com/jilleb/mqb-pm) app. 

It displays custom PIDs for Hyundai Elantra CN7 (it might also work with other Hyundai/ Kia/ Genesis vehicles that use similar custom PIDs).

This works together with Torque Pro (play.google.com/store/apps/details?id=org.prowl.torque) and uses a list of custom PIDs (see apk/OilTempPID.csv) for:
- Oil temperature
- Engine coolant temperature
- Current gear

A basic how-to guide is available at apk/HowTo.txt

<img src="https://github.com/gdincu/mqb-pm/raw/HyundaiElantraCN7/apk/Screenshot.jpeg">

# Known issues
- Google is actively blocking custom apps for Android Auto. So the app is not working with Android Auto v3.0 (unless you apply the workaround). Its also not working on Google Play Services v12.5.21. There are workarounds, but I will not describe or support them. 

- Black screen of death: On some cars it doesn't work for unknown reasons. This will not kill your car or headunit. Send me a logcat. 
On Huawei and Honor devices this is a common problem, caused by a bug in their ROMs. A workaround to get OEM apps working again is to clear the Android Auto apk cache when this happens. (thanks to nerone-github for the information.)

- No data
If you don't see any data in the app, it can have various reasons:
Some cars don't provide any data to the headunit. Workaround: Use Torque with an OBD2 dongle to get data. 
Some MIB2 firmware versions don't provide data to the exlap channel.
Not all data elements are available on all cars. If one element doesn't provide data, try an other one.
Most cars do not report oil and coolant temperatures below 50.
Most cars do not report any turbo pressure. Consider yourself lucky when your car does.

- Appkillers/memory managers kill the service
Put the Vag extensions for Android Auto app in the whitelist of your memory manager.

- Phone locking causes data to stop
Some phones kill the datafeed as soon as the screen is locked. This doesn't happen with all phones.

# What to do when it's not working?
- Try choosing a different type of data in the settings app. Not all cars have all data available. Reconnect to the car after you've done this.
- Check if you have applied all rights. Did you open the settings app after installing? Did you install both APK's?
- Unplug/replug your phone and try again
