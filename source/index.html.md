---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - json

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes: # api - group - category - call
  - background/api_bkg_background
  - users/api_users_divider
  - users/api_users_act_activate2fa
  - users/api_users_user_adduseraffiliatetag
  - users/api_users_auth_authenticate2fa
  - users/api_users_auth_authenticateuser
  - users/api_users_user_canceluserreport
  - users/api_users_user_getl2snapshot
  - users/api_users_user_getlevel1
  - users/api_users_user_getuseraccountinfos
  - users/api_users_user_getuseraccounts
  - users/api_users_user_getuseraffiliatecount
  - users/api_users_user_getuseraffiliatetag
  - users/api_users_user_getuserreporttickets
  - users/api_users_auth_logout
  - users/api_users_user_subscribeaccountevents
  - users/api_users_user_subscribelevel1
  - users/api_users_user_subscribelevel2
  - users/api_users_user_subscribeticker
  - users/api_users_user_subscribetrades
  - users/api_users_user_unsubscribelevel1
  - users/api_users_user_unsubscribelevel2
  - users/api_users_user_unsubscribeticker
  - users/api_users_user_unsubscribetrades
  - users/api_users_user_updateuseraffiliatetag
  - accounts/api_accts_divider
  - accounts/api_accts_user_generatetradeactivityreport
  - accounts/api_accts_user_generatetransactionactivityreport
  - accounts/api_accts_user_generatetreasuryactivityreport
  - accounts/api_accts_user_getaccountinfo
  - accounts/api_accts_user_getaccountpositions
  - accounts/api_accts_user_scheduletradeactivityreport
  - accounts/api_accts_user_scheduletransactionactivityreport
  - accounts/api_accts_user_scheduletreasuryactivityreport
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
  - oms_orders/api_omsord_user_modifyorder
  - oms_orders/api_omsord_user_sendorder
  - oms_orders/api_omsord_user_submitblocktrade
  - oms_orders/api_omsord_user_updatequote
  - products/api_products_divider
  - products/api_prods_user_getproduct
  - products/api_prods_user_getproducts
  - instrs/api_instrs_divider
  - instrs/api_instrs_user_getinstrument
  - instrs/api_instrs_user_getinstruments
  - tickets/api_tickets_divider
  - tickets/api_tix_user_getaccountdeposittransactions
  - tickets/api_tix_user_getaccountwithdrawtransactions
  - tickets/api_tix_user_getwithdrawfee
  - user_verification/api_userverification_divider
  - uncertain/api_uncertain_divider
  - uncertain/api_uncert_user_getearliestticktime
  - uncertain/api_uncert_user_ping




search: true
---

# Introduction

This API covers **version 3.1** of the AlphaPoint Exchange software. It includes calls in the "User" category, as well as a few others required for log-in and authentication.

The calls have been organized roughly to correspond to similar functions you would find in the AlphaPoint Admin. For example, in the Admin you manage users in the Users function. So calls that manage users have been gathered in the Users section of the API.

###Changed calls in this revision:
Generally, upper- and lowercase is not important for the key-value pairs inside a request or response. If an otherwise well formed call returns an unexpected error, check the case of the key-value pairs in the request.

- **CreateQuote:** The number of fields in the response has been reduced.
- **GetInstrument:** The quantityIncrement field has been changed from a long to a real.
- **GetInstruments:** The quantityIncrement field has been changed from a long to a real.
- **GetOpenQuotes:** Simplified response.
- **GetOrderHistory:** Major reduction in the number and fields of the response.
- **GetOrderHistoryByOrderId:** Major reduction in number of fields in the response.
- **GetOrdersHistory:** Reduction in number of fields in the response.
- **GetProduct:** TickSize changed from a long to a real.
- **GetProducts:** TickSize changed from a long to a real.
- **GetTickerHistory:** Permission revised to *Public.*
- **SendOrder:** Reduction in number of fields in the request.
- **SubscribeLevel2:** Added the ability to subscribe by specifying a product symbol.
- **UpdateQuote:** The number of fields in the response has been reduced.
