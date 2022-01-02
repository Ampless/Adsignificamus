# Adsignificamus
These are some docs for heinekingmedia's DSBMobile APIs.
Additionally, we may soon document Untis's HTML.

# Licensing
You can license the files in this repository under the terms of the
[CC BY-ND license](https://creativecommons.org/licenses/by-nd/4.0/).

# 0 An overview
There are many different DSBMobile API implementations and most of
them…are the same. This is because of pydsb (1), which can be
considered the reference implementation of the Android API. But there
are still four different APIs known to us, and two more with only one
implementation each.

## The APIs
* Mobile API (Section 1)
* Android API (Section 2)
* Web API (Section 2.1)
* iOS API (Section 3)

## The implementations
This is an incomplete list of DSBMobile API implementations:

### Mobile API

| Implementation                                                             | Language   | Data types                    | Extra features                                          | Bundle ID                   | App Version        | OS Version         |
|----------------------------------------------------------------------------|------------|-------------------------------|---------------------------------------------------------|-----------------------------|--------------------|--------------------|
| [dsbuntis ≥3](https://github.com/Ampless/dsbuntis)                         | Dart       | Plans (others with a raw API) | Sorting, Searching and DSB-based Previews               | de.heinekingmedia.dsbmobile | 36 (configurable)  | 30 (configurable)  |
| [dsb-api](https://github.com/CinePlays/dsb-api)                            | Dart       | Plans, News, Documents        | Violates Ampless Copyleft (no notice about copied code) | de.heinekingmedia.dsbmobile | 36                 | 30                 |
| [pydsb (1) ≥2.2](https://github.com/sn0wmanmj/pydsb)                       | Python     | Plans, News, Postings         | DSB-based Previews                                      | de.heinekingmedia.dsbmobile | 35                 | 22                 |
| [dsbmobile.js](https://github.com/Tch1b0/dsbmobile.js)                     | TypeScript | Plans, News, Documents        | ?                                                       | ? (probably empty)          | ? (probably empty) | ? (probably empty) |
| [vertretungsplan.io](https://codeberg.org/vertretungsplan/integration-dsb) | TypeScript | Plans, News, Documents        |                                                         | (empty)                     | (empty)            | (empty)            |
| [DSBDirect](https://notabug.org/fynngodau/DSBDirect)                       | Java       | Plans, News, Documents        |                                                         | (empty)                     | (empty)            | (empty)            |

### Android API

| Implementation                                                                  | Language   | Data types            | Extra features & drawbacks  | Bundle ID                               | Device   | App Version | OS Version | Simulated Language |
|---------------------------------------------------------------------------------|------------|-----------------------|-----------------------------|-----------------------------------------|----------|-------------|------------|--------------------|
| [dsbuntis <3](https://github.com/Ampless/dsbuntis)                              | Dart       | Plans                 | Sorting and Searching       | de.heinekingmedia.dsbmobile             | SM-G950F | 2.5.9       | 29 10.0    | de (configurable)  |
| [pydsb (1) 2.0-2.1](https://github.com/sn0wmanmj/pydsb)                         | Python     | Plans, News, Postings | DSB-based previews          | de.heinekingmedia.dsbmobile             | Pixel 3  | 2.5.9       | 27 8.1.0   | de                 |
| [OpenDSBMobile](https://github.com/KaiJan57/OpenDSBmobile)                      | Java       | Plans, News, Postings | reimplementation of the app | de.heinekingmedia.dsbmobile             | (empty)  | 2.5.9       | (empty)    | your os language   |
| [DSBMobile-API](https://github.com/Sematre/DSBmobile-API)                       | Java       | Plans, News           | User-Agent spoofing         | de.heinekingmedia.dsbmobile             | Nexus 4  | 2.5.9       | 27 8.1.0   | de                 |
| [DSBApi](https://github.com/nerrixDE/DSBApi)                                    | Python     | Plans                 |                             | de.heinekingmedia.dsbmobile             | SM-G930F | 2.5.9       | 27 8.1.0   | de                 |
| [DSBAPI](https://github.com/TheNoim/DSBAPI)                                     | JavaScript | raw json              | User-Agent spoofing         | de.digitales-schwarzes-brett.dsblight   | iPhone   | 2.5.6       | 13.2.2     | en-DE              |
| [dsb-go](https://github.com/irgendwr/dsb-go)                                    | Go         | Plans, News           | User-Agent "dsb-go"         | de.heinekingmedia.dsbmobile             | Nexus 4  | 2.5.9       | 27 8.1.0   | de                 |
| [Vertretungsplangak\_Bot](https://github.com/MakerStuff/Vertretungsplangak_Bot) | Python     | ?                     | no parsing                  | de.heinekingmedia.dsbmobile             | SM-G935F | 2.5.9       | 28 9       | de                 |
| [dsbmobile-php-api](https://github.com/irgendwr/dsbmobile-php-api)              | PHP        | Plans, News           | faked Referer header        | de.heinekingmedia.inhouse.dsbmobile.web | WebApp   | 2.3         | (empty)    | de                 |
| [dsbmobile\_api](https://github.com/spnda/dsbmobile_api)                        | Dart       | ?                     | ?                           | de.heinekingmedia.dsbmobile             | Nexus 4  | 2.5.9       | 27 8.1.0   | de (configurable)  |

### Web API

#### [Vertretungsplangak\_Bot (2)](https://github.com/MakerStuff/Vertretungsplangak_Bot)
* Language: Python
* Drawbacks: no parsing, constant Date and LastUpdate
* Supported requests: 1 (GetData)
* Simulated Bundle ID: de.heinekingmedia.inhouse.dsbmobile.web
* Simulated Device: WebApp
* Simulated Version: 2.3
* Simulated OS Version: Mozilla/5.0 (X11; Linux x86\_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.70 Safari/537.36
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

# 1 The Mobile API
This is the simplest known API of DSBMobile. It **does** require the use of
sessions/tokens. Like the other APIs it uses HTTPS for what could be referred to
as Layer 4 or 5 in the OSI Model. All requests are `GET` requests.

## Requests
There are two requests needed for getting substitution plans:
* Auth
* Timetables

### Auth
Auth is sent to `https://mobileapi.dsbcontrol.de/authid`
with the arguments appended to it.

The server then responds with a new session/token in double quotes.
(or `""` if the credentials are invalid)

#### Arguments

The arguments are `?bundleid=BUNDLE&appversion=VER&osversion=OSVER&pushid&user=USERNAME&password=PASSWORD`.

`USERNAME` and `PASSWORD` are kinda obvious.

`BUNDLE` is the bundle id, usually `de.heinekingmedia.dsbmobile`.

`VER` is the DSBMobile app version.

`OSVER` is the OS version, for example on Android the API Version.

### Timetables

Timetables are gotten from
`https://mobileapi.dsbcontrol.de/dsbtimetables?authid=TOKEN`, where `TOKEN`
is the token from Auth. The server then responds with a JSON array of entries
that are reasonably complex. Each one represents a timetable/substitution plan
and looks like this:

```json
{
  "Id": "ID",
  "Date": "DATE",
  "Title": "TITLE",
  "Detail": "",
  "Tags": "",
  "ConType": 2,
  "Prio": 0,
  "Index": 0,
  "Childs": CHILDS,
  "Preview": ""
}
```

`ID` is a (supposedly random) UUID.

`DATE` is a date and time in the format `%d.%m.%Y %H:%M`.
(e.g. `13.12.2016 18:00`)

As far as we currently know, the `Preview`, `Tags` and `Detail` are actually
always empty strings, the `Index` and `Prio`rity always 0, and `ConType` is
always 2.
<!--TODO: check this using aggregamus-->

`CHILDS` is another JSON list of very similar objects that represent "pages",
a feature discovered very late
([1.5 years into Amplissimus](https://github.com/Ampless/dsbuntis/issues/10)),
since most schools tend to not use multiple ones. Every page looks like this:

```json
{
  "Id": "TABLE_ID",
  "Date": "DATE",
  "Title": "TITLE",
  "Detail": "DETAIL",
  "Tags": "",
  "ConType": CONTYPE,
  "Prio": 0,
  "Index": INDEX,
  "Childs": [],
  "Preview": "PREVIEW"
}
```

`TABLE` is the `ID` of the table.

`ID` is some (small) integer like `123`, `371` or `820`.

`DATE` is another date and time in the format `%d.%m.%Y %H:%M`.

In the two real-world schools tested, `TITLE` is always `subst_001`, but the
public/test account shows, that it might not be.

`DETAIL` is the full URL pointing to the HTML of the plan in question.
(e.g. `https://light.dsbcontrol.de/DSBlightWebsite/Data/13ccccbb-e6a8-466a-addc-00bba830c6cf/4f301632-7422-4186-96a2-2b7911f54bc5/Vertretungen-Woche.htm`)

`CONTYPE` is another integer, usually 6, sometimes 4.

`INDEX` is yet another integer that may (!) be intended for sorting the pages.

`PREVIEW` is the path to the preview PNG hosted on the preview endpoint (usually `https://light.dsbcontrol.de/DSBlightWebsite/Data/`).
(e.g. `13ccccbb-e6a8-466a-addc-00bba830c6cf/4f301632-7422-4186-96a2-2b7911f54bc5/preview.png`)

As far as we currently know, the `Tags` is actually always an empty string,
the `Prio`rity always 0, and `Childs` always an empty list.
<!--TODO: check this using aggregamus-->

Parsing the plans from the HTML depends on the format of them, which
usually is like Untis always does HTML. But the HTML format is not
documented here, because it does not depend on the DSB API used.

# 2 The Android API

This was the most-used API of DSBMobile. Most implementations used it
It does **not** require any kind of session. Like the other APIs it uses HTTPS
for what could be referred to as Layer 4 or 5 in the OSI Model.

## Requests

There are seven known requests:

* DataUnknown (0)
* GetData (1)
* MailType (2)
* FeedbackType (3)
* SubjectsType (4)
* ErrorType (5)
* PushSettings (6)

But only one of them, GetData (1), is actually used.

## GetData

GetData is sent as an HTTP POST request to
`https://app.dsbcontrol.de/JsonHandler.ashx/GetData`.

### Request
The body of the request looks like this:
```js
{"req": {"Data": "DATA", "DataType": 1}}
```

The body of the response looks like this:
```js
{"d": "DATA"}
```

DATA is the actual data compressed with GZIP and encoded as Base64.
The actual data is a string, which for the request looks like this:

```js
{
    "UserId": "USERNAME",
    "UserPw": "PASSWORD",
    "AppVersion": "APP_VERSION",
    "Language": "LANGUAGE",
    "OsVersion": "OS_VERSION",
    "AppId": "APP_ID",
    "Device": "DEVICE_NAME",
    "BundleId": "BUNDLE_ID",
    "Date": "DATETIME",
    "LastUpdate": "DATETIME"
}
```

`USERNAME` and `PASSWORD` are obvious.

`APP_VERSION` is the version of the DSBMobile app you are running.
(or pretend to)

`LANGUAGE` should usually be `de`, because DSBMobile is used only in
Germany and only in German, but some implementations allow for other
languages.

`OS_VERSION` should be the Android API Level and Android
Version joined by a single space. Of course most implementations send
a static string for a bunch of reasons.

What `APP_ID` is supposed to be is not really clear, most implementations just
generate a random v4 UUID, but probably it is supposed to be unique to every
instance of the app and not to every request.

`DEVICE_NAME` is supposed to be the model of the device running the app,
most implementations just use some recent Samsung Galaxy phones.

`BUNDLE_ID` is the bundle id of the app, with most implementations pretending
to be `de.heinekingmedia.dsbmobile`.

`DATETIME` is the current date and time as printed by ECMAScript,
which is ISO 8601 with a Z at the end.

### Response

For the response the actual data is a really big JSON, which we will
not care to fully document here. But for getting the plans this is
enough:

```dart
if (actualData['Resultcode'] != 0)
  throw Error(actualData['ResultStatusInfo']);

for (var p in actualData['ResultMenuItems'][0]['Childs'][0]
                        ['Root']['Childs']) {
  var url = p['Childs'][0]['Detail'];
  var title = p['Title'];
  outputPlan(title, url);
}
```

Parsing the plans from the HTML depends on the format of them, which
usually is like Untis always does HTML. But the HTML format is not
documented here, because it does not depend on the DSB API used.

## 2.1 The Web API

This is the API used mainly by the DSBMobile Webapp. It **does**
require a session kept in HTTP cookies. This API's requests are quite
horrible and officially implemented in hundreds of lines of weirdly
obfuscated JavaScript. Its similarities to the Android API, however,
are quite obvious.

### Login

Before you can do anything else, you first have to login.

<!-- vim: set wrap! : -->
