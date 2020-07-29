---

title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - json

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes: # api - group - category - call
  - background/api_bkg_background
  - users/api_users_divider
  - users/api_users_act_activate2fa
  # - users/api_users_system_adduseraccount
  - users/api_users_system_addeditrole
  - users/api_users_user_adduseraffiliatetag
  - users/api_users_user_adduserinstrumentpermissions
  - users/api_users_user_adduserinstrumentpermissionsbulk
  # - users/api_users_system_addusermarketdatapermission
  # - users/api_users_system_adduserpermission
  - users/api_users_user_adduserproductpermissions
  - users/api_users_user_adduserproductpermissionsbulk
  - users/api_users_system_adduserrole
  - users/api_users_auth_authenticate2fa
  - users/api_users_auth_authenticateuser
  - users/api_users_user_canceluserreport
  # - users/api_users_system_coinsoauthauthenticateuser
  # - users/api_users_system_coinsoauthlogout
  # - users/api_users_system_confirmuseremail
  # - users/api_users_system_createuser
  # - users/api_users_system_disable2fa
  - users/api_users_system_deleterole
  - users/api_users_user_enablexp2fa
  # - users/api_users_system_enablegoogle2fa
  # - users/api_users_system_forceuserlogoff
  # - users/api_users_system_getaccountbadges
  # - users/api_users_system_getallbadges
  # - users/api_users_system_getavailablepermissionlist
  # - users/api_users_system_getbadgeaccount
  - users/api_users_system_getallroles
  - users/api_users_system_getconfigmanagementsupportedservicenames
  - users/api_users_user_getl2snapshot
  - users/api_users_user_getlevel1
  - gen_admin/api_genadmin_system_getoperatorusers
  # - users/api_users_system_getlockedusers
  # - users/api_users_system_getloggedinuserbysessiontoken
  - users/api_users_foureyes_getpendingfoureyerequests
  - users/api_users_foureyes_getcompletedfoureyerequests
  # - users/api_users_system_getrecentaffiliateregistrations
  - users/api_users_system_getrole
  - users/api_users_system_getserviceconfigs
  - users/api_users_system_getserviceconfigsbykey
  - users/api_users_system_reverttopreviousconfigvalue
  - users/api_users_user_getuseraccountinfos
  - users/api_users_user_getuseraccounts
  - users/api_users_user_getuseraffiliatecount
  # - users/api_users_system_getuseraffiliates
  - users/api_users_user_getuseraffiliatetag
  - users/api_users_system_getuserconfig
  - users/api_users_system_getallunredacteduserconfigsforuser
  - users/api_users_system_getunredacteduserconfigbykey
  - users/api_users_system_getuserdevices
  # - users/api_users_system_getuserinfo
  # - users/api_users_system_getusermarketdatapermissions
  # - users/api_users_system_getuserpermissions
  - users/api_users_user_getuserreporttickets
  - users/api_users_system_getuserroles
  # - users/api_users_system_getuserreportticketsbystatus
  - users/api_users_user_getuserreportwriterresultrecords
  - users/api_users_system_getvalidate2farequiredendpoints
  - users/api_users_auth_logout
  - users/api_users_system_registernewdevice
  # - users/api_users_system_registernewuser
  # - users/api_users_system_registeruser
  # - users/api_users_system_removeuseraccount
  # - users/api_users_system_removeuserconfig
  # - users/api_users_system_removeusermarketdatapermission
  - users/api_users_user_removeuserproductpermissions
  - users/api_users_system_removeuserrole
  # - users/api_users_system_removeuserreportticket
  # - users/api_users_system_resendverificationemail
  # - users/api_users_system_resetpassword
  # - users/api_users_system_resetpassword2
  # - users/api_users_system_revokeuserpermission
  # - users/api_users_system_setuserconfig
  # - users/api_users_system_setuserinfo
  - users/api_users_user_subscribeaccountevents
  - users/api_users_user_subscribelevel1
  - users/api_users_user_subscribelevel2
  - users/api_users_user_subscribeticker
  - users/api_users_user_subscribetrades
  - users/api_users_user_subscribeblocktrades
  - users/api_users_user_unsubscribeblocktrades
  # - users/api_users_system_unlockuser
  - users/api_users_user_unsubscribelevel1
  - users/api_users_user_unsubscribelevel2
  - users/api_users_user_unsubscribeticker
  - users/api_users_user_unsubscribetrades
  - users/api_users_user_updateuseraffiliatetag
  - users/api_users_system_updateserviceconfig
  - users/api_users_system_validate2fa
  - accounts/api_accts_divider
  # - accounts/api_accts_system_addaccount
  # - accounts/api_accts_system_addaccounthold
  # - accounts/api_accts_system_addbalancereconciliationinfo
  # - accounts/api_accts_system_addeditaccountbadge
  # - accounts/api_accts_system_addverificationlevelconfig
  # - accounts/api_accts_system_deleteverificationlevelconfig
  - accounts/api_accts_user_generatetradeactivityreport
  - accounts/api_accts_user_generatetransactionactivityreport
  - accounts/api_accts_user_generatetreasuryactivityreport
  # - accounts/api_accts_system_getaccountconfig
  # - accounts/api_accts_system_getaccountfees
  - accounts/api_accts_user_getaccountinfo
  - accounts/api_accts_user_getaccountledgerentry
  - accounts/api_accts_user_getaccountpositions
  - accounts/api_accts_system_getallaccountconfigs
  # - accounts/api_accts_system_getaccounts
  # - accounts/api_accts_system_getallaccountpositions
  # - accounts/api_accts_system_getallbalancereconciliationinfo
  # - accounts/api_accts_system_getbalancereconciliationinfo
  - accounts/api_accts_user_getledgerentriesbyaccount
  # - accounts/api_accts_system_getopenholds
  # - accounts/api_accts_system_getopenwithdrawholds
  - accounts/api_accts_user_gettreasuryproductsforaccount
  # - accounts/api_accts_system_getverificationlevelconfigs
  # - accounts/api_accts_system_removeaccountconfig
  # - accounts/api_accts_system_resetholds
  # - accounts/api_accts_system_resettradinglimits
  # - accounts/api_accts_system_resettreasurylimits
  # - accounts/api_accts_system_reverseaccounthold
  # - accounts/api_accts_system_reversewithdrawhold
  - accounts/api_accts_user_scheduletradeactivityreport
  - accounts/api_accts_user_scheduletransactionactivityreport
  - accounts/api_accts_user_scheduletreasuryactivityreport
  # - accounts/api_accts_system_setaccountconfig
  # - accounts/api_accts_system_submitaccountledgerentry
  # - accounts/api_accts_system_updateaccount
  - trades/api_trades_divider
  - trades/api_trades_user_getaccounttrades
  - trades/api_trades_user_getaccounttransactions
  - trades/api_trades_user_getopentradereports
  - trades/api_trades_user_getallopentradereports
  - trades/api_trades_user_gettickerhistory
  - trades/api_trades_user_gettradeshistory
  - oms_orders/api_omsord_divider
  - oms_orders/api_omsord_user_cancelallorders
  - oms_orders/api_omsord_user_cancelorder
  - oms_orders/api_omsord_user_cancelquote
  - oms_orders/api_omsord_user_cancelreplaceorder
  - oms_orders/api_omsord_user_createquote
  - oms_orders/api_omsord_user_getopenorders
  - oms_orders/api_omsord_user_getopenquotes
  - oms_orders/api_omsord_user_getorderfee
  - oms_orders/api_omsord_user_getorderhistory
  - oms_orders/api_omsord_user_getorderhistorybyorderid
  - oms_orders/api_omsord_user_getordershistory
  - oms_orders/api_omsord_user_getorderstatus
  - oms_orders/api_omsord_user_modifyorder
  # - oms_orders/api_omsord_system_sendexchangeorderstateevent
  - oms_orders/api_omsord_user_sendorder
  - oms_orders/api_omsord_user_submitblocktrade
  - oms_orders/api_omsord_user_updatequote
  - products/api_products_divider
  # - products/api_prods_system_addproduct
  - products/api_prods_user_addproductattributes
  # - products/api_prods_system_callaccountprovideradminfunction
  # - products/api_prods_system_canceltransferfunds
  # - products/api_prods_system_confirmrequesttransferfunds
  # - products/api_prods_system_confirmtransferfunds
  # - products/api_prods_system_createamlproviderconfig
  # - products/api_prods_system_deleteamlproviderconfig
  # - products/api_prods_system_editverificationlevelconfig
  # - products/api_prods_system_getaccountprovideradminfunctions
  # - products/api_prods_system_getaccountproviderdetails
  - products/api_prods_system_getamlproviderconfig
  - products/api_prods_system_getamlproviderconfigsforoms
  - products/api_prods_user_getproduct
  - products/api_prods_user_getproductattributes
  - products/api_prods_user_getproducts
  # - products/api_prods_system_getrequesttransfer
  # - products/api_prods_system_gettransfer
  # - products/api_prods_system_gettransfers
  # - products/api_prods_system_gettransfersreceived
  # - products/api_prods_system_rejectrequesttransferfunds
  # - products/api_prods_system_requesttransferfunds
  # - products/api_prods_system_transferfunds
  - products/api_prods_user_removeproductattributes
  - instrs/api_instrs_divider
  # - instrs/api_instrs_system_addinstrument
  - instrs/api_instrs_user_addinstrumentattributes
  # - instrs/api_instrs_system_editinstrumentverificationlevelconfig
  # - instrs/api_instrs_system_getdistributions
  - instrs/api_instrs_user_getinstrument
  - instrs/api_instrs_user_getinstrumentattributes
  - instrs/api_instrs_user_getinstruments
  # - instrs/api_instrs_system_getinstrumentverificationlevelconfigs
  # - instrs/api_instrs_system_getvenueinstruments
  - instrs/api_instrs_user_removeinstrumentattributes
  - instrs/api_instrs_user_getomsfeetiers
  # - instrs/api_instrs_system_setdistribution
  # - instrs/api_instrs_system_updateinstrument
  - tickets/api_tickets_divider
  # - tickets/api_tix_system_acceptwithdrawticket
  # - tickets/api_tix_system_adddepositticketattachment
  # - tickets/api_tix_system_addwithdrawticketattachment
  # - tickets/api_tix_system_cancelfailedwithdrawticket
  - tickets/api_tix_system_cancelwithdraw
  # - tickets/api_tix_system_confirmwithdraw
  # - tickets/api_tix_system_createassetmanagerwalletticket
  - tickets/api_tix_system_createdepositticket
  - tickets/api_tix_system_createwithdrawticket
  #- tickets/api_tix_system_deposit
  - tickets/api_tix_user_getaccountdeposittransactions
  - tickets/api_tix_user_getaccountwithdrawtransactions
  # - tickets/api_tix_system_getallassetmanagerwallettickets
  - tickets/api_tix_system_getallledgerentrytickets
  - tickets/api_tix_system_getalldeposittickets
  - tickets/api_tix_system_getalldepositrequestinfotemplates
  - tickets/api_tix_system_getallwithdrawtickets
  - tickets/api_tix_system_getassetmanagerwalletticket
  - tickets/api_tix_system_getdepositinfo
  - tickets/api_tix_system_getdepositrequestinfotemplate
  - tickets/api_tix_system_getdeposits
  - tickets/api_tix_system_getdepositticket
  # - tickets/api_tix_system_getdepositticketattachment
  - tickets/api_tix_system_getdeposittickets
  - tickets/api_tix_system_getomswithdrawfees
  - tickets/api_tix_user_getwithdrawfee
  - tickets/api_tix_system_getwithdraws
  - tickets/api_tix_system_getwithdrawtemplate
  - tickets/api_tix_system_getwithdrawtemplatetypes
  - tickets/api_tix_system_getwithdrawticket
  # - tickets/api_tix_system_getwithdrawticketattachment
  - tickets/api_tix_system_getwithdrawtickets
  # - tickets/api_tix_system_markdepositticketasfullyprocessed
  # - tickets/api_tix_system_markwithdrawticketascancelled
  # - tickets/api_tix_system_markwithdrawticketasconfirmed
  # - tickets/api_tix_system_markwithdrawticketasfullyprocessed
  # - tickets/api_tix_system_resubmitfailedwithdrawticket
  - tickets/api_tix_system_submitdepositticketcomment
  - tickets/api_tix_system_submitwithdrawticketcomment
  # - tickets/api_tix_system_updateassetmanagerwalletticket
  # - tickets/api_tix_system_updatedepositticket
  # - tickets/api_tix_system_updatewithdrawticket
  # - tickets/api_tix_system_withdraw
  # - user_verification/api_userverification_divider
  # - user_verification/api_uver_system_createvalidatorconfig
  # - user_verification/api_uver_system_setuserverificationlevel
  # - margin/api_margin_divider
  # - margin/api_marg_user_cancelmarginquote
  # - margin/api_marg_user_getaccountmarginstate
  # - margin/api_marg_user_sendmarginquote
  - uncertain/api_uncertain_divider
  # - uncertain/api_uncert_user_getallusergrouppermissions
  # - uncertain/api_uncert_null_getallusergroups
  # - uncertain/api_uncert_user_getalluserinstrumentpermissions
  # - uncertain/api_uncert_user_getalluserproductpermissions
  - uncertain/api_uncert_user_getearliestticktime
  # - uncertain/api_uncert_user_getusergrouppermissions
  - uncertain/api_uncert_user_ping
  # - uncertain/api_uncert_user_removeuserinstrumentpermissions
  # - uncertain/api_uncert_user_setusergrouppermission
  # - am_mgr/api_ammgr_divider
  # - am_mgr/api_ammgr_system_am_addeditaccountassetinfo
  # - am_mgr/api_ammgr_system_am_addeditaccountproviderinfo
  # - am_mgr/api_ammgr_system_am_addeditassetinfo
  # - am_mgr/api_ammgr_system_am_addedituser
  # - am_mgr/api_ammgr_system_am_getaccountassetdepositinfo
  # - am_mgr/api_ammgr_system_am_getaccountidbydepositinfo
  # - am_mgr/api_ammgr_system_am_getaccountinfo
  # - am_mgr/api_ammgr_system_am_getaccountproviderinfolist
  # - am_mgr/api_ammgr_system_sendassetmanagersequencereset
  # - exchange_admin/api_exchadmin_divider
  - exchange_admin/api_exchadmin_system_addeditexchange
  - exchange_admin/api_exchadmin_system_addeditexchangeinstrument
  # - exchange_admin/api_exchadmin_system_getexchanges
  # - exchange_admin/api_exchadmin_system_getexchangeserviceids
  # - exchange_admin/api_exchadmin_system_markethalt
  # - exchange_admin/api_exchadmin_system_marketpause
  # - exchange_admin/api_exchadmin_system_marketreopen
  # - exchange_admin/api_exchadmin_system_marketresume
  # - exchange_admin/api_exchadmin_system_marketresync
  # - exchange_admin/api_exchadmin_system_resetallmarketdatas
  # - exchange_admin/api_exchadmin_system_resetmarketdata
  # - gen_admin/api_genadmin_divider.md
  # - gen_admin/api_genadmin_system_addeditoms
  # - gen_admin/api_genadmin_system_addoperator
  # - gen_admin/api_genadmin_system_addoperatorconfig
  # - gen_admin/api_genadmin_system_addoperatoroms
  # - gen_admin/api_genadmin_system_createoperatorloyaltyfeeconfig
  # - gen_admin/api_genadmin_system_deleteoperatorloyaltyfeeconfig
  # - gen_admin/api_genadmin_system_getalloperatorloyaltyfeeconfigs
  # - gen_admin/api_genadmin_system_getoperatorloyaltyfeeconfig
  # - gen_admin/api_genadmin_system_getoperatorloyaltyfeeconfigsforoms
  # - gen_admin/api_genadmin_system_getoperatoromslist
  - gen_admin/api_genadmin_system_getoperators
  - gen_admin/api_genadmin_system_getoperatorusers
  # - gen_admin/api_genadmin_system_removeoperatoroms
  - gen_admin/api_genadmin_system_removeoperatoruser
  # - gen_admin/api_genadmin_system_sendemail
  # - gen_admin/api_genadmin_system_sendendofday
  # - gen_admin/api_genadmin_system_setdefaultoperatoroms
  # - gen_admin/api_genadmin_system_updateoperator

  # - functions/api_fees_divider
  # - products/api_prods_system_addproduct
  # - gen_admin/api_genadmin_system_createoperatorloyaltyfeeconfig
  # - gen_admin/api_genadmin_system_deleteoperatorloyaltyfeeconfig
  # - accounts/api_accts_system_getaccountfees
  # - trades/api_trades_user_getaccounttrades
  # - gen_admin/api_genadmin_system_getalloperatorloyaltyfeeconfigs
  # - tickets/api_tix_system_getallledgerentrytickets
  # - tickets/api_tix_system_getallwithdrawtickets
  # - tickets/api_tix_system_getdepositticket
  # - tickets/api_tix_system_getdeposittickets
  # - instrs/api_instrs_system_getdistributions
  # - tickets/api_tix_system_getomswithdrawfees
  # - accounts/api_accts_system_getopenholds
  # - accounts/api_accts_system_getopenwithdrawholds
  # - gen_admin/api_genadmin_system_getoperatorloyaltyfeeconfig
  # - gen_admin/api_genadmin_system_getoperatorloyaltyfeeconfigsforoms
  # - oms_orders/api_omsord_user_getorderfee
  # - products/api_prods_user_getproduct
  # - products/api_prods_user_getproducts
  # - users/api_users_user_getuseraccountinfos
  # - tickets/api_tix_user_getwithdrawfee
  # - tickets/api_tix_system_getwithdraws
  # - tickets/api_tix_system_getwithdrawticket
  # - instrs/api_instrs_system_setdistribution
  # - accounts/api_accts_system_updateaccount
  # - tickets/api_tix_system_updateassetmanagerwalletticket
  # - tickets/api_tix_system_updatedepositticket
  # - tickets/api_tix_system_updatewithdrawticket



  
  # - apad-markdown-documentation/api_apad_divider
  # - apad-markdown-documentation/api_apad_background
  # - apad-markdown-documentation/api_apad_clawbackshares
  # - apad-markdown-documentation/api_apad_createasset
  # - apad-markdown-documentation/api_apad_createcoadmin
  # - apad-markdown-documentation/api_apad_createcompany
  # - apad-markdown-documentation/api_apad_createcompanywithexistinguser
  # - apad-markdown-documentation/api_apad_createcompanywithuser
  # - apad-markdown-documentation/api_apad_createuser
  # - apad-markdown-documentation/api_apad_createuseragent
  # - apad-markdown-documentation/api_apad_createusercoshareholder
  # - apad-markdown-documentation/api_apad_getassets
  # - apad-markdown-documentation/api_apad_getcompanies
  # - apad-markdown-documentation/api_apad_getuserfromsession
  # - apad-markdown-documentation/api_apad_getusers
  # - apad-markdown-documentation/api_apad_removeallcoadmins
  # - apad-markdown-documentation/api_apad_removeuserrole
  # - apad-markdown-documentation/api_apad_setassetaccessforuser
  # - apad-markdown-documentation/api_apad_transferasset
  # - apad-markdown-documentation/api_apad_updatecompanyaddroles
  # - apad-markdown-documentation/api_apad_updateuser
  # - apad-markdown-documentation/api_apad_version
  # - digitizer/api_digitizer_doc
 


 
search: true
---

# Introduction

This API covers the User-category calls in **version 3.3** of the AlphaPoint Exchange software. It includes calls required for log-in and authentication.

The calls have been organized roughly to correspond to similar functions you would find in the AlphaPoint Admin. For example, in the Admin you manage users in the Users function. So calls that manage users have been gathered in the Users section of the API.


## 3.4.1 New Endpoints
**RegisterNewDevice**

**GetUserDevices**

**GetPendingFourEyeRequests**

**GetCompletedFourEyeRequests**

**ProcessPendingFourEyeRequest**

**GetConfigManagementSupportedServiceNames**

**GetServiceConfigs**

**GetServiceConfigByKey**

**UpdateServiceConfig**

**RevertToPreviousConfigValue**

**GetValidate2FARequiredEndpoints**

**Validate2FA**

**AddEditRole**

**DeleteRole**

**GetAllRoles**

**GetRole**

**AddUserRoles**

**RemoveUserRoles**

**GetUserRoles**

**GetAmlProviderConfigsForOMS**

**UpdateAmlProviderConfig**

## Revised Calls 3.4.1

**SendOrder**

Request Payload changed for Market Buy Value - if Buy order and Value (decimal) parameter is supplied, the Market order will execute up to the value specified.

**AddEditExchange**

