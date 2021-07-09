# Event Booking Started

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Event Booking Started",
    "booking": {
        "ticketList": [
            {
                "event": {
                    "fakeProductId": "<fakeProductId>",
                    "startDate": "<startDate>",
                    "startTime": "<startTime>"
                }
            }
        ]
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|fakeProductId|string|Helper node used by AA Product String Builder to set product to location. This field gets a static value of "event".  With updates to the AA PS extension, this will soon go away.|event|event||||||
|startDate|string|Start date. ISO 8601 form \(YYYY-MM-DD\). Jan 1, 2019 is 2019-01-01|2001-12-22, 2011-01-01|^([0-9]{4})-(1[0-2]|0[1-9])-(3[01]|0[1-9]|[12][0-9])$||||||
|startTime|string|Start Time. 24H format zero padded.|10:30, 14:45, 23:59, 07:00|^[0-2][0-9]:[0-5][0-9] ||||||
