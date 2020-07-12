# Chapter 1 - The Android API
This is the most-used API of DSBMobile. All official implementations
seem to point towards using it and we do not know of any, except the
Web, using anything else. It does **not** need any kind of session.
Like the other APIs it uses HTTPS for what could be referred to as
Layer 4 or 5 in the OSI Model.

# Requests
Every request is sent as an HTTP POST. There are seven known requests:
* DataUnknown (0)
* GetData (1)
* MailType (2)
* FeedbackType (3)
* SubjectsType (4)
* ErrorType (5)
* PushSettings (6)
Only one of them, GetData (1), is ever used.