Response Payload changed: 


>Old AddEditExchange Response

```json
{
    "Id": 1,
    "RejectMessage": ""
}
```

>New AddEditExchange Response

```json
{
    "result": true,
    "errormsg": "",
    "errorcode": 0,
    "detail": ""
}
```

**GetExchangeServiceIds**
>Old GetExchangeServiceIDs Response
An array of strings representing service ids.

>New GetExchangeServiceIds Response
Array hard coded with a single entry: "Matching Engine"

```json
[
    {
        "Name": "V2ExchangeCore|1",
        "ServiceId": "Matching Engine"
        "URI": null
    }
]
```

**GetExchanges**
>Old GetExchangeServiceIds Response
A list of exchanges within a specified exchange service id.

>New GetExchangeServiceIds Response
Retrieves exchanges from "THE" mathcing engine as there can only ever be one as of 3.4

**CreateAmlProviderConfig**
>Old CreateAmlProviderConfig Request

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

>New CreateAmlProviderConfig Request

```json
{
    "AmlProviderType": "ChainAnalysis",
    "Enabled": true,
    "OMSId": 0,
    "ProductId": 1
}
```

**DeleteAmlProviderConfig**
>Old DeleteAmlProviderConfig Request

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

>New DeleteAmlProviderConfig Request

