# Chapter 1 - The Android API
This is the most-used API of DSBMobile. All official implementations
seem to point towards using it and we do not know of any, except the
Web, using anything else. It does **not** need any kind of session.
Like the other APIs it uses HTTPS for what could be referred to as
Layer 4 or 5 in the OSI Model.

## Requests
There are seven known requests:
* DataUnknown (0)
* GetData (1)
* MailType (2)
* FeedbackType (3)
* SubjectsType (4)
* ErrorType (5)
* PushSettings (6)

But only one of them, GetData (1), is ever used.

## GetData
GetData is sent over an HTTP POST request to
`https://app.dsbcontrol.de/JsonHandler.ashx/GetData`.

The body of the request looks like this:
```js
{ "req": { "Data": "DATA", "DataType": 1 } }
```

The body of the response looks like this:
```js
{ "d": "DATA" }
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

USERNAME and PASSWORD are obvious, APP\_VERSION is the version of the
DSBMobile app you are running (or the one you like to simulate),
LANGUAGE should usually be de, because DSBMobile is used only in
Germany and only in German, but some implementations allow for other
languages. OS\_VERSION should be the Android API Level and Android
Version joined by a single space. Of course most implementations send
a static string for privacy reasons. What APP\_ID is supposed to be
is not really clear, most implementations just generate a random v4
UUID, but probably it is supposed to be unique to every instance of
the app and not to every request. DEVICE\_NAME is supposed to be the
name of the device running the app, most implementations just use some
recent Samsung Galaxy phones for privacy reasons. BUNDLE\_ID is the
bundle id of the app, with most implementations pretending to be
`de.heinekingmedia.dsbmobile`. DATETIME is the current date and time
as printed by ECMAScript, which is ISO 8601 with a Z at the end.

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
documented here, because it does necessarily not depend on the DSB API
used.
