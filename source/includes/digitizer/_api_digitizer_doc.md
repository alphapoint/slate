# Digitizer

The Digitizer is an application separate from the APAD Private Shares API (PSAPI). It creates and merges small contracts (currently exclusive to Ethereum). Digitizer makes minimal contact with the AlphaPoint Exchange API. The APAD Private Shares API handles the connection with the Exchange software. The Digitizer works with a specific Account Provider to post information to and read information from the Blockchain.

Digitizer was developed using GraphQL. Extensive deocumentation for the GraphQL language is available on line at https://graphql.org/learn/.

<aside class="notice"><strong>Note: </strong>Digitizer differentiates between uppercase and lowercase letters.</aside>

## Operation Types

There are three operation types used by Digitizer: *query,* *mutation,* and *subscription.* In the following explanations, "the server" is the Ethereum Blockchain.

- **Query** &mdash; Reads data from the server via an Account Provider. A query is essentially a *get.*
- **Mutation** &mdash; Sends or writes data to the server via an Account Provider (it "mutates" or changes existing data). A mutation is essentially a *put* or a *post.*
- **Subscription** &mdash; Pushes data from the server to a client that is listening in real-time. A subscription notifies the client of an event.

## Data Types

There are three scalar data types: *String,* *Int,* and *Boolean.*

- **String** &mdash; Represents textual data as UTF-8 character sequences. Digitizer uses strings to show free-form, human-readable text.
- **Int** &mdash; Represents non-fractional signed whole-number values between &ndash;(2^31) and (2^31)&ndash;1.
- **Boolean** &mdash; Represents values of *true* or *false.*

<aside class="notification"><strong>Note: </strong>An exclamation point (!) or "bang" at the end of an argument's type means that a value for the argument's parameter is required by the call. An exclamation point/bang in the type of field of an object means that that field will contain and return content; fields without a ! may or may not contain content and may not return content.</aside>

## Object Types

Digitizer includes 14 predefined object types that the queries and mutations refer to and use. Some objects include other objects as defined here.

Some fields of the objects are relevant only to certain templates. For example, RABT or ERC20 tokens can be paused. A paused status would not be returned for a token that was not pausable.

### Account

| Key     | Value                                                        |
| ------- | ------------------------------------------------------------ |
| balance | **String!** The quantity of tokens in the account of the calling user. |

### Asset

The **deploy** mutation creates an instance of the Asset object.

| Key             | Value                                                        |
| --------------- | ------------------------------------------------------------ |
| id              | **String!** The ID of the asset, assigned by the system.     |
| name            | **String!** The name of the asset.                           |
| symbol          | **String!** The trading symbol of the asset; usually a four-letter string. |
| decimals        | **Int!** The number of decimal places in which the asset is denominated. The maximum number of decimal places is 18. |
| address         | **String!** The *contract address* of the transaction; the address on the Ethereum blockchain that contains the contract. The **deploy** mutation returns this address. |
| issuerAddress   | **String!** The *issuerAddress* is generated in the Digitizer UI from the initial wallet setup. This value is a constant per environment. Minting takes place from the *issuerAddress.* |
| template        | **String!** The name of the template used by the asset.      |
| network         | **Network!** object. See the Network object.                 |
| supply          | **Int!** Not currently used. Set to 0 and always returns 0.  |
| cap             | **Int!**  The maximum amount of tokens allowed to be minted for the life of the token. Equivalent to "authorized shares" as opposed to shares in circulation. |
| transferCount   | **Int!** A count of all transfers that have happened to the token. |
| isPausable      | **Boolean!** A value of *true* means that the token can be paused. |
| paused          | **Boolean!** A value of *true* means that the token currently is paused. |

### CapTableRow

The blockchain does not include the concept of balances; balances must be calculated from transaction history. The *capTable* holds the balances from these transactions.

| Key        | Value                                                        |
| ---------- | ------------------------------------------------------------ |
| name       | **String!** A human-readable account name &mdash; if an account name is associated with the deposit key address in the AlphaPoint Exchange. If the name association does not exist, this field shows the address of the transfer destination; a wallet address. |
| address    | **String!** The actual deposit key or the public key to which the token is sent. |
| balance    | **String** The quantity of tokens in the account.            |
| percentage | **String!** The ratio of balance to the total potential supply of tokens (see *cap* in the Assets object). |

### ChainEvent

Values in the ChainEvent object are valid for different operations, for example querying for historical chain event, a subscription that provides confirmations, whitelist events, or other events.

<aside class="notice"><strong>Note: </strong>A RABT token behaves like a standard ERC20 token, but will force a third-party approval process on any transaction; this process may take additional time.</aside>

| Key                   | Value                                                        |
| --------------------- | ------------------------------------------------------------ |
| type                  | **String!** Describes the type of event that occurred on the blockchain. One of:<br /><br />**PendingEvent:** Occurs prior to receiving the first confirmation (ConfirmationEvent)<br />**ConfirmationEvent:** Occurs when a confirmation is received from the blockchain.<br />**ErrorEvent:** Any error. Provides the token address and an error string.<br />**CheckStatusEvent:** Specific to RABT.<br />**PendingTransferEvent:** Specific to RABT. |
| symbol                | **String!** Short name for the token; created during the **deploy** mutation. |
| name                  | **String!** Long name for the token; created during the **deploy** mutation. |
| tokenAddress          | **String** The *tokenAddress* is the contract address (called *deploy*) returned during the **deploy** mutation. |
| blockNumber           | **Int** An index into the blockchain that shows where the transaction resides (in the form of a hash). |
| blockHash             | **String** A hexadecimal in string form that represents the metadata from the block on the blockchain where the transaction resides. |
| transactionHash       | **String**  A hexadecimal in string form that represents a hash of the transaction. It cannot be decrypted. It acts as a checksum because a third party with access to the transaction information can obtain an equivalent hash using the same algorithm. This value is always available on the blockchain. |
| requiredConfirmations | **Int** The number of confirmations required for confidence that a transaction has been written to the blockchain. Set by AlphaPoint generally at 12 and configurable upon creation of the Account Provider for that token. |
| confirmation          | **Int** Count of received confirmations (up to *requiredConfirmations*). Any additional confirmations are ignored. |
| json                  | **String**  A JSON representation of the raw event object retrieved from the blockchain directly and without imposing any processing. Part of the CheckStatusEvent used for RABTs. |
| code                  | **String** Unused field                                                |
| description           | **String** A human-readable description of the transaction.  |
| spender               | **String** **RTokens only.** The contract address of the entity paying Gas for the transfer. Usually this is the same entity shown in the *from* value (below) but allows for a separation if required. In most cases, contains the AlphaPoint address. |
| from                  | **String** The address of the sender of the transaction.     |
| to                    | **String** The address of the receiver of the transaction.   |
| amount                | **String** The amount of the transfer, expressed in unit tokens and decimals. Ethereum imposes a maximum of 18 decimal places on tokens. |

### LoginUser

| Key    | Value                                                       |
| ------ | ----------------------------------------------------------- |
| userId | **Int!** The user ID obtained from the AlphaPoint Exchange. |

### Network

Each Networks object is an Ethereum network. The **networks** query returns an array of Network objects.

| Key             | Value                                                        |
| --------------- | ------------------------------------------------------------ |
| id              | **String!** The ID of the network, for example, 42.          |
| name            | **String!** The name of the network, for example "Jones Net". |
| enabled         | **Boolean!** The *enabled* Boolean determines whether the network is enabled in this API. Not all networks available generally may be enabled in the API. A value of *true* means that the network is enabled. |
| etherscanDomain | **String** Etherscan is a tool that visualizes the Ethereum blockchain. The value of *etherscanDomain* sets a base URL so that the Etherscan tool can build the correct Etherscan domain for your network. Not every network will have a valid Etherscan domain. For example, if you're using the Kovan (test) blockchain, setting the value of *etherscanDomain* to https://etherscan.io/ results in a value for *etherscanDomain* of https://kovan.etherscan.io/. |