```json
{
    "AmlProviderType": "ChainAnalysis",
    "Enabled": true,
    "OMSId": 0,
    "ProductId": 1
}
```


**GetAmlProviderConfig**
>Old GetAmlProviderConfig Request

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

>New GetAmlProviderConfig Request

```json
{
    "OMSId": 0,
    "ProductId": 1
}
```

**GetAmlProviderConfigsForOMS**
>New GetAmlProviderConfigForOMS Request

```json
{
    "OMSId": 0,
}
```

**Validate2FA**

Behavior change, no longer has public permissions specified. 

**AddInstrument (DEPRECATED)**

Behavior change, endpoint returns with bad request message specifying the endpoint is deprecated. 

**UpdateInstrument (DEPRECATED)**

Behavior change, endpoint returns with bad request message specifying the endpoint is deprecated. 

**RemoveOperatorUser**

Behavior change from “Deprecated” to “Remove Association of Operator with User" 

**GetOperatorUsers**

Behavior change from “Deprecated” to “Getting all Operator Users”


**GetOperators**

Field “EmailTemplateCount” [integer] added to response. 

## 3.5.0 Behavior Changes

**API Behavior Changes**

Any query APIs that return these objects now have the below new fields and response value changes as listed.

**AccountPosition**

| Key                 | Value                                                        |
| ------------------- | ------------------------------------------------------------ |
| NotionalHoldAmount| **decimal.** Cross Product Amount on Hold from open orders |
| NotionalRate | **decimal.** Current notional rate from base currency |
| TotalDayDepositNotional | **decimal.** Total Calendar Day Deposit Notional |
| TotalMonthDepositNotional | **deicmal.** Total Calendar Month Deposit Notional |
| TotalDayWithdrawNotional | **decimal.** Total Calendar Day Withdraw Notional |
| TotalMonthWithdrawNotional | **decimal.** Total Calendar Month Withdraw Notional |

