## GetValidate2FARequiredEndpoints

**Category:** System<br />**Permissions:** Public<br />**Call Type:** Synchronous

Gets endpoints that require 2FA Validation
### Request

```json
{}
```

There is no payload.

### Response

```json
["CreateWithdrawTicket", "CreateDepositTicket", "AddUserPermission"]
```
The response is a list of endpoints.