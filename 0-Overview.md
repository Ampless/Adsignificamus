# Chapter 0 – An overview
There are many different DSBMobile API implementations and most of
them…are the same. This is because of pydsb (1), which can be
considered the reference implementation of the Android API. But there
are still three different APIs known to us, and two more with only one
implementation each.

## The APIs
* The Android API (chapter 1)
* The Web API (chapter 2)
* The iOS API (doesn't work, chapter 3)

## The implementations
This is an incomplete list of DSBMobile API implementations:

###### [Amplessimus](https://github.com/Ampless/Amplessimus/blob/master/amplissimus/lib/dsbapi.dart)
* Language: Dart
* API: Android
* Supported data types: plans
* Supported extra features: sorting and searching, an app even better than DSBMobile
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.heinekingmedia.dsbmobile
* Simulated Device: Samsung Galaxy S8 (SM-G950F)
* Simulated Version: 2.5.9
* Simulated OS Version: 29 10.0
* Simulated Language: German (de)

###### [pydsb (1)](https://github.com/sn0wmanmj/pydsb/blob/master/pydsb/__init__.py)
* Language: Python
* API: Android (2.x), iOS (1.x)
* Supported data types: plans, news, postings
* Supported extra features: DSB-based previews
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.heinekingmedia.dsbmobile
* Simulated Device: Pixel 3
* Simulated Version: 2.5.9
* Simulated OS Version: 27 8.1.0
* Simulated Language: German (de)

###### [OpenDSBMobile](https://github.com/KaiJan57/OpenDSBmobile/blob/master/app/src/main/java/com/kai_jan_57/opendsbmobile/network/RequestSenderTask.java)
* Language: Java
* API: Android
* Supported data types: plans, news, postings
* Supported extra features: full reimplementation of the DSBMobile app
* Supported requests (theoretically): 0 (DataUnknown), 1 (GetData), 2 (MailType), 3 (FeedbackType), 4 (SubjectsType), 5 (ErrorType), 6 (PushSettings)
* Supported requests (in reality): 1 (GetData)
* Simulated Bundle ID: unknown (maybe de.heinekingmedia.dsbmobile)
* Simulated Device: (empty)
* Simulated Version: 2.5.9
* Simulated OS Version: (empty)
* Simulated Language: Your OS language

###### [DSBMobile-API](https://github.com/Sematre/DSBmobile-API/blob/master/src/main/java/de/sematre/dsbmobile/DSBMobile.java)
* Language: Java
* API: Android
* Supported data types: plans, news
* Supported extra features: user-agent spoofing by default
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.heinekingmedia.dsbmobile
* Simulated Device: Nexus 4
* Simulated Version: 2.5.9
* Simulated OS Version: 27 8.1.0
* Simulated Language: German (de)

###### [DSBApi](https://github.com/nerrixDE/DSBApi/blob/master/dsbapi/__init__.py)
* Language: Python
* API: Android
* Supported data types: plans
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.heinekingmedia.dsbmobile
* Simulated Device: Samsung Galaxy S7 (SM-G930F)
* Simulated Version: 2.5.9
* Simulated OS Version: 27 8.1.0
* Simulated Language: German (de)

###### [DSBAPI](https://github.com/TheNoim/DSBAPI/blob/master/src/index.js)
* Language: JavaScript
* API: Android
* Supported data types: returns the raw json (+experimental filtering)
* Supported extra features: user-agent spoofing by default
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.digitales-schwarzes-brett.dsblight
* Simulated Device: iPhone
* Simulated Version: 2.5.6
* Simulated OS Version: 13.2.2
* Simulated Language: English (en-DE)

###### [dsb-go](https://github.com/irgendwr/dsb-go/blob/master/dsb.go)
* Language: Go
* API: Android
* Supported data types: plans, news
* Supported extra drawbacks: custom user-agent ("dsb-go")
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.heinekingmedia.dsbmobile
* Simulated Device: Nexus 4
* Simulated Version: 2.5.9
* Simulated OS Version: 27 8.1.0
* Simulated Language: German (de)

###### [Vertretungsplangak\_Bot (1)](https://github.com/MakerStuff/Vertretungsplangak_Bot/blob/master/dsbapi/dsbsession_android.py)
* Language: Python
* API: Android
* Supported extra drawbacks: no parsing
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.heinekingmedia.dsbmobile
* Simulated Device: Samsung Galaxy S7 Edge (SM-G935F)
* Simulated Version: 2.5.9
* Simulated OS Version: 28 9
* Simulated Language: German (de)

###### [Vertretungsplangak\_Bot (2)](https://github.com/MakerStuff/Vertretungsplangak_Bot/blob/master/dsbapi/dsbsession_web.py)
* Language: Python
* API: Web
* Supported extra drawbacks: no parsing, constant Date and LastUpdate
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.heinekingmedia.inhouse.dsbmobile.web
* Simulated Device: WebApp
* Simulated Version: 2.3
* Simulated OS Version: a good User Agent (Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.70 Safari/537.36)
* Simulated Language: German (de)

###### [dsbmobile-php-api](https://github.com/irgendwr/dsbmobile-php-api/blob/master/dsb_api.php)
* Language: PHP
* API: Android
* Supported data types: plans, news
* Supported extra features: faked referer header
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.heinekingmedia.inhouse.dsbmobile.web
* Simulated Device: WebApp
* Simulated Version: 2.3
* Simulated OS Version: an empty string
* Simulated Language: German (de)

###### [pydsb (2)](https://github.com/ScholliYT/pydsb/blob/master/pydsb.py)
* Language: Python
* API: iOS
* Supported data types: plans, news (seems weird, may not work)

###### [DSBMobileBot](https://github.com/ScholliYT/DSBMobileBot/blob/master/scraper/src/dsbmobil_scraper.py)
* Language: Python
* API: iOS
* Supported data types: plans

###### [myplan](https://github.com/jrheiner/myplan/blob/master/app/src/main/java/de/myplan/android/MyplanService.java)
* Language: Java
* API: iOS
* Supported data types: plans
* Supported extra features: a custom app (havent tried it, might be cool)

###### [DSBot](https://github.com/sargantana/DSBot/blob/master/scraper)
* Language: Shell (wget)
* API: Unknown (looks like Web at first glance, but is significantly different)
* Supported data types: plans (not 100% sure about that)
* Supported extra drawbacks: no parsing

###### [DSB - Abrage](https://forum.iobroker.net/topic/19140/dsb-abrage)
* Language: JavaScript
* API: iOS
* Supported data types: plans, news

###### [Untitled](https://pastebin.com/ds0AjK6T)
* Language: Python
* API: iOS
* Supported data types: plans

###### [vertretungsplan.io](https://codeberg.org/vertretungsplan/integration-dsb/src/branch/master/src/client/index.ts)
* Language: TypeScript
* API: Unknown (mobileapi.dsbcontrol.de)
* Supported data types: plans, news, "documents" (idk what that is)