### PendingTransfers

The PendingTransfers object is for Regulated Asset-Backed Tokens (RABTs).

| Key         | Value                                                        |
| ----------- | ------------------------------------------------------------ |
| assetId     | **String!** Contract address for the token (not the value of *assetId* as returned by the **assets** call). |
| pendingHash | **String!** A 32-byte hexadecimal hash ID that uniquely identifies the transfer. |
| from        | **String!** The source address of the token.                 |
| to          | **String!** The destination address of the token.            |
| amount      | **String!** The unit and fractional amount of token being transferred. Ethereum sets the  maximum number of decimal places to 18. |

### Protocols

The query **protocols** returns an array of protocols that are available to you.

| Key     | Value                                                        |
| ------- | ------------------------------------------------------------ |
| id      | **String!** The ID assigned to the protocol by the system.   |
| name    | **String!** The name of the protocol; for example, "Ethereum". |
| enabled | **Boolean!** The *enabled* Boolean determines whether the protocol is enabled in this API. Not all protocols generally available may be enabled in the API. A value of *true* means that the protocol is available. |

### Templates

| Key         | Value                                                        |
| ----------- | ------------------------------------------------------------ |
| id          | **String** The ID of this template.                          |
| name        | **String** The short name of this template; for example, "MegaERC20". |
| fullName    | **String** The full name of this template; for example, "ERC20 + Mint, Burn, Pause, Reclaim". |
| description | **String** A human-readable description of the template. For example, "Best suited for company shares and assets that appreciate." |

### TokenDefinition

| Key      | Value                                                        |
| -------- | ------------------------------------------------------------ |
| name     | **String!** The ID of this token.                            |
| symbol   | **String!** The trading symbol of this token (usually four characters). |
| supply   | **String!** Not currently used. Set to 0 and always returns 0. |
| decimals | **Int!** The number of decimal places in which the token is denominated. The Ethereum blockchain imposes a limit of 18 decimal places. |
| cap      | **Int!** The maximum amount of tokens allowed to be minted for the life of the token. Equivalent to "authorized shares" as opposed to shares in circulation. |

### TxStatus 

In Digitizer, a "transaction" can be several different things &mdash; not just a transfer of tokens from one address to another. Some of these transactions cost Gas, and some do not. The TxStatus (transaction status) object describes the nature of the transaction.

| Key                   | Value                                                        |
| --------------------- | ------------------------------------------------------------ |
| transactionHash       | **String!**  **RABT only.** A 32-byte hexadecimal hash ID that uniquely identifies the transfer. |
| type                  | **String!** Describes the type of transaction. One of:<br /><br />mint<br />whitelist<br />burn<br />pause<br />resume<br />transferAllowed<br />transferRejected<br />maxshareholders<br />transfer<br />clawback |
| status                | **String!**  Provides the status of the transaction. One of:<br /><br />PendingEvent<br />ConfirmationEvent<br />ErrorEvent<br />CheckStatusEvent<br />PendingTransferEvent |
| uuid                  | **String!** AlphaPoint internally-generated unique ID. The ID is generated prior to receiving the hash ID from the blockchain. |
| confirmation          | **Int** The current count of confirmations received for the transaction (up to the value of *requiredConfirmations*). |
| requiredConfirmations | **Int** The number of confirmations required for confidence that a transaction has been written to the blockchain. Set by AlphaPoint generally at 12. |
| data                  | **String** Contains context-specific data direct from the blockchain that can be used for verification. |
| error                 | **String** This string contains whatever error message the blockchain supplies. |

### Users

| Key        | Value                                                        |
| ---------- | ------------------------------------------------------------ |
| name       | **String!** The human-readable user name from the AlphaPoint Exchange. |
| apexUserId | **Int!** The user ID generated by the AlphaPoint Exchange.   |

### 

# Queries

Queries retrieve data from the Blockchain.

> Example 1.

