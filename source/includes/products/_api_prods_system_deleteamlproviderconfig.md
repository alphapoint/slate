## DeleteAmlProviderConfig

**Category:** System<br />**Permissions:** Operator<br />**Call Type:** Synchronous

Deletes an AML ("anti-money laundering") provider configuration.

You can disable an existing configuration without deleting it by using **UpdateAmlProviderConfig** and setting the value of *enabled* to *false.*

### Request

```json
{
    "omsId": 0,
    "productId": 0,
    "url": "",
    "amlProviderType": 0,
    "apiToken": "",
    "enabled": true
}
```

| Key             | Value                                                        |
| --------------- | ------------------------------------------------------------ |
| omsId           | **integer.** The Order Management System on which the anti-money laundering service functions. |
| productId       | **integer.** The ID of the product for which this AML service provider functions. Each product ID may have its own AML service provider. |
| url             | **string.** The URL address of the AML service provider.     |
| amlProviderType | **integer.** There are three AML configuration settings, or *types:*<br />**0** PassThrough &mdash; Allows cryptocurrency to be freely deposited.<br />**1** ChainAnalysis &mdash; A third-party that scores cryptocurrency deposits according to configurations from the Blockchain.<br />**2** Manual &mdash; Used for fiat (national) currency deposits. |
| apiToken        | **string.**  Token used by the Exchange to contact AML providers. The value for *apiToken* is supplied by AlphaPoint to the Exchange. Contact AlphaPoint if you need this token.   |
| enabled         | **Boolean.** If *true* the AML configuration is active for this product. If *false,* the configuration is not live. Setting *enabled* to *false* using **UpdateAmlProviderConfig** does not require deleting the whole configuration. |

### Response

```json
{
    "result": true,
    "errormsg": "",
    "errorcode": 0,
    "detail": ""
}
```
The Response is a standard response object.

| Key       | Value                                                        |
| --------- | ------------------------------------------------------------ |
| result    | **Boolean.** If the call has been successfully received by the Order Management System, *result* is *true;* otherwise it is *false.* |
| errormsg  | **string.** A successful receipt of the call returns *null.* The *errormsg* key for an unsuccessful call returns one of the following messages:<br />Not Authorized (errorcode 20)<br />Invalid Response (errorcode 100)<br />Operation Failed (errorcode 101)<br />Server Error (errorcode 102)<br />Resource Not Found (errorcode 104)<br />Operation Not Supported (errorcode 106) |
| errorcode | **integer.** A successful receipt of the call returns 0. An unsuccessful receipt of the call returns one of the *errorcodes* shown in the *errormsg* list. |
| detail    | **string.** Message text that the system may send.           |