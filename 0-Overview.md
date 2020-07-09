# Chapter 0 – An overview
There are many different DSBMobile API implementations and most of
them…are the same. This is because of pydsb, which can be considered
the reference implementation of the Android API. But there are still
three different APIs known to us.

## The APIs
* The Android API (chapter 1)
* The Web API (chapter 2)
* The iOS API (doesn't work, chapter 3)

## The implementations
This is an incomplete list of DSBMobile API implementations:

###### [Amplissimus](https://github.com/Amplissimus/Amplissimus/blob/master/amplissimus/lib/dsbapi.dart)
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

###### [pydsb](https://github.com/sn0wmanmj/pydsb/blob/master/pydsb/__init__.py)
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
