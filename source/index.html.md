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


### Revised calls - 3.3.2 --> 3.3.3


**GetAccountTrades**
**GetTradesHistory**

New fields added to response object

>Old Response

```json
[
    {
        "omsId": 0,
        "executionId": 0,
        "tradeId": 0,
        "orderId": 0,
        "accountId": 0,
        "subAccountId": 0,
        "clientOrderId": 0,
        "instrumentId": 0,
        "side": 0,
        "quantity": 0.0,
        "remainingQuantity": 0.0,
        "price": 0.0,
        "value": 0.0,
        "tradeTime": 0,
        "counterParty": null,
        "orderTradeRevision": 0,
        "direction": 0,
        "isBlockTrade": false,
        "tradeTimeMS": 0,
        "fee": 0.0,
        "feeProductId": 0,
        "orderOriginator": 0
    },
]
```

>New Response - Additional Fields OrderType, AccountName, UserName, MakerTaker, AdapterTradeId, InsideBid, InsideBidSize, InsideAsk, InsideAskSize, IsQuote

```json
[
    {
        "OMSId": 0,
        "ExecutionId": 0,
        "TradeId": 0,
        "OrderId": 0,
        "AccountId": 0,
        "AccountName": "",
        "SubAccountId": 0,
        "ClientOrderId": 0,
        "InstrumentId": 0,
        "Side": "Buy",
        "OrderType": "Limit"
        "Quantity": 0.0,
        "RemainingQuantity": 0.0,
        "Price": 0.0,
        "Value": 0.0,
        "CounterParty": "",
        "OrderTradeRevision": 0,
        "Direction": 0,
        "IsBlockTrade": false,
        "Fee": 0.0,
        "FeeProductId": 0,
        "OrderOriginator": 0,
        "UserName": "",
        "TradeTimeMS": 0,
        "MakerTaker": "Maker",
        "AdapterTradeId": 0,
        "InsideBid": 0,
        "InsideBidSize": 0,
        "InsideAsk": 0,
        "InsideAskSize": 0,
        "IsQuote": 0,
        "TradeTime": 0
    },
]
```


**GetUserConfig**
User Config Values are redacted by default (can be turned off via configuration).

### New Endpoints calls - 3.3.2 --> 3.3.3
**GetAllUnredactedUserConfigsForUser**

**GetAllLedgerEntryTickets**

**GetUnredactedUserConfigByKey**



### Revised calls - 3.0.X --> 3.3.2
Generally, upper- and lowercase is not important for the key-value pairs inside a request or response. If an otherwise well formed call returns an unexpected error, check the case of the key-value pairs in the request.

**AuthenticateUser**

Some integer Request values are now strings

> Old AuthenticateUser Request

```json
{
    "UserName": "",
    "Password":""
} or
{
    "APIKey": "",
    "Signature": "",
    "UserId":1,
    "Nonce": 12345
}
```

> New AuthenticateUser Request

```
{
    "UserName": "",
    "Password": ""
} or 
{
    "APIKey": "",
    "Signature": "",
    "UserId": "1",
    "Nonce": "12345"
 }
```

**CancelAllOrders**

The *userId* and *instrumentId* have been eliminated from the Request.

>Old CancelAllOrders Request

```json
{
    "AccountId": 0,
    "UserId": 0,
    "OMSId": 0,
    "InstrumentId": 0
}
```

>New CancelAllOrders Request

```json
{
    "AccountId": 0,
    "OMSId": 0
}
```



**CancelOrder**

*AccountId* added to Request.


>Old CancelOrder Request

```json
{
    "OMSId": 0,
    "OrderId": 0,
    "ClientOrderId": 0
}
```

>New CancelOrder Request

```json
{
    "OMSId": 0,
    "AccountId": 0,
    "OrderId": 0,
    "ClientOrderId": 0
}
```


**CancelQuote**

Now separate Response objects for *BidResult* and *AskResult* in Response


>Old CancelQuote Response

```json
{
    "BidResult": "",
    "AskResult": ""
}
```

>New CancelQuote Response

```json
{
 "BidResult": {
 "result": true,
  "errormsg": "",
  "errorcode": 0,
  "detail": "",
 },
 "AskResult": {
  "result": true,
   "errormsg": "",
   "errorcode": 0,
   "detail": "",
 }
}
```

**CreateQuote**

