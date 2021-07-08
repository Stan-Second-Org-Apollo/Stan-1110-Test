# Event Booking Completed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Event Booking Completed",
    "booking": {
        "ticketList": [
            {
                "event": {
                    "eventName": "<eventName>",
                    "fakeProductId": "<fakeProductId>"
                }
            }
        ],
        "total": {
            "currency": "<currency>"
        }
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|currency|string|Currency of the payment for the booking. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|eventName|string|The friendly name of the event.|Max your 401K, Structured JavaScript, Mid Day Yoga, Frosty 5K Fun Run, Whiskey Wednesday|||||||
|fakeProductId|string|Helper node used by AA Product String Builder to set product to location. This field gets a static value of "event".  With updates to the AA PS extension, this will soon go away.|event|event||||||
