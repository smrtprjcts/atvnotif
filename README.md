# Android TV Notifier

Android TV Notifier is an Android app that allows users to send notifications from phone or tablet to an Android TV.
It can immediately forward app notifications from your mobile device to your Android TV. Including the application logo, content image or the incoming caller/sms sender contact image.<br>
You can also send custom notifications using automation apps like **Tasker, Macrodroid**, etc.

[![Github All Releases](https://img.shields.io/github/v/release/smrtprjcts/atvnotif?label=Release&logo=github&display_name=release)]()
[![Github All Releases](https://img.shields.io/github/downloads/smrtprjcts/atvnotif/total.svg?label=APK%20Downloads&logo=github)]()

# Download / Installation

**Minimum requirements:** Android 7 or higher.<br>

**Supported devices:** every Android and Google TV (real TV devices and TV Boxes, like Xiaomi Miboxes), Amazon Fire TV and some special devices (e.g.: GE Kitchen Hub).<br> If you need support for any device, drop me an [e-mail](mailto:smrtprjcts+atvnotif@gmail.com)

## Google Play version
* Has restrictions required by Google for publishing on Google Play (SMS and call permissions). These differences are only affect the mobile side working (so installing the Github version doesn't give any advantage on the TV site)
* **Get it on [Google Play](https://play.google.com/store/apps/details?id=com.smrtprjcts.atvnotif)**

[<img src="https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png" alt="Get it on Google Play" height="80">](https://play.google.com/store/apps/details?id=com.smrtprjcts.atvnotif)

## Github version
* Has no restrictions. It includes the SMS and call permissions. Useful on mobiles, not on TVs.
* Via **[GitHub Releases](https://github.com/smrtprjcts/atvnotif/releases)** the [latest release](https://github.com/smrtprjcts/atvnotif/releases/latest/download/ATVNotifier-github-release.apk)

[<img src="https://raw.githubusercontent.com/ismartcoding/plain-app/main/assets/get-it-on-github.png" alt="Get it on GitHub" height="80">](https://github.com/smrtprjcts/atvnotif/releases)

## Important 
**Permissions**
* **Draw over other apps permission**: Permission required to create an overlay. Depending on the Android version and manufacturer this option may not be available on a system setting menu. In this case, you will have to enable it via ADB command:\
\
adb shell appops set com.smrtprjcts.atvnotif SYSTEM_ALERT_WINDOW allow

* **Battery optimization**: This step is optional, but recommended to avoid the app being killed by the system. If the the battery optimization permission isn't granted on the TV the app may be killed  by the system after a while. Then the mobile device won't be able to communicate with the TV. You can grant it in the settings of the TV. To turn off the energy optimization, go to:\
Settings -> Apps -> Special App Permissions -> Energy Optimization and select the Android TV Notifier app.\
But this menu may differ depending on the manufacturer and Android version.<br>
If you cannot access the system option to disable battery optimizationn, you may have to enable it via ADB command:\
\
adb shell dumpsys deviceidle whitelist +com.smrtprjcts.atvnotif
