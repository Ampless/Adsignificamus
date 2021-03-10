# Chapter 0 – An overview
There are many different DSBMobile API implementations and most of
them…are the same. This is because of pydsb (1), which can be
considered the reference implementation of the Android API. But there
are still three different APIs known to us, and two more with only one
implementation each.

## The APIs
* The Android API (chapter 1)
* The Mobile API (chapter 2)
* The Web API (chapter 3)
* The iOS API (chapter 4)

## The implementations
This is an incomplete list of DSBMobile API implementations:

### Mobile API

| Implementation                                                             | Language   | Data types             | Extra features        | Bundle ID                   | App Version | OS Version |
|----------------------------------------------------------------------------|------------|------------------------|-----------------------|-----------------------------|-------------|------------|
| [dsbuntis ≥3](https://github.com/Ampless/dsbuntis)                         | Dart       | Plans                  | Sorting and Searching | de.heinekingmedia.dsbmobile | 35          | 22         |
| [pydsb (1) ≥2.2](https://github.com/sn0wmanmj/pydsb)                       | Python     | Plans, News, Postings  | DSB-based Previews    | de.heinekingmedia.dsbmobile | 35          | 22         |
| [vertretungsplan.io](https://codeberg.org/vertretungsplan/integration-dsb) | TypeScript | Plans, News, Documents |                       | de.heinekingmedia.dsbmobile | (empty)     | (empty)    |

### Android API

| Implementation                                                                      | Language   | Data types            | Extra features & drawbacks  | Bundle ID                               | Device   | App Version | OS Version | Simulated Language          |
|-------------------------------------------------------------------------------------|------------|-----------------------|-----------------------------|-----------------------------------------|----------|-------------|------------|-----------------------------|
| [dsbuntis](https://github.com/Ampless/dsbuntis)                                     | Dart       | Plans                 | Sorting and Searching       | de.heinekingmedia.dsbmobile             | SM-G950F | 2.5.9       | 29 10.0    | configurable, de by default |
| [pydsb (1) 2.0-2.1](https://github.com/sn0wmanmj/pydsb)                             | Python     | Plans, News, Postings | DSB-based previews          | de.heinekingmedia.dsbmobile             | Pixel 3  | 2.5.9       | 27 8.1.0   | de                          |
| [OpenDSBMobile](https://github.com/KaiJan57/OpenDSBmobile)                          | Java       | Plans, News, Postings | reimplementation of the app | de.heinekingmedia.dsbmobile             | (empty)  | 2.5.9       | (empty)    | your os language            |
| [DSBMobile-API](https://github.com/Sematre/DSBmobile-API)                           | Java       | Plans, News           | User-Agent spoofing         | de.heinekingmedia.dsbmobile             | Nexus 4  | 2.5.9       | 27 8.1.0   | de                          |
| [DSBApi](https://github.com/nerrixDE/DSBApi)                                        | Python     | Plans                 |                             | de.heinekingmedia.dsbmobile             | SM-G930F | 2.5.9       | 27 8.1.0   | de                          |
| [DSBAPI](https://github.com/TheNoim/DSBAPI)                                         | JavaScript | raw json              | User-Agent spoofing         | de.digitales-schwarzes-brett.dsblight   | iPhone   | 2.5.6       | 13.2.2     | en-DE                       |
| [dsb-go](https://github.com/irgendwr/dsb-go)                                        | Go         | Plans, News           | User-Agent "dsb-go"         | de.heinekingmedia.dsbmobile             | Nexus 4  | 2.5.9       | 27 8.1.0   | de                          |
| [Vertretungsplangak\_Bot (1)](https://github.com/MakerStuff/Vertretungsplangak_Bot) | Python     | ?                     | no parsing                  | de.heinekingmedia.dsbmobile             | SM-G935F | 2.5.9       | 28 9       | de                          |
| [dsbmobile-php-api](https://github.com/irgendwr/dsbmobile-php-api)                  | PHP        | Plans, News           | faked Referer header        | de.heinekingmedia.inhouse.dsbmobile.web | WebApp   | 2.3         | (empty)    | de                          |

### Web API

[Vertretungsplangak\_Bot (2)](https://github.com/MakerStuff/Vertretungsplangak_Bot)
Python
* Supported extra drawbacks: no parsing, constant Date and LastUpdate
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.heinekingmedia.inhouse.dsbmobile.web
* Simulated Device: WebApp
* Simulated Version: 2.3
* Simulated OS Version: a good User Agent (Mozilla/5.0 (X11; Linux x86\_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.70 Safari/537.36)
* Simulated Language: German (de)

### iOS API

| Implementation                                                    | Language   | Data types            | Extra features     |
|-------------------------------------------------------------------|------------|-----------------------|--------------------|
| [pydsb (1) 1.x](https://github.com/sn0wmanmj/pydsb)               | Python     | Plans, News, Postings | DSB-based previews |
| [pydsb (2)](https://github.com/ScholliYT/pydsb)                   | Python     | Plans, News           |                    |
| [DSBMobileBot](https://github.com/ScholliYT/DSBMobileBot)         | Python     | Plans                 |                    |
| [myplan](https://github.com/jrheiner/myplan)                      | Java       | Plans                 | a custom app       |
| [DSB - Abrage](https://forum.iobroker.net/topic/19140/dsb-abrage) | JavaScript | Plans, News           |                    |
| [Untitled](https://pastebin.com/ds0AjK6T)                         | Python     | Plans                 |                    |

### Other

###### [DSBot](https://github.com/sargantana/DSBot)
Shell (wget)
* API: Unknown (looks like Web at first glance, but is significantly different)
* Supported data types: plans (not 100% sure about that)
* Supported extra drawbacks: no parsing

### Other interesting URLs

These are some resources for learing things, you might need while
building DSB API implementations:

* https://pastebin.com/7XZD38V5
* https://light.dsbcontrol.de/DSBlightWebsite/(S(kvgpcwcoqorwq3xxgbx42u2b))/Homepage/IFrame.aspx
