## SubmitBlockTrade

**Category:** User<br />
**Permissions:** Operator<br />
**Call Type:** Asynchronous

Reports an off-market trade has occurred between two parties.

Once reported, you can follow the trade using **GetAccountTrades** or **GetTradesHistory.**

###Request

```json
{
    "omsId": 0,
    "accountId":0,
    "counterPartyAccountName": "test",
    "counterPartyAccountId": 0,
    "counterPartyId": "",
    "clientOrderId":0,
    "quantity":0.0,
    "limitPrice":0.0,
    "instrumentId":0,
    "timestamp":0,
    "side":0,
    "lockedIn":false
}
```

| Key            | Value                                                        |
| -------------- | ------------------------------------------------------------ |
| omsId          | **integer.** The ID of the Order Management System where the block trade is to be reported. |
| accountId      | **integer.** The ID of the account making the report of the block trade. |
| counterPartyAccountName | **string.** The name of the account of the other party in the off-market trade. |
| counterPartyAccountId | **integer.** The ID of the account of the other party in the off-market trade. |
| counterPartyId | **integer.** The ID of the other party in the off-market trade. |
| clientOrderId  | **long integer.** The client-provided ID for the trade (much like a client-provided purchase order number). |
| quantity       | **real.** The quantity on the instrument that was traded.    |
| limitPrice     | **real.** The price at which to execute the block trade.     |
| instrumentId   | **integer.** The ID of the instrument being traded.          |
| timestamp      | **long integer.** The time that the block trade was submitted, in POSIX format.               |
| side           | **integer.** A number that represents the side of the transaction associated with accountId. One of:<br />0 Buy<br />1 Sell<br />2 Short<br />3 Unknown (error condition) |
| lockedIn       | **Boolean.** *True* if both parties to the block trade agree that one of the parties will report the trade for both sides. Otherwise, *false*. |

### Response

```json
{
    "status":"Accepted",
    "errormsg":"",
    "OrderId": 22
}
```

| Key      | Value                                                        |
| -------- | ------------------------------------------------------------ |
| status   | **string.** If the order is accepted by the system, it returns "Accepted," if not, it returns "Rejected." One of:<br />Accepted<br />Rejected |
| errormsg | **string.** Any error message that the server returns.       |
| OrderId  | **long integer.** The ID assigned to the order by the server. This allows you to track the order later. |


