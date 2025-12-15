# Adsignificamus

These are some docs for heinekingmedia's DSBMobile APIs. Additionally, we will
soon document Untis's HTML.

# Licensing

You can license the files in this repository under the terms of the
[CC BY-ND license](https://creativecommons.org/licenses/by-nd/4.0/).

# 0 An overview

There are many different DSBMobile API implementations and most of them…are the
same. This is because of pydsb (1), which can be considered the reference
implementation of the Android API. But there are still four different APIs known
to us, and two more with only one implementation each.

## The APIs

- [Mobile API (Section 1)](#1-the-mobile-api)
- [Android API (Section 2)](#2-the-android-api)
- [Web API (Section 2.1)](#21-the-web-api)
- iOS API (Section 3, TBD)

## The implementations

This is an incomplete list of DSBMobile API implementations:

<!--TODO: split between DSB and Untis implementations-->

### Mobile API

| Implementation                                                             | Language   | Data types               | Extra features                         | Bundle ID                   | App Version        | OS Version         |
| -------------------------------------------------------------------------- | ---------- | ------------------------ | -------------------------------------- | --------------------------- | ------------------ | ------------------ |
| [dsbuntis ≥3](https://github.com/Ampless/dsbuntis)                         | Dart       | Plans, News, Documents\* | Sorting, Searching, DSB-based Previews | de.heinekingmedia.dsbmobile | 36 (configurable)  | 30 (configurable)  |
| [dsb-api](https://github.com/CinePlays/dsb-api)                            | Dart       | Plans, News, Documents   | Probably violates Ampless Copyleft     | de.heinekingmedia.dsbmobile | 36                 | 30                 |
| [pydsb (1) ≥2.2](https://github.com/sn0wmanmj/pydsb)                       | Python     | Plans, News, Documents   | DSB-based Previews                     | de.heinekingmedia.dsbmobile | 35                 | 22                 |
| [dsbmobile.js](https://github.com/Tch1b0/dsbmobile.js)                     | TypeScript | Plans, News, Documents   | ?                                      | ? (probably empty)          | ? (probably empty) | ? (probably empty) |
| [vertretungsplan.io](https://codeberg.org/vertretungsplan/integration-dsb) | TypeScript | Plans, News, Documents   |                                        | (empty)                     | (empty)            | (empty)            |
| [DSBDirect](https://notabug.org/fynngodau/DSBDirect)                       | Java       | Plans, News, Documents   |                                        | (empty)                     | (empty)            | (empty)            |

\* dsbuntis supports every other data type that might exist through a very
low-level API.

### Android API

<!--TODO: check whether postings are the same as documents-->

| Implementation                                                                  | Language   | Data types            | Extra features & drawbacks  | Bundle ID                               | Device   | App Version | OS Version | Language          |
| ------------------------------------------------------------------------------- | ---------- | --------------------- | --------------------------- | --------------------------------------- | -------- | ----------- | ---------- | ----------------- |
| [dsbuntis <3](https://github.com/Ampless/dsbuntis)                              | Dart       | Plans                 | Sorting and Searching       | de.heinekingmedia.dsbmobile             | SM-G950F | 2.5.9       | 29 10.0    | de (configurable) |
| [pydsb (1) 2.0-2.1](https://github.com/sn0wmanmj/pydsb)                         | Python     | Plans, News, Postings | DSB-based previews          | de.heinekingmedia.dsbmobile             | Pixel 3  | 2.5.9       | 27 8.1.0   | de                |
| [OpenDSBMobile](https://github.com/KaiJan57/OpenDSBmobile)                      | Java       | Plans, News, Postings | reimplementation of the app | de.heinekingmedia.dsbmobile             | (empty)  | 2.5.9       | (empty)    | your os language  |
| [DSBMobile-API](https://github.com/Sematre/DSBmobile-API)                       | Java       | Plans, News           | User-Agent spoofing         | de.heinekingmedia.dsbmobile             | Nexus 4  | 2.5.9       | 27 8.1.0   | de                |
| [DSBApi](https://github.com/nerrixDE/DSBApi)                                    | Python     | Plans                 |                             | de.heinekingmedia.dsbmobile             | SM-G930F | 2.5.9       | 27 8.1.0   | de                |
| [DSBAPI](https://github.com/TheNoim/DSBAPI)                                     | JavaScript | raw json              | User-Agent spoofing         | de.digitales-schwarzes-brett.dsblight   | iPhone   | 2.5.6       | 13.2.2     | en-DE             |
| [dsb-go](https://github.com/irgendwr/dsb-go)                                    | Go         | Plans, News           | User-Agent "dsb-go"         | de.heinekingmedia.dsbmobile             | Nexus 4  | 2.5.9       | 27 8.1.0   | de                |
| [Vertretungsplangak\_Bot](https://github.com/MakerStuff/Vertretungsplangak_Bot) | Python     | ?                     | no parsing                  | de.heinekingmedia.dsbmobile             | SM-G935F | 2.5.9       | 28 9       | de                |
| [dsbmobile-php-api](https://github.com/irgendwr/dsbmobile-php-api)              | PHP        | Plans, News           | faked Referer header        | de.heinekingmedia.inhouse.dsbmobile.web | WebApp   | 2.3         | (empty)    | de                |
| [dsbmobile\_api](https://github.com/spnda/dsbmobile_api)                        | Dart       | ?                     | ?                           | de.heinekingmedia.dsbmobile             | Nexus 4  | 2.5.9       | 27 8.1.0   | de (configurable) |

### Web API

| Implementation                                                                      | Language | Drawbacks                                | Supported requests | Bundle ID                               | Device | Version | OS Version                                                                                                | Language |
| ----------------------------------------------------------------------------------- | -------- | ---------------------------------------- | ------------------ | --------------------------------------- | ------ | ------- | --------------------------------------------------------------------------------------------------------- | -------- |
| [Vertretungsplangak\_Bot (2)](https://github.com/MakerStuff/Vertretungsplangak_Bot) | Python   | no parsing, constant Date and LastUpdate | 1 (GetData)        | de.heinekingmedia.inhouse.dsbmobile.web | WebApp | 2.3     | Mozilla/5.0 (X11; Linux x86\_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.70 Safari/537.36 | de       |

### iOS API

| Implementation                                                    | Language   | Data types            | Extra features     |
| ----------------------------------------------------------------- | ---------- | --------------------- | ------------------ |
| [pydsb (1) 1.x](https://github.com/sn0wmanmj/pydsb)               | Python     | Plans, News, Postings | DSB-based previews |
| [pydsb (2)](https://github.com/ScholliYT/pydsb)                   | Python     | Plans, News           |                    |
| [DSBMobileBot](https://github.com/ScholliYT/DSBMobileBot)         | Python     | Plans                 |                    |
| [myplan](https://github.com/jrheiner/myplan)                      | Java       | Plans                 | a custom app       |
| [DSB - Abrage](https://forum.iobroker.net/topic/19140/dsb-abrage) | JavaScript | Plans, News           |                    |
| [Untitled](https://pastebin.com/ds0AjK6T)                         | Python     | Plans                 |                    |

### Other

| Implementation                               | Language     | API                                                                      | Data types                       | Drawbacks  |
| -------------------------------------------- | ------------ | ------------------------------------------------------------------------ | -------------------------------- | ---------- |
| [DSBot](https://github.com/sargantana/DSBot) | Shell (wget) | Unknown (looks like Web at first glance, but is significantly different) | plans (not 100% sure about that) | no parsing |

### Other interesting URLs

These are some resources for learning things, you might need while building DSB
API implementations:

- https://pastebin.com/7XZD38V5
- https://light.dsbcontrol.de/DSBlightWebsite/(S(kvgpcwcoqorwq3xxgbx42u2b))/Homepage/IFrame.aspx

# 1 The Mobile API

> ![NOTE]
> The Mobile API is also extensively documented on
> [the DSBDirect wiki](https://notabug.org/fynngodau/DSBDirect/wiki/mobileapi.dsbcontrol.de),
> which is unavailable and not archived as of December 2025.

This is the simplest known API of DSBMobile. It **does** require the use of
sessions/tokens. Like the other APIs it uses HTTPS for what could be referred to
as Layer 4 or 5 in the OSI Model. All requests are `GET` requests.

## Requests

### Auth

Auth is sent to `https://mobileapi.dsbcontrol.de/authid` with the arguments
appended to it.

#### Arguments

The arguments are
`?bundleid=BUNDLE&appversion=VER&osversion=OSVER&pushid&user=USERNAME&password=PASSWORD`.

`USERNAME` and `PASSWORD` are kinda obvious.

`BUNDLE` is the bundle id, usually `de.heinekingmedia.dsbmobile`.

`VER` is the DSBMobile app version.

`OSVER` is the OS version, for example on Android the API Version.

<!--TODO: pushid-->

#### Response

The server then responds with a new session/token in double quotes. (or `""` if
the credentials are invalid)

The tokens are UUIDs that are always the same for the same `USERNAME` (and
`PASSWORD`), which means that (a) they can be cached indefinitely and (b) could
be generated on the client side somehow, if it was known, which exact algorithms
are used.

### Plans, News, Documents, ...

All other endpoints use a JSON-based format and very similar requests, too.

Plans are gotten from
`https://mobileapi.dsbcontrol.de/dsbtimetables?authid=TOKEN`, News from
`https://mobileapi.dsbcontrol.de/newstab?authid=TOKEN`, and Documents from
`https://mobileapi.dsbcontrol.de/dsbdocuments?authid=TOKEN`, where `TOKEN` is
always the token from Auth.

#### Response

From all of these, JSON lists are returned. They contain `Item`s, each of which
might represent a Plan, Document, News item, etc. `Item`s look like this:

```ts
{
  // a (supposedly random) UUID
  "Id": string,

  // `%d.%m.%Y %H:%M` (e.g. `13.12.2016 18:00`)
  // **might** have been displayed as "Last Updated" in old DSBMobile versions
  "Date": string,

  // as displayed in the DSBMobile app
  "Title": string,

  // payload (see below)
  "Detail": string,

  // usually empty
  "Tags": string,

  "ConType": number,

  // usually 0
  "Prio": number,

  // usually 0, might be another number (might be useful for sorting?)
  "Index": number,

  // payload (see below)
  "Childs": object[],

  // the path of the preview PNG hosted on the preview endpoint (usually
  // <https://light.dsbcontrol.de/DSBlightWebsite/Data/>)
  "Preview": string,
}
```

<!--TODO: check-->

`ConType` determines, how and where data is encoded:

| `ConType` | Where?   | What?                                 |
| --------- | -------- | ------------------------------------- |
| `2`       | `Childs` | child `Item`s, like pages of the plan |
| `4`       | `Detail` | link to an HTML web page              |
| `5`       | `Detail` | string of text                        |
| `6`       | `Detail` | link to a PNG/GIF image               |

If it doesn't contain data, `Childs` is an empty list (`[]`), `Detail` an empty
string (`""`).

##### Example

The list of timetables might look something like this
(`accemus -T 187801 public`):

```json
[
  {
    "Id": "67b3035c-51ff-4106-a2ec-b50f8680e0c4",
    "Date": "31.03.2020 17:33",
    "Title": "Vertretungen-heute",
    "Detail": "",
    "Tags": "",
    "ConType": 2,
    "Prio": 0,
    "Index": 0,
    "Childs": [
      {
        "Id": "67b3035c-51ff-4106-a2ec-b50f8680e0c4_76",
        "Date": "31.03.2020 17:33",
        "Title": "Vertretungen-heute",
        "Detail": "https://light.dsbcontrol.de/DSBlightWebsite/Data/13ccccbb-e6a8-466a-addc-00bba830c6cf/67b3035c-51ff-4106-a2ec-b50f8680e0c4/Vertretungen-heute.htm",
        "Tags": "",
        "ConType": 6,
        "Prio": 0,
        "Index": 76,
        "Childs": [],
        "Preview": "13ccccbb-e6a8-466a-addc-00bba830c6cf/67b3035c-51ff-4106-a2ec-b50f8680e0c4/preview.png"
      }
    ],
    "Preview": ""
  },
  {
    "Id": "4f301632-7422-4186-96a2-2b7911f54bc5",
    "Date": "31.03.2020 17:34",
    "Title": "Vertretungen-Woche",
    "Detail": "",
    "Tags": "",
    "ConType": 2,
    "Prio": 0,
    "Index": 0,
    "Childs": [
      {
        "Id": "4f301632-7422-4186-96a2-2b7911f54bc5_76",
        "Date": "31.03.2020 17:34",
        "Title": "Vertretungen-Woche",
        "Detail": "https://light.dsbcontrol.de/DSBlightWebsite/Data/13ccccbb-e6a8-466a-addc-00bba830c6cf/4f301632-7422-4186-96a2-2b7911f54bc5/Vertretungen-Woche.htm",
        "Tags": "",
        "ConType": 6,
        "Prio": 0,
        "Index": 76,
        "Childs": [],
        "Preview": "13ccccbb-e6a8-466a-addc-00bba830c6cf/4f301632-7422-4186-96a2-2b7911f54bc5/preview.png"
      }
    ],
    "Preview": ""
  }
]
```

# 2 The Android API

This was the most-used API of DSBMobile. Most implementations used it until it
was shut down in early 2021. It does **not** require any kind of session. Like
the other APIs it uses HTTPS for what could be referred to as Layer 4 or 5 in
the OSI Model.

## Requests

There are seven known requests:

- DataUnknown (0)
- GetData (1)
- MailType (2)
- FeedbackType (3)
- SubjectsType (4)
- ErrorType (5)
- PushSettings (6)

But only one of them, GetData (1), is actually used.

## GetData

GetData is sent as an HTTP POST request to
`https://app.dsbcontrol.de/JsonHandler.ashx/GetData`.

### Request

The body of the request looks like this:

```js
{"req": {"Data": "DATA", "DataType": 1}}
```

DATA is the actual data compressed with GZIP and encoded as Base64. The actual
data is a JSON-encoded string of the following schema:

```ts
{
  // username
  "UserId": string,

  // password
  "UserPw": string,

  // the version of the DSBMobile app you're pretending to run
  "AppVersion": string,

  // usually "de", some implementation allow for other languages
  "Language": string,

  // Android API Level + " " + Android Version
  // usually a static string (e.g. "29 10.0")
  "OsVersion": string,

  // original purpose unclear, probably a unique UUID for each DSBMobile install
  // most implementations generate a random UUIDv4 for each request
  "AppId": string,

  // model of the device running the app
  // usually a static string (e.g. "SM-G950F")
  "Device": string,

  // the bundle id of the app
  // most implementations pretend to be "de.heinekingmedia.dsbmobile"
  "BundleId": string,

  // the current datetime in JS Date.toISOString format, i.e. ISO 8601 with "Z"
  // at the end to indicate UTC timezone
  "Date": string,
  // the same as Date
  "LastUpdate": string,
}
```

### Response

The body of the response looks like this:

```js
{"d": "DATA"}
```

For the response the actual data is a really big JSON, which we will not care to
fully document here. But for getting the plans this is enough:

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

Parsing the plans from the HTML depends on the format of them, which usually is
like Untis always does HTML. But the HTML format is not documented here, because
it does not depend on the DSB API used.

## 2.1 The Web API

This is the API used mainly by the DSBMobile Webapp. It **does** require a
session kept in HTTP cookies. This API's requests are quite horrible and
officially implemented in hundreds of lines of weirdly obfuscated JavaScript.
Its similarities to the Android API, however, are quite obvious.

<!-- vim: set wrap! : -->