**OrderTrade**

| Key                 | Value                                                        |
| ------------------- | ------------------------------------------------------------ |
| CounterPartyClientUserId| **int.** Indicates counterparty source of trade (OMS, Remarketer, FIX) |
| NotionalProductId | **int.** Notional product the notional value was captured in |
| NotionalRate | **decimal.** Notional rate from base currency at time of trade |
| NotionalValue | **decimal.** Notional value in base currency of venue at time of trade |

**AccountInstrumentStatistics**

| Key                 | Value                                                        |
| ------------------- | ------------------------------------------------------------ |
| NotionalProductId | **int.** Notional product the notional value was captured in |
| DailyNotionalTradeVolume | **decimal.** Total Calendar Day Trading Notional |
| MonthlyNotionalTradeVolume | **decimal.** Total Calendar Month Trading Notional |
| YearlyNotionalTradeVolume | **decimal.** Total Calendar Year Trading Notional |

**VerificationLevelInstruments**

| Key                 | Value                                                        |
| ------------------- | ------------------------------------------------------------ |
| NotionalProductId | **int.** Notional product the notional value was captured in |
| DailyNotionalLimit | **decimal.** Total Calendar Day Trading Notional |
| MonthlyNotionalLimit | **decimal.** Total Calendar Month Trading Notional |
| YearlyNotionalLimit | **decimal.** Total Calendar Year Trading Notional |

