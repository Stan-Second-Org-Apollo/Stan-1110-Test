# User Signed In

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "User Signed In",
    "user": {
        "country": "<country>",
        "loginStatus": "<loginStatus>",
        "registrationStatus": "<registrationStatus>",
        "system": "<system>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|country|string|The country associated with this user's profile.|USA, Canada|||||||
|loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||
|registrationStatus|string|Describes the registration state of the user \(independent of sign-in state\)|registered|||||||
|system|string|Describes the system that the user is logged into.  \(rarely used\). |admin, shop, member|||||||
