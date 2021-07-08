# Order Placed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Order Placed",
    "cart": {
        "cartID": "<cartID>"
    },
    "transaction": {
        "item": [
            {
                "altPersonPickUp": "<altPersonPickUp>",
                "pickUpTextNotifications": "<pickUpTextNotifications>",
                "price": {
                    "basePrice": "<basePrice>",
                    "markdownPrice": "<markdownPrice>",
                    "sellingPrice": "<sellingPrice>"
                },
                "productInfo": {
                    "isGiftWrapped": "<isGiftWrapped>",
                    "productID": "<productID>",
                    "webExclusive": "<webExclusive>"
                },
                "quantity": "<quantity>",
                "voucherDiscount": {
                    "orderLevelDiscountAmount": "<orderLevelDiscountAmount>",
                    "orderLevelDiscountCode": "<orderLevelDiscountCode>",
                    "productLevelDiscountAmount": "<productLevelDiscountAmount>"
                }
            }
        ],
        "payment": [
            {
                "loyaltyPointsAmount": "<loyaltyPointsAmount>",
                "paymentAmount": "<paymentAmount>"
            }
        ],
        "productIDList": "<productIDList>",
        "profile": {
            "address": {
                "country": "<country>",
                "postalCode": "<postalCode>",
                "stateProvince": "<stateProvince>"
            }
        },
        "purchaseID": "<purchaseID>",
        "skuList": "<skuList>",
        "total": {
            "currency": "<currency>",
            "numPayments": "<numPayments>",
            "revenue": "<revenue>"
        },
        "transactionID": "<transactionID>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|altPersonPickUp|integer|When a user has put in the information of an alternate pick up person during the checkout process.||||||||
|basePrice|string|String representation of MSRP of a product. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|cartID|string|Back-end identifier for a shopping cart|12345, 435678, 34567, XCV456, XCV876|||||||
|country|string|Indicates the country of the billing address. ISO 3166 \(alpha-2\) Uppercase.|US, CA, FR, UK|^[A-Z]{2}$||||||
|currency|string|Currency of the transaction. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|isGiftWrapped|boolean|At order confirmaton, set a to true for every product that is gift wrapped.||||||||
|loyaltyPointsAmount|integer|Number of loyalty points |100, 101, 1000||||0|||
|markdownPrice|string|String representation of the price offered. Often called 'hard mark' price. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|numPayments|integer|Collects the number of payment methods used for an order at order confirmaton||||||||
|orderLevelDiscountAmount|string|String representation of an order level discount applied to an item in a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5, 20, 10.22, 19.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|orderLevelDiscountCode|string|Order Level Discount code applied at the item level of a transaction. |FRIENDSANDFAMILY20, EASTER10|||||||
|paymentAmount|string|String representation of the payment amount. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|pickUpTextNotifications|integer|The count of times a user has selected to receive text notifications during the checkout process.||||||||
|postalCode|string|The mailing zip or postal code associated with the billing address. |53533, 30381, M1R 0E9, M3C 0C1|||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|productIDList|string|A delimited list of product IDs in the transaction.|1234\|7878\|9039, abc12\|deh213, abc12|||||||
|productLevelDiscountAmount|string|String representation of product level discount for a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5, 20, 10.22, 19.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|purchaseID|string|Unique identifier of the purchase. Max Length 20. Used as Unique ID of the purchase or deduplication.|ABC-132456789, DEF-132456789, 0987654567|^[a-zA-Z0-9]{6,20}$|6|20||||
|quantity|integer|Integer number of products being acted upon \(added to a cart, removed from wishlist, purchased, reserved\)|1, 2, 3, 4, 5||||1|||
|revenue|string|The total revenue for a transaction. Does not include tax or shipping. |125.05, 432.21, 90.22, 12.05|^[0-9]*(\.[0-9]{1,2})?$||||||
|sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|skuList|string| A delimited list of skus in the transaction.|sku123\|sku465, 67890\|87576\|74674, 87654|||||||
|stateProvince|string|The mailing state or province associated with billing address. |WI, GA, NB, ON|||||||
|transactionID|string|Unique identifier of the transaction. Max Length 100. Used as a key for upload of post transaction data. |123e4567-e89b-12d3-a456-426614174000|^[a-zA-Z0-9]{6,100}$|6|100||||
|webExclusive|boolean|Captures whether or not the product is sold on website\/app only.||||||||