```
query {
    queryName(arg1: arg1Value,
    arg2: arg2Value, ...
    arg_n: arg_n_value) {param1 param2 ... param_n}
}
```

The format of a query (Example 1).

> Example 2.

```
{
  "data": {
    "protocols": [
      {
        "id": "0",
        "name": "Ethereum"
      }
    ]
  }
}
```

The format of a typical query response (Example 2).

> Example 3: Error message

```
{
  "data": {
    "capTable": null
  },
  "errors": [
    {
      "message": "no Asset found for assetId=651002070",
      "locations": [
        {
          "line": 2,
          "column": 3
        }
      ],
      "path": [
        "capTable"
      ]
    }
  ]
}
```

The Digitizer will return error messages, as in Example 3.

## Account

```
query {
    account(assetId: "0x4B3d449442a2fdECF1bA128e562c97Bbb6AFFDa9", 
    accountAddress: "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56" ) 
    {balance}
}

# Account response:
To come
```

*account(assetId: String, accountAddress: String): Account*

Returns the balance of the asset identified by *assetId.* The *assetId* must match an *address* returned by the **assets** query (not an ID returned by the **assets** query). The *accountAddress* must match a token-holding address.

## Asset

```
query {
    asset(assetId: "0x4B3d449442a2fdECF1bA128e562c97Bbb6AFFDa9") { id name cap }
}

# Asset response:
{
  "data": {
    "asset": {
      "id": "253154359",
      "name": "Ttest",
      "cap": 8
    }
  }
}
```

*asset(assetId: String): Asset*

Returns the general attributes and state of a single deployed token (the *assetId*). The value of *assetId* must match an *asset address* returned by the **assets** query (not the *asset ID* value). 

## Assets

```
query {
    assets(networkId: "42") {id name symbol address}
}

#Assets response:
{
  "data": {
    "assets": [
      {
        "id": "46930172",
        "name": "FundXYZ",
        "symbol": "FXYZ",
        "address": "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56"
      },
      {
        "id": "120478063",
        "name": "ERC223-Test",
        "symbol": "E223T",
        "address": "0x9f9321FcdE598e9db1BDE3b599D3F5e035054DbC"
      },
      {
        "id": "55930076",
        "name": "Z-ERC223",
        "symbol": "Z223",
        "address": "0x51F3EB640C09854fEdB660a8E353175991f0F1e6"
      },
      {
        "id": "86150153",
        "name": "TokenNBA",
        "symbol": "TNBA",
        "address": "0xB05D537902F6720568Be2220Ed96c330A78C091B"
      },
      {
        "id": "651002070",
        "name": "ZToken",
        "symbol": "ZT1",
        "address": "0x21be0fdad4cAc4381D8FF273B7c583070C6B79C6"
      },
      {
        "id": "84926442",
        "name": "TokenMFH",
        "symbol": "TMFH",
        "address": "0xfeD1FcAbCAb5DDFe38F4694E64564aC5930aa725"
      }
    ]
  }
}
```

*assets(networkId: String): [Asset]*

Returns an array of data from all tokens that have been deployed to the network via APAD. Tokens deployed to the network outside of APAD are ignored. The value of *networkId* must match a network returned from the **networks** query.

## CapTable

```
query {
    capTable(assetId: "0x4B3d449442a2fdECF1bA128e562c97Bbb6AFFDa9") 
    {name address balance percentage}
}

# capTable response:
{
  "data": {
    "capTable": [
      {
        "name": "0x0FdC8aE59cC945BeEd8e7C71aAF1557d1Bb7119A",
        "address": "0x0FdC8aE59cC945BeEd8e7C71aAF1557d1Bb7119A",
        "balance": "5",
        "percentage": "100.00%"
      }
    ]
  }
}
```

*captTable(assetId: String): [CapTableRow]*

Calculates and returns an array that describes the captable for the asset identified by *assetId.* The value for *assetId* must match a contract address returned by the **assets** query. 

## Events

