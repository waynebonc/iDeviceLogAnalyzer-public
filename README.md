# iDevice Panic Log Analyzer
A quick and easy panic log extraction and analysis tool for iDevices.

<img src="https://github.com/waynebonc/iDeviceLogAnalyzer-public/blob/master/image.jpg" width="350">

## False Malware Detection
This app makes use of [Squirrel](https://github.com/Squirrel/Squirrel.Windows), a one click installation and update framework. Setup files produced with this framework have a habit of being falsely detected as various types of malware, such as a backdoor or trojan (see issue [#1204](https://github.com/Squirrel/Squirrel.Windows/issues/1204), [#1653](https://github.com/Squirrel/Squirrel.Windows/issues/1653)). The only fix for this is for me to codesign the application with a certificate, which incurs yearly $4xx costs. I have no intention on doing this due the project receiving only a handful of donations.

### Workaround for Windows 10 Users
- Make sure Virus and Threat Protection is on.
- Download Setup.exe from the Releases tab and run it. This will install the application.
- You should now get a Threats found notification and "Installation has failed" message.
- Close the installation has failed message and open "Virus and threat protection" from system settings.
- Click on Protection history. You should see "Threat quarantined".
- Drop down to view full threat information. Under affected items, confirm that the path contains "AppData\Local\iDevicePanicLogAnalyzer". You should also confirm the date and time of when it was quarantined. <b>Do not take this step lightly, it is very easy to mark harmful malware as safe.</b>
- From the Actions selector, select "Restore". Windows will prompt to confirm.
- Re-install the application with Setup.exe. If you did everything right, the installation should complete without any interruptions. The app should also open for the first time.

## Supported Devices
Officially supported are all iPhones, iPads and iPod touch on iOS 12 and later. I have successfully tested this as low as iOS 10.3.3, but there are no guarantees it will work as expected.

## Requirements
iTunes or Apple Mobile Device Support must be installed.

## Supported Panic Logs
```bash
panic-full-*.ips
```

## Latest Version
v1.4.1

<sup>This repository is the updater endpoint.</sup>