Revised Request structure; separate Response objects for *BidResult* and *AskResult[*

>Old CreateQuote Request

```json
{
    "BidQuoteId": 1,
    "BidRequest": "",
    "AskQuoteId": 1,
    "AskRequest": "" 
}
```

>New CreateQuote Request

```json
{
 "OMSId": 0,
 "AccountId": 0,
 "InstrumentId": 0,
 "Bid": 0,
 "BidQty": 0,
 "Ask": 0,
 "AskQty": 0,
}
```

>Old CreateQuote Response

```json
{ 
    "BidQuoteId": 1,
    "BidRequest": "",
    "AskQuoteId": 1,
    "AskRequest": ""
}
```

>New CreateQuote Response

```json
{
 /"BidResult": {
 / /"result": true,
 / /"errormsg": "",
 / /"errorcode": 0,
 / /"detail": "",
 /},
 /"AskResult": {
 / /"result": true,
 / /"errormsg": "",
 / /"errorcode": 0,
 / /"detail": "",
 /}
}
```

**GetAccountInfo**

*accountHandle* removed from Request.


>Old GetAccountInfo Request

```json
{
    "omsId": 0,
    "accountId": 0,
    "accountHandle": ""
}
```

>New GetAccountInfo Request

```json
{
    "omsId":0,
    "accountId":0
}
```

**GetAccountTrades**

Extended Response structure


>Old GetAccountTrades Response

```json
[
    {
        "omsId":0,
        "executionId":0,
        "tradeId":0,
        "orderId":0,
        "accountId":0,
        "subAccountId":0,
        "clientOrderId":0,
        "instrumentId":0,
        "side":0,
        "quantity":0.0,
        "remainingQuantity":0.0,
        "price":0.0,
        "value":0.0,
        "tradeTime":0
    },
]
```

>New GetAccountTrades Response

```json
[
    {
        "omsId": 0,
        "executionId": 0,
        "tradeId": 0,
        "orderId": 0,
        "accountId": 0,
        "subAccountId": 0,
        "clientOrderId": 0,
        "instrumentId": 0,
        "side": 0,
        "quantity": 0.0,
        "remainingQuantity": 0.0,
        "price": 0.0,
        "value": 0.0,
        "tradeTime": 0,
        "counterParty": null,
        "orderTradeRevision": 0,
        "direction": 0,
        "isBlockTrade": false,
        "tradeTimeMS": 0,
        "fee": 0.0,
        "feeProductId": 0,
        "orderOriginator": 0
    },
]
```

**GetAccountTransactions** 

*transactionType* and *referenceType* have changed to integer in Response.


>Old GetAccountTransactions Response

```json
[
    {
        {
        "TransactionId": 0,
        "OMSId": 0,
        "AccountId": 0,
        "CR": 0,
        "DR": 0,
        "CounterParty": 0,
        "TransactionType": {
        "Options": [
        	"Fee",
        	"Trade",
        	"Other",
        	"Reverse",
        	"Hold" ]
         },
		"ReferenceId": 0,
		"ReferenceType": {
    		"Options": [
      		  "Trade",
        	  "Deposit",
      	  	  "Withdraw",
        	  "Transfer",
        	  "OrderHold",
       	      "WithdrawHold",
        	  "DepositHold",
        	  "MarginHold" ]
			},
			"ProductId": 0,
			"Balance": 0,
			"TimeStamp": 0,
    	}
	]
```

>New GetAccountTransactions Response

```json
[
  {
    "transactionId":0,
    "omsId":0,
    "accountId":0,
    "cr":0.0,
    "dr":0.0,
    "counterparty":0,
    "transactionType":0,
    "referenceId":0,
    "referenceType":0,
    "productId":0,
    "balance":0.0,
    "timeStamp":0
    },
]
```

**GetInstrument**

*priceIncrement* added to Response


>Old GetInstrument Response

```json
{
    "omsId":0,
    "instrumentId":0,
    "symbol":null,
    "product1":0,
    "product1Symbol":null,
    "product2":0,
    "product2Symbol":null,
    "instrumentType":0,
    "venueInstrumentId":0,
    "venueId":0,
    "sortIndex":0,
    "sessionStatus":0,
    "previousSessionStatus":0,
    "sessionStatusDateTime":"0001-01-01T00:00:00",
    "selfTradePrevention":false,
    "quantityIncrement":0.0
}
```

>New GetInstrument Response

```json
{
    "omsId": 0,
    "instrumentId": 0,
    "symbol": null,
    "product1": 0,
    "product1Symbol": null,
    "product2": 0,
    "product2Symbol": null,
    "instrumentType": 0,
    "venueInstrumentId": 0,
    "venueId": 0,
    "sortIndex": 0,
    "sessionStatus": 0,
    "previousSessionStatus": 0,
    "sessionStatusDateTime": "0001-01-01T00:00:00",
    "selfTradePrevention": false,
    "quantityIncrement": 0.0,
    "priceIncrement": 0.0
}
```

**GetInstruments**

*priceIncrement* added to Response


>Old GetInstruments Response

```json
[
    {
        "omsId":0,
        "instrumentId":0,
        "symbol":"",
        "product1":0,
        "product1Symbol":"",
        "product2":0,
        "product2Symbol":"",
        "instrumentType":0,
        "venueInstrumentId":0,
        "venueId":0,
        "sortIndex":0,
        "sessionStatus":0,
        "previousSessionStatus":0,
        "sessionStatusDateTime":"0001-01-01T00:00:00",
        "selfTradePrevention":false,
        "quantityIncrement":0.0
    },
]
```

>New GetInstruments Response

```json
[
    {
        "omsId":0 ,
        "instrumentId": 0,
        "symbol": "",
        "product1": 0,
        "product1Symbol": "",
        "product2": 0,
        "product2Symbol": "",
        "instrumentType": 0,
        "venueInstrumentId": 0,
        "venueId":0,"sortIndex": 0,
        "sessionStatus": 0,
        "previousSessionStatus": 0,
        "sessionStatusDateTime": "0001-01-01T00:00:00",
        "selfTradePrevention": false,
        "quantityIncrement": 0.0,
        "priceIncrement": 0.0
    },
]
```

**GetOpenOrders**

Expanded and reorganized Response structure


>Old GetOpenOrders Response

```json
[
    {"omsId":0,
     "side":0,
     "orderId":0,
     "price":0.0,
     "quantity":0.0,
     "displayQuantity":0.0,
     "instrument":0,
     "account":0,
     "orderType":0,
     "clientOrderId":0,
     "orderState":0
    },
]
```

>New GetOpenOrders Response

```json
[
    {
        "Side": "Buy",
        "OrderId": 0,
        "Price":  0.0,
        "Quantity":  0.0,
        "DisplayQuantity":  0.0,
        "Instrument": 0,
        "Account": 0,
        "OrderType": "Unknown",
        "ClientOrderId": 0,
        "OrderState": "Unknown",
        "ReceiveTime": 0,
        "ReceiveTimeTicks": 0,
        "OrigQuantity": 0.0,
        "QuantityExecuted": 0.0,
        "AvgPrice": 0.0,
        "CounterPartyId": 0,
        "ChangeReason": "Unknown",
        "OrigOrderId": 0,
        "OrigClOrdId": 0,
        "EnteredBy": 0,
        "IsQuote": false,
        "InsideAsk": 0.0,
        "InsideAskSize": 0.0,
        "InsideBid": 0.0,
        "InsideBidSize": 0.0,
        "LastTradePrice": 0.0,
        "RejectReason": "",
        "IsLockedIn": false,
        "CancelReason": "",
        "OMSId": 0
    },
```

**GetOpenQuotes**

Expanded and reorganized Response structure


>Old GetOpenQuotes Response

```json
{
    "Bid":"",
    "Ask":""
}
```

>New GetOpenQuotes Response

```json
{
    "bid": {
        "omsId": 0,
        "side": 0,
        "orderId": 0,
        "price": 0.0,
        "quantity": 0.0,
        "displayQuantity": 0.0,
        "instrument": 0,
        "account": 0,
        "orderType": 0,
        "clientOrderId": 0,
        "orderState": 0
    },
    "ask": {
        "omsId": 0,
        "side": 0,
        "orderId": 0,
        "price": 0.0,
        "quantity": 0.0,
        "displayQuantity": 0.0,
        "instrument": 0,
        "account": 0,
        "orderType": 0,
        "clientOrderId": 0,
        "orderState": 0
    }
}
```

**GetOpenTradeReports**

Expanded and reorganized Response structure


>Old GetOpenTradeReports Response

```json
[
    {
        "omsId":0,
        "side":0,
        "orderId":0,
        "price":0.0,
        "quantity":0.0,
        "displayQuantity":0.0,
        "instrument":0,
        "account":0,
        "orderType":0,
        "clientOrderId":0,
        "orderState":0
    },
]
```

>New GetOpenTradeReports Response

```json
[
    {
        "Side": "Buy",
        "OrderId": 0,
        "Price":  0.0,
        "Quantity":  0.0,
        "DisplayQuantity":  0.0,
        "Instrument": 0,
        "Account": 0,
        "OrderType": "Unknown",
        "ClientOrderId": 0,
        "OrderState": "Unknown",
        "ReceiveTime": 0,
        "ReceiveTimeTicks": 0,
        "OrigQuantity": 0.0,
        "QuantityExecuted": 0.0,
        "AvgPrice": 0.0,
        "CounterPartyId": 0,
        "ChangeReason": "Unknown",
        "OrigOrderId": 0,
        "OrigClOrdId": 0,
        "EnteredBy": 0,
        "IsQuote": false,
        "InsideAsk": 0.0,
        "InsideAskSize": 0.0,
        "InsideBid": 0.0,
        "InsideBidSize": 0.0,
        "LastTradePrice": 0.0,
        "RejectReason": "",
        "IsLockedIn": false,
        "CancelReason": "",
        "OMSId": 0
    },
]
```

**GetOrderHistory**

Expanded and reorganized Response structure


>Old GetOrderHistory Response

```json
[
    {
        "omsId":0,
        "side":0,
        "orderId":0,
        "price":0.0,
        "quantity":0.0,
        "displayQuantity":0.0,
        "instrument":0,
        "account":0,
        "orderType":0,
        "clientOrderId":0,
        "orderState":0
    }
]
```

>New GetOrderHistory Response

```json
[
    {
        "Side": "Buy",
        "OrderId": 0,
        "Price":  0.0,
        "Quantity":  0.0,
        "DisplayQuantity":  0.0,
        "Instrument": 0,
        "Account": 0,
        "OrderType": "Unknown",
        "ClientOrderId": 0,
        "OrderState": "Unknown",
        "ReceiveTime": 0,
        "ReceiveTimeTicks": 0,
        "OrigQuantity": 0.0,
        "QuantityExecuted": 0.0,
        "AvgPrice": 0.0,
        "CounterPartyId": 0,
        "ChangeReason": "Unknown",
        "OrigOrderId": 0,
        "OrigClOrdId": 0,
        "EnteredBy": 0,
        "IsQuote": false,
        "InsideAsk": 0.0,
        "InsideAskSize": 0.0,
        "InsideBid": 0.0,
        "InsideBidSize": 0.0,
        "LastTradePrice": 0.0,
        "RejectReason": "",
        "IsLockedIn": false,
        "CancelReason": "",
        "OMSId": 0
    },
]
```

**GetOrderHistoryByOrderId**

Expanded and reorganized Response structure


>Old GetOrderHistoryByOrderId Response

```json
[
    {
        "omsId":0,
        "side":0,
        "orderId":0,
        "price":0.0,
        "quantity":0.0,
        "displayQuantity":0.0,
        "instrument":0,
        "account":0,
        "orderType":0,
        "clientOrderId":0,
        "orderState":0
    }
]
```

>New GetOrderHistoryByOrderId Response

```json
[
    {
        "Side": "Buy",
        "OrderId": 0,
        "Price":  0.0,
        "Quantity":  0.0,
        "DisplayQuantity":  0.0,
        "Instrument": 0,
        "Account": 0,
        "OrderType": "Unknown",
        "ClientOrderId": 0,
        "OrderState": "Unknown",
        "ReceiveTime": 0,
        "ReceiveTimeTicks": 0,
        "OrigQuantity": 0.0,
        "QuantityExecuted": 0.0,
        "AvgPrice": 0.0,
        "CounterPartyId": 0,
        "ChangeReason": "Unknown",
        "OrigOrderId": 0,
        "OrigClOrdId": 0,
        "EnteredBy": 0,
        "IsQuote": false,
        "InsideAsk": 0.0,
        "InsideAskSize": 0.0,
        "InsideBid": 0.0,
        "InsideBidSize": 0.0,
        "LastTradePrice": 0.0,
        "RejectReason": "",
        "IsLockedIn": false,
        "CancelReason": "",
        "OMSId": 0
    },
]
```

**GetOrdersHistory**

Expanded and reorganized Response structure


>Old GetOrdersHistory Response

```json
[
    {
        "omsId":0,
        "side":0,
        "orderId":0,
        "price":0.0,
        "quantity":0.0,
        "displayQuantity":0.0,
        "instrument":0,
        "account":0,
        "orderType":0,
        "clientOrderId":0,
        "orderState":0
    }
]
```

>New GetOrdersHistory Response

```json
[
    {
        "Side": "Buy",
        "OrderId": 0,
        "Price":  0.0,
        "Quantity":  0.0,
        "DisplayQuantity":  0.0,
        "Instrument": 0,
        "Account": 0,
        "OrderType": "Unknown",
        "ClientOrderId": 0,
        "OrderState": "Unknown",
        "ReceiveTime": 0,
        "ReceiveTimeTicks": 0,
        "OrigQuantity": 0.0,
        "QuantityExecuted": 0.0,
        "AvgPrice": 0.0,
        "CounterPartyId": 0,
        "ChangeReason": "Unknown",
        "OrigOrderId": 0,
        "OrigClOrdId": 0,
        "EnteredBy": 0,
        "IsQuote": false,
        "InsideAsk": 0.0,
        "InsideAskSize": 0.0,
        "InsideBid": 0.0,
        "InsideBidSize": 0.0,
        "LastTradePrice": 0.0,
        "RejectReason": "",
        "IsLockedIn": false,
        "CancelReason": "",
        "OMSId": 0
    },
]
```

**GetOrderStatus**

Expanded and reorganized Response structure


>Old GetOrderStatus Response

```json
{
    "omsId":0,
    "side":0,
    "orderId":0,
    "price":0.0,
    "quantity":0.0,
    "displayQuantity":0.0,
    "instrument":0,
    "account":0,
    "orderType":0,
    "clientOrderId":0,
    "orderState":0
}
```

>New GetOrderStatus Response

```json
[
    {
        "Side": "Buy",
        "OrderId": 0,
        "Price":  0.0,
        "Quantity":  0.0,
        "DisplayQuantity":  0.0,
        "Instrument": 0,
        "Account": 0,
        "OrderType": "Unknown",
        "ClientOrderId": 0,
        "OrderState": "Unknown",
        "ReceiveTime": 0,
        "ReceiveTimeTicks": 0,
        "OrigQuantity": 0.0,
        "QuantityExecuted": 0.0,
        "AvgPrice": 0.0,
        "CounterPartyId": 0,
        "ChangeReason": "Unknown",
        "OrigOrderId": 0,
        "OrigClOrdId": 0,
        "EnteredBy": 0,
        "IsQuote": false,
        "InsideAsk": 0.0,
        "InsideAskSize": 0.0,
        "InsideBid": 0.0,
        "InsideBidSize": 0.0,
        "LastTradePrice": 0.0,
        "RejectReason": "",
        "IsLockedIn": false,
        "CancelReason": "",
        "OMSId": 0
    },
]
```

**GetTradesHistory**

Extended Response structure


>Old GetTradesHistory Response

```json
[
    {
        "omsId":0,
        "executionId":0,
        "tradeId":0,
        "orderId":0,
        "accountId":0,
        "subAccountId":0,
        "clientOrderId":0,
        "instrumentId":0,
        "side":0,
        "quantity":0.0,
        "remainingQuantity":0.0,
        "price":0.0,
        "value":0.0,
        "tradeTime":0
    }
]
```

>New GetTradesHistory Response

```json
[
    {
        "omsId": 0,
        "executionId": 0,
        "tradeId": 0,
        "orderId": 0,
        "accountId": 0,
        "subAccountId": 0,
        "clientOrderId": 0,
        "instrumentId": 0,
        "side": 0,
        "quantity": 0.0,
        "remainingQuantity": 0.0,
        "price": 0.0,
        "value": 0.0,
        "tradeTime": 0,
        "counterParty": null,
        "orderTradeRevision": 0,
        "direction": 0,
        "isBlockTrade": false,
        "tradeTimeMS": 0,
        "fee": 0.0,
        "feeProductId": 0,
        "orderOriginator": 0
    },
]
```

**SendOrder**

Request: *timeInOrder* removed; *quantity,* *PegPriceType* changed to integer enumerations


>Old SendOrder Request

```json
{
    "InstrumentId": 1,
    "OMSId": 1,
    "AccountId": 1,
    "TimeInForce": 1,
    "ClientOrderId": 1,
    "OrderIdOCO": 0, 
    "TimeInOrder":0, 
    "UseDisplayQuantity":false, 
    "Side": 0,
    "quantity": "1",
    "OrderType": 2,
    "PegPriceType": "3",
    "LimitPrice": 8800 
}
```

>New SendOrder Request

```json
{
     "InstrumentId": 1,
     "OMSId": 1,
     "AccountId": 1,
     "TimeInForce": 1,
     "ClientOrderId": 1,
     "OrderIdOCO": 0,
     "UseDisplayQuantity": false,
     "Side": 0,
     "quantity": 1,
     "OrderType": 2,
     "PegPriceType": 3,
     "LimitPrice": 8800
 }
```

**SubscribeLevel2**

Request alternative available; changed to comma-separated data from numerical key-value pairs in the Response.


>Old SubscribeLevel2 Request

```json
{
    "OMSId": 1,
    "InstrumentId": 1,
    "Depth": 10
}
```

>New SubscribeLevel2 Request

```json
{
    "OMSId":  1,
    "InstrumentId": 0
    "Depth":  10 
}
or
{
    "OMSId":  1,
    "Symbol": "BTCUSD",
    "Depth":  10 
}
```

>Old SubscribeLevel2 Response

```json
[
    {
        0: 1,
        1: 1,
        2: 1534865075981,
        3: 0,
        4: 6415.01,
        5: 1,
        6: 6399.79,
        7: 1, 
        8: 1.49364749, 
        9: 0
    }
]
```

>New SubscribeLevel2 Response

```json
[
    [
        0, // MDUpdateId        
        1, // AccountId
        123,// ActionDateTime in Posix format X 1000
        0,   // ActionType 0 (New), 1 (Update), 2(Delete)
        0.0, // LastTradePrice
        0, // OrderId
        0.0, //Price
        0,  // ProductPairCode
        0.0, // Quantity
        0, // Side
    ],
]
```


>Old SubmitLedgerEntry Response

```json
{
    "result":true,
    "errormsg":"",
    "errorcode": 0,
    "detail":"",
}
```

>New SubmitLedgerEntry Response

```json
{
        "accountLedgerEntryId": 0,
        "accountId": 0,
        "productId": 0,
        "CR_Amt": 0.0,
        "DR_Amt": 0.0,
        "enteredBy": 0.0,
        "comments": "",
        "onsSidedTransaction": false
    },
```


### Previously unrevealed calls

**AddProductAttributes**

*InstrumentId* changed to *ProductId* in Request


>Old AddProductAttributes Request

```json
{
    "OMSId": 1,
    "InstrumentId": 1,
    "KeyName": key,
    "KeyValue": "value"
}
```

>New AddProductAttributes Request

```json
{
    "OMSId": 1,
    "ProductId": 1,
    "KeyName": key,
    "KeyValue": "value"
}
```

**AddUserInstrumentPermissionsBulk**

*InstrumentIds* now an array in Request


>Old AddUserInstrumentPermissionsBulk Request

```json
{
    "OMSId": 1,
    "InstrumentId": 1,
    "UserId": 1
}
```

>New AddUserInstrumentPermissions Bulk Request

```json
{
    "OMSId": 1,
    "InstrumentIds": [1,2],
    "UserId": [1,2]
}
```

**AddUserProductPermissionsBulk**

*ProductIds* now an array in Request


>Old AddUserProductPermissionsBulk Request

```json
{
    "omsid":0,
    "productids":"",
    "userids":""}

```

>New AddUserProductPermissionsBulk Request

```json
{
    "omsid": 0,
    "productids": [1,2],
    "userids": [1,2]
}
```

**GetEarliestTickTime**

Request requires only *OMSId* and *instrumentId*


>Old GetEarliestTickTime Request

```json
{
    "InstrumentId": 1,
    "FromDate": date
}
```

>New GetEarliestTickTime

```json
{
    "InstrumentId": 1,
    "OMSId": 1
}
```

**RemoveProductAttributes**

*InstrumentId* changed to *ProductId* in Request


>Old RemoveProductAttributes Request

```json
{
    "OMSId": 1,
    "InstrumentId": 1, 
    "KeyName": key, 
    "KeyValue": "value" 
}
```

>New RemoveProductAttributes Request

```json
{
    "OMSId": 1,
    "ProductId": 1,
    "KeyName": "key",
    "KeyValue": "value"
}
```

### 3.4.1 New Endpoints
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

### RevisedCalls 3.4.1

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