```
query {
    events {type symbol from to}
}

#Events response:
{
  "data": {
    "events": []
  }
}
```

*events: [ChainEvent]*

**RToken and RABT only.** Returns data from the last 100 events of the Digitizer. Users are encouraged to issue the **events** call and follow up with a subscription to **eventsAdded.** 

## Me

```
query {
    me { userId }
}

# Me response:
{
    "data": {
        "me": {
            "userId": 1
        }
    }
}
```

*me: LoginUser*

Returns the user ID of the logged-in user. 

## Networks

```
query {
    networks { id name enabled etherscanDomain }
}

#Networks response:
{
  "data": {
    "networks": [
      {
        "id": "42",
        "name": "Jones Net"
      }
    ]
  }
}
```

*networks: [Network]*

Returns an array of the supported Ethereum networks to which you have access.

## PendingTransfers

```
query {
    pendingTransfers(assetId: "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56") 
    { assetId pendingHash from to amount }
}
```

*pendingTransfers(assetId: String): [PendingTransfer]*

**RABT only.** Returns a list of *pendingHash* strings that denote the pending transfers for a RABT (Regulated Asset-Backed Token). The value for *assetId* must match an address returned by the **assets** query.

## Protocols

```
query {
    protocols { id name enabled }
}

# Protocols response:
{
  "data": {
    "protocols": [
      {
        "id": "0",
        "name": "Ethereum",
        "enabled": true
      }
    ]
  }
}
```

*protocols: [Protocol]*

**Ethereum only.** Returns an array of the available protocols to which you have access. 

## Templates

```
query {
    templates { id name fullName description }
}

# Templates response:

whitelisted before receiving."
      },
      {
        "id": "3",
        "name": "MegaERC20",
        "fullName": "ERC20 + Mint, Burn, Pause, Reclaim",
        "description": "Best suited for company shares, and assets that appreciate"
      },
      {
        "id": "4",
        "name": "BaseERC20",
        "fullName": "ERC20 + Mint, Burn",
        "description": "Best suited for company shares"
      },
      {
        "id": "5",
        "name": "BaseERC721",
        "fullName": "ERC721 non-fungible Token",
        "description": "Best suited for individual assets or collectibles such as Art"
      },
      {
        "id": "6",
        "name": "BaseERC223",
        "fullName": "ERC223 + Mint, Burn",
        "description": "New Ethereum token standard"
      },
      {
        "id": "1",
        "name": "RTOKEN",
        "fullName": "HarborHQ R-Token",
        "description": "Best suited for ICOs and crowdsales"
      },
      {
        "id": "7",
        "name": "ERC621",
        "fullName": "ERC621 + Ownable",
        "description": "Best suited for company shares with minting/burning and owner transference"
      }
    ]
  }
}
```

*templates: [Template]*

Returns an array of ERC20 token templates supported. 

## Users

```
query {
    users { name apexUserId }
}

#Users response:
{
  "data": {
    "users": [
      {
        "name": "user1052",
        "apexUserId": 12
      },
      {
        "name": "user3606",
        "apexUserId": 11
      },
      {
        "name": "user4447",
        "apexUserId": 10
      },
      {
        "name": "user5883",
        "apexUserId": 9
      },
      {
        "name": "alphajosh",
        "apexUserId": 8
      },
      {
        "name": "pat-daskin",
        "apexUserId": 7
      },
      {
        "name": "user9516",
        "apexUserId": 6
      },
      {
        "name": "user9244",
        "apexUserId": 5
      },
      {
        "name": "demo-issuer",
        "apexUserId": 4
      },
      {
        "name": "demo-operator",
        "apexUserId": 3
      },
      {
        "name": "apadadmin",
        "apexUserId": 2
      },
      {
        "name": "admin",
        "apexUserId": 1
      }
    ]
  }
}
```

*users: [Users]*

Returns an array of the AlphaPoint user accounts available to you. 

## Version

```
query {
    version
}

#Version response:
{
  "data": {
    "version": "24.0.2"
  }
}
```

*version: String!*