**AccountStatistics**

| Key                 | Value                                                        |
| ------------------- | ------------------------------------------------------------ |
| TotalDayDepositNotional | **decimal.** Total Calendar Day Deposit Notional |
| TotalMonthDepositNotional | **deicmal.** Total Calendar Month Deposit Notional |
| TotalDayWithdrawNotional | **decimal.** Total Calendar Day Withdraw Notional |
| TotalMonthWithdrawNotional | **decimal.** Total Calendar Month Withdraw Notional |

**VerificationLevelProducts**

| Key                 | Value                                                        |
| ------------------- | ------------------------------------------------------------ |
| DailyDepositNotionalLimit | **decimal.** Total Calendar Day Deposit Notional Limit |
| MonthlyDepositNotionalLimit | **decimal.** Total Calendar Month Deposit Notional Limit |
| DailyWithdrawNotionalLimit | **decimal.** Total Calendar Day Withdraw Notional Limit |
| MonthlyWithdrawNotionalLimit | **decimal.** Total Calendar Month Withdraw Notional Limit |

**OMSInfo**

| Key                 | Value                                                        |
| ------------------- | ------------------------------------------------------------ |
| BaseNotionalProductId | **int.** Id of Base Product to be used in Notional Limits |

**Fee**

| Key                 | Value                                                        |
| ------------------- | ------------------------------------------------------------ |
| FeeTier | **int.** Id of the Fee Tier the fee belongs to. Matches AccountInfo FeeGroupId (previously existing field) |

