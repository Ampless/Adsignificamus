# Chapter 1 - The Mobile API
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

The arguments are
`?bundleid=BUNDLE&appversion=VER&osversion=OSVER&pushid&user=ID&password=PASS`.

`BUNDLE` is the bundle id, usually `de.heinekingmedia.dsbmobile`.

`VER` is the app version, current implementations pretend to be `35`.

`OSVER` is the OS version, current implementations pretend to be on `22`.

`ID` and `PASS` are kinda obvious.

### Timetables
Timetables are gotten from
`https://mobileapi.dsbcontrol.de/dsbtimetables?authid=TOKEN`, where `TOKEN`
is the token from Auth. The server then responds with a JSON array of entries
that are reasonably complex, but if you just want the URLs to the substitutions:

```dart
for (var plan in json) {
        downloadAndOutputHtmlPlan(plan['Childs'][0]['Detail']);
}
```

Parsing the plans from the HTML depends on the format of them, which
usually is like Untis always does HTML. But the HTML format is not
documented here, because it does not necessarily depend on the DSB API
used.