Returns the current deployed version of the service

# Mutations

Mutations add data to or change data on the Blockchain.

## AllowTransfer

```
mutation {
    allowTransfer(assetId: "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56", 
    pendinghash: "05c84513-4c92-4605-b2a0-a782d36839cf" )
}

# allowTransfer response:
To come
```

*allowTransfer(assetId: String!, pendingHash: String!): String!*

**RABT only.** Allow a pending transfer of RABT (Regulated Asset-Backed Token) denoted by the *pendingHash* parameter. The value for *assetId* must match an address returned by the **assets** query. **Required:** *assetId* and *pendinghash*.

## Burn

```
mutation {
    burn(amount: 1, contractAddress: "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56")
}

# burn response:
{
  "data": {
    "burn": "8c76a1a4-1143-4322-845a-0ccc51d13049"
  }
}
```

*burn(amount: Int!, contractAddress: String!): String!*

Burns a specified amount of tokens from your custodial account, thus decreasing the total supply. The value for *contractAddress* must match an address returned by the **assets** query. The value for *amount* is a whole number of tokens that you wish to create and add to the total supply of your asset. The **burn** mutation make take a few moments to execute. **Required:** *amount* and *contractAddress*.

## Clawback

```
mutation {
    clawback(
      clawbackaddress: "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56",
      amount: 1,
      contractAddress: "0x4B3d449442a2fdECF1bA128e562c97Bbb6AFFDa9"
    )
}

# clawback response:
To Come
```

*clawback(clawbackAddress: String!, amount: Int!, contractAddress: String!): String!*

Clawback the amount of the specified token from the *clawbackAddress* to the contract owner address. The value for *contractAddress* must match a token deployed by this server. Use the **assets** query to check. **Required:** *clawbackAddress,* *amount,* *contractAddress.* 

## Deploy

```
mutation {
    deploy(token: {
        name: "Ttest",
        symbol: "TTST",
        supply: 5,
        decimals: 2,
        cap: 8
    },
    networkId: "42", template: "MegaERC20" )
}

# deploy response:
{
  "data": {
    "deploy": "0x4B3d449442a2fdECF1bA128e562c97Bbb6AFFDa9"
  }
}
```

*deploy(token: TokenDefinition!, networkId: String!, template: String!): String!*

Deploys a new ERC token to the Ethereum blockchain. The *template* parameter must match the name value of a *Template* from the **templates** query. The *networkId* value must match the ID of a Network returned by the **networks** query. The *token* is a complex object of type Token as described in earlier this document. **Required:** *token,* *networkId,* *template.* 

## Login

```
mutation {
    login(username: "jsmith", password: "1234") { userId }
}

# login response:
{
    "data": {
        "login": {
            "userId": 1
        }
    }
}
```

*login(username: "String!", password: "String!"): LoginUser!*

Logs the specified user into the Digitizer, and returns that user's *userId,* as shown in the Login response example.

## Logout

```
mutation {
    logout
}

# logout response:
{
  "data": {
    "logout": false
  }
}
```

Logs the current user out of the Digitizer and responds with "logout": *false.* 

## Mint

```
mutation {
    mint(uuid: "912f842e-6acf-4829-a74f-1b1a768f9a1a",
    custodianAddress: "0x0fdc8ae59cc945beed8e7c71aaf1557d1bb7119a",
    amount: 5,
    contractAddress: "0x4B3d449442a2fdECF1bA128e562c97Bbb6AFFDa9")
}

# mint response:
{
  "data": {
    "mint": "912f842e-6acf-4829-a74f-1b1a768f9a1a"
  }
}
```

*mint(uuid: String!, custodianAddress: String!, amount: Int!, contractAddess: String!): String!*

Mints the specified number of tokens to your custodial account, thus increasing the total supply of your ERC tokens. The value for *contractAddress* must match an address returned by the **assets** query. The value of *custodianAddress* must be the Ethereum address in the AlphaPoint Exchange that you want to have custody of the assets. The value of *amount* is the whole number of tokens that you wish to create and add to the total supply of your asset. **Required:** *uuid*, *custodianAddress,* *amount,* *contractAddress.*