**Instrument**

| Key                 | Value                                                        |
| ------------------- | ------------------------------------------------------------ |
| PriceCollarIndexDifference | **decimal.** The percent different from the index price that an order is allowed to execute at. Anything falling outside of the index price +/- (1 + PriceCollarIndexDifference) will be collared |
| PriceCollarConvertToOtcEnabled | **bool.** Turns on/off conversion of collared orders to block trades |
| PriceCollarConvertToOtcClientUserId | **int.** Internal System UserId to assign the collared otc orders to. Should alwaays be 1 in current implementation (default) |
| PriceCollarConvertToOtcAccountId | **int.** Account Id to assign the collared orders to. This will effectively be a liability account that will need to have working block trades managed by operator. |
| PriceCollarConvertToOtcThreshold | **decimal.** Threshold of remaining size of order to convert to block trade. If collared order does not have remaining quantity above this threshold the remainder will be cancelled. |
| OtcConvertSizeEnabled | **bool.** Turns on/off auto conversion of 'large' limit orders converted to block trade orders upon receipt by the matching engine |
| OtcConvertSizeThreshold | **decimal.** Threshold to convert limit order quantity to block trade automatically for discovery by block trade market participants |

## Revised Calls 3.5.0

Support for additional fields has been added to the following requests:

 * GetAllDepositTickets
 * GetAllWithdrawTickets
 * GetAccounts
 * SubmitBlockTrade
 * ModifyOrder

Additional fields have been added to the following responses:

* GetWithdrawFormTemplateTypes
* SubmitAccountLedgerEntry
* GetAccountLedgerEntry
* GetAllLedgerEntryTickets
* GetOpenWithdrawHolds
* GetOrderStatus
* TransferFunds
* GetLevel1 / Level1UpdateEvent / SubscribeLevel1

## 3.5.0 New Endpoints

**GetAllAccountsConfigs**

**GetOMSFeeTiers**

**GetAllOpenTradeReports**

**SubscribeBlockTrades**

**UnsubscribeBlockTrades**