## Pause

```
mutation {
    pause(assetId: "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56" )
}

# pause response:
{
  "data": {
    "pause": "6143edb6-a396-4112-b2dc-fb14ed74cafb"
  }
}
```

*pause(assetId: String!): String!*

Pauses the specified token if the token supports pause. The value for *assetId* must match a contract address returned by the **assets** query. **Required:** *assetId.* 

## Resume

```
mutation {
    resume(assetId: "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56" )
}

# resume response:
{
  "data": {
    "resume": "5ff96e72-3c06-463f-8d88-04cf712949f8"
  }
}
```

*resume(assetId: String!,): String!*

Resumes the specified token if the token supports resuming, *and* if the token currently is paused. The value for *assetId* must match a contract address returned by the **assets** query. **Required:** *assetId.* 

## RejectTransfer

```
mutation {
    rejectTransfer(assetId: "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56", pendingHash: " ")
}

# rejectTransfer response:
{
  "data": {
    "rejectTransfer": "77a78c49-1e2f-4726-803f-db9b4eb22147"
  }
}
```

*rejectTransfer(assetId: String! pendingHash: String!): String!*

**RABT only.** Rejects a pending transfer of the RABT token denoted by the *pendingHash* parameter. The value for *assetId* must match an address returned by the **assets** query. **Required:** *assetId,* *pendingHash.*

## Transfer

```
mutation {
    transfer(
    	destinationAddress: "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56",
    	amount: 5,
    	contractAddress: "0x0fdc8ae59cc945beed8e7c71aaf1557d1bb7119a")
}

# transfer response:
{
  "data": {
    "transfer": "77a78c49-1e2f-4726-803f-db9b4eb22147"
  }
}
```

*transfer(destinationAddress: String!, amount: Int!, contractAddress: String!): String!*

Transfers an integer amount of the specified token to the *destinationAddress.* The value for *contractAddress* must match an address returned by the **assets** query. The amount is a whole number of tokens that you wish to transfer from your custodial account. **Required:** *destinationAddress,* *amount,* *contractAddress.*

## Whitelist

```
mutation {
    whitelist(address: "0xE04dA47580C5162b26371FF59DF922Af3DE0Bc56", tokenAddress: "0x0fdc8ae59cc945beed8e7c71aaf1557d1bb7119a", shouldWhitelist: true )
}

# whitelist response:
{
  "data": {
    "whitelist": "2709ffec-860d-4e59-98b1-85e91a8f8a3b"
  }
}
```

*whitelist(address: String!, tokenAddress: String!, shouldWhitelist: "Boolean!"): String!*

**RTokens only.** The command whitelists an address (always permits) for sending to or receiving from an RToken transfer. The value for *contractAddress* must match an address returned by the **assets** query. You can enable or disable the whitelist address using the *shouldWhitelist* parameter. **Required:** *address,* *tokenAddress,* *shouldWhitelist.*

# Subscriptions

A subscription pushes data from the server to applications listening for them.

## EventAdded

```
subscription {
    eventAdded { type: "whitelist", symbol: "TNBA", name: "TokenNBA" }
}
```

*eventAdded: ChainEvent!*

**RToken and RABT only.** The subscription listens to whitelist and transfer-approval events. These events are returned by ChainEvent objects.

## TxStatus

```
subscription {
    txStatus { transactionHash type status uuid confirmation requiredConfirmations data error }
}

# txStatus response:
{
    transactionHash: "2709ffec-860d-4e59-98b1-85e91a8f8a3b",
    type: "transferAllowed",
    status: "confirmationEvent",
    uuid: "c27f1459-53d2-4f33-92cc-790c81e5019e",
    confirmation: 11,
    requiredConfirmations: 12,
    data: "",
    error: ""
}

```

*txStatus: TxStatus!*

Subscribes the user to monitoring the various states of a single user-executed transaction on the Blockchain. 

