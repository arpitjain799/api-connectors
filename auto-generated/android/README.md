# swagger-android-client

## Requirements

Building the API client library requires [Maven](https://maven.apache.org/) to be installed.

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn deploy
```

Refer to the [official documentation](https://maven.apache.org/plugins/maven-deploy-plugin/usage.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
    <groupId>io.swagger</groupId>
    <artifactId>swagger-android-client</artifactId>
    <version>1.0.0</version>
    <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "io.swagger:swagger-android-client:1.0.0"
```

### Others

At first generate the JAR by executing:

    mvn package

Then manually install the following JARs:

* target/swagger-android-client-1.0.0.jar
* target/lib/*.jar

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import io.swagger.client.api.APIKeyApi;

public class APIKeyApiExample {

    public static void main(String[] args) {
        APIKeyApi apiInstance = new APIKeyApi();
        Boolean reverse = false; // Boolean | If true, will sort results newest first.
        try {
            List<APIKey> result = apiInstance.aPIKeyGet(reverse);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling APIKeyApi#aPIKeyGet");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://www.bitmex.com/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*APIKeyApi* | [**aPIKeyGet**](docs/APIKeyApi.md#aPIKeyGet) | **GET** /apiKey | Get your API Keys.
*AnnouncementApi* | [**announcementGet**](docs/AnnouncementApi.md#announcementGet) | **GET** /announcement | Get site announcements.
*AnnouncementApi* | [**announcementGetUrgent**](docs/AnnouncementApi.md#announcementGetUrgent) | **GET** /announcement/urgent | Get urgent (banner) announcements.
*ChatApi* | [**chatGet**](docs/ChatApi.md#chatGet) | **GET** /chat | Get chat messages.
*ChatApi* | [**chatGetChannels**](docs/ChatApi.md#chatGetChannels) | **GET** /chat/channels | Get available channels.
*ChatApi* | [**chatGetConnected**](docs/ChatApi.md#chatGetConnected) | **GET** /chat/connected | Get connected users.
*ChatApi* | [**chatNew**](docs/ChatApi.md#chatNew) | **POST** /chat | Send a chat message.
*ExecutionApi* | [**executionGet**](docs/ExecutionApi.md#executionGet) | **GET** /execution | Get all raw executions for your account.
*ExecutionApi* | [**executionGetTradeHistory**](docs/ExecutionApi.md#executionGetTradeHistory) | **GET** /execution/tradeHistory | Get all balance-affecting executions. This includes each trade, insurance charge, and settlement.
*FundingApi* | [**fundingGet**](docs/FundingApi.md#fundingGet) | **GET** /funding | Get funding history.
*GlobalNotificationApi* | [**globalNotificationGet**](docs/GlobalNotificationApi.md#globalNotificationGet) | **GET** /globalNotification | Get your current GlobalNotifications.
*InstrumentApi* | [**instrumentGet**](docs/InstrumentApi.md#instrumentGet) | **GET** /instrument | Get instruments.
*InstrumentApi* | [**instrumentGetActive**](docs/InstrumentApi.md#instrumentGetActive) | **GET** /instrument/active | Get all active instruments and instruments that have expired in &lt;24hrs.
*InstrumentApi* | [**instrumentGetActiveAndIndices**](docs/InstrumentApi.md#instrumentGetActiveAndIndices) | **GET** /instrument/activeAndIndices | Helper method. Gets all active instruments and all indices. This is a join of the result of /indices and /active.
*InstrumentApi* | [**instrumentGetActiveIntervals**](docs/InstrumentApi.md#instrumentGetActiveIntervals) | **GET** /instrument/activeIntervals | Return all active contract series and interval pairs.
*InstrumentApi* | [**instrumentGetCompositeIndex**](docs/InstrumentApi.md#instrumentGetCompositeIndex) | **GET** /instrument/compositeIndex | Show constituent parts of an index.
*InstrumentApi* | [**instrumentGetIndices**](docs/InstrumentApi.md#instrumentGetIndices) | **GET** /instrument/indices | Get all price indices.
*InsuranceApi* | [**insuranceGet**](docs/InsuranceApi.md#insuranceGet) | **GET** /insurance | Get insurance fund history.
*LeaderboardApi* | [**leaderboardGet**](docs/LeaderboardApi.md#leaderboardGet) | **GET** /leaderboard | Get current leaderboard.
*LeaderboardApi* | [**leaderboardGetName**](docs/LeaderboardApi.md#leaderboardGetName) | **GET** /leaderboard/name | Get your alias on the leaderboard.
*LiquidationApi* | [**liquidationGet**](docs/LiquidationApi.md#liquidationGet) | **GET** /liquidation | Get liquidation orders.
*OrderApi* | [**orderAmend**](docs/OrderApi.md#orderAmend) | **PUT** /order | Amend the quantity or price of an open order.
*OrderApi* | [**orderCancel**](docs/OrderApi.md#orderCancel) | **DELETE** /order | Cancel order(s). Send multiple order IDs to cancel in bulk.
*OrderApi* | [**orderCancelAll**](docs/OrderApi.md#orderCancelAll) | **DELETE** /order/all | Cancels all of your orders.
*OrderApi* | [**orderCancelAllAfter**](docs/OrderApi.md#orderCancelAllAfter) | **POST** /order/cancelAllAfter | Automatically cancel all your orders after a specified timeout.
*OrderApi* | [**orderClosePosition**](docs/OrderApi.md#orderClosePosition) | **POST** /order/closePosition | Close a position. [Deprecated, use POST /order with execInst: &#39;Close&#39;]
*OrderApi* | [**orderGetOrders**](docs/OrderApi.md#orderGetOrders) | **GET** /order | Get your orders.
*OrderApi* | [**orderNew**](docs/OrderApi.md#orderNew) | **POST** /order | Create a new order.
*OrderBookApi* | [**orderBookGetL2**](docs/OrderBookApi.md#orderBookGetL2) | **GET** /orderBook/L2 | Get current orderbook in vertical format.
*PositionApi* | [**positionGet**](docs/PositionApi.md#positionGet) | **GET** /position | Get your positions.
*PositionApi* | [**positionIsolateMargin**](docs/PositionApi.md#positionIsolateMargin) | **POST** /position/isolate | Enable isolated margin or cross margin per-position.
*PositionApi* | [**positionTransferIsolatedMargin**](docs/PositionApi.md#positionTransferIsolatedMargin) | **POST** /position/transferMargin | Transfer equity in or out of a position.
*PositionApi* | [**positionUpdateLeverage**](docs/PositionApi.md#positionUpdateLeverage) | **POST** /position/leverage | Choose leverage for a position.
*PositionApi* | [**positionUpdateRiskLimit**](docs/PositionApi.md#positionUpdateRiskLimit) | **POST** /position/riskLimit | Update your risk limit.
*QuoteApi* | [**quoteGet**](docs/QuoteApi.md#quoteGet) | **GET** /quote | Get Quotes.
*QuoteApi* | [**quoteGetBucketed**](docs/QuoteApi.md#quoteGetBucketed) | **GET** /quote/bucketed | Get previous quotes in time buckets.
*SchemaApi* | [**schemaGet**](docs/SchemaApi.md#schemaGet) | **GET** /schema | Get model schemata for data objects returned by this API.
*SchemaApi* | [**schemaWebsocketHelp**](docs/SchemaApi.md#schemaWebsocketHelp) | **GET** /schema/websocketHelp | Returns help text &amp; subject list for websocket usage.
*SettlementApi* | [**settlementGet**](docs/SettlementApi.md#settlementGet) | **GET** /settlement | Get settlement history.
*StatsApi* | [**statsGet**](docs/StatsApi.md#statsGet) | **GET** /stats | Get exchange-wide and per-series turnover and volume statistics.
*StatsApi* | [**statsHistory**](docs/StatsApi.md#statsHistory) | **GET** /stats/history | Get historical exchange-wide and per-series turnover and volume statistics.
*StatsApi* | [**statsHistoryUSD**](docs/StatsApi.md#statsHistoryUSD) | **GET** /stats/historyUSD | Get a summary of exchange statistics in USD.
*TradeApi* | [**tradeGet**](docs/TradeApi.md#tradeGet) | **GET** /trade | Get Trades.
*TradeApi* | [**tradeGetBucketed**](docs/TradeApi.md#tradeGetBucketed) | **GET** /trade/bucketed | Get previous trades in time buckets.
*UserApi* | [**userCancelWithdrawal**](docs/UserApi.md#userCancelWithdrawal) | **POST** /user/cancelWithdrawal | Cancel a withdrawal.
*UserApi* | [**userCheckReferralCode**](docs/UserApi.md#userCheckReferralCode) | **GET** /user/checkReferralCode | Check if a referral code is valid.
*UserApi* | [**userCommunicationToken**](docs/UserApi.md#userCommunicationToken) | **POST** /user/communicationToken | Register your communication token for mobile clients
*UserApi* | [**userConfirm**](docs/UserApi.md#userConfirm) | **POST** /user/confirmEmail | Confirm your email address with a token.
*UserApi* | [**userConfirmWithdrawal**](docs/UserApi.md#userConfirmWithdrawal) | **POST** /user/confirmWithdrawal | Confirm a withdrawal.
*UserApi* | [**userGet**](docs/UserApi.md#userGet) | **GET** /user | Get your user model.
*UserApi* | [**userGetAffiliateStatus**](docs/UserApi.md#userGetAffiliateStatus) | **GET** /user/affiliateStatus | Get your current affiliate/referral status.
*UserApi* | [**userGetCommission**](docs/UserApi.md#userGetCommission) | **GET** /user/commission | Get your account&#39;s commission status.
*UserApi* | [**userGetDepositAddress**](docs/UserApi.md#userGetDepositAddress) | **GET** /user/depositAddress | Get a deposit address.
*UserApi* | [**userGetExecutionHistory**](docs/UserApi.md#userGetExecutionHistory) | **GET** /user/executionHistory | Get the execution history by day.
*UserApi* | [**userGetMargin**](docs/UserApi.md#userGetMargin) | **GET** /user/margin | Get your account&#39;s margin status. Send a currency of \&quot;all\&quot; to receive an array of all supported currencies.
*UserApi* | [**userGetQuoteFillRatio**](docs/UserApi.md#userGetQuoteFillRatio) | **GET** /user/quoteFillRatio | Get 7 days worth of Quote Fill Ratio statistics.
*UserApi* | [**userGetWallet**](docs/UserApi.md#userGetWallet) | **GET** /user/wallet | Get your current wallet information.
*UserApi* | [**userGetWalletHistory**](docs/UserApi.md#userGetWalletHistory) | **GET** /user/walletHistory | Get a history of all of your wallet transactions (deposits, withdrawals, PNL).
*UserApi* | [**userGetWalletSummary**](docs/UserApi.md#userGetWalletSummary) | **GET** /user/walletSummary | Get a summary of all of your wallet transactions (deposits, withdrawals, PNL).
*UserApi* | [**userLogout**](docs/UserApi.md#userLogout) | **POST** /user/logout | Log out of BitMEX.
*UserApi* | [**userMinWithdrawalFee**](docs/UserApi.md#userMinWithdrawalFee) | **GET** /user/minWithdrawalFee | Get the minimum withdrawal fee for a currency.
*UserApi* | [**userRequestWithdrawal**](docs/UserApi.md#userRequestWithdrawal) | **POST** /user/requestWithdrawal | Request a withdrawal to an external wallet.
*UserApi* | [**userSavePreferences**](docs/UserApi.md#userSavePreferences) | **POST** /user/preferences | Save user preferences.
*UserEventApi* | [**userEventGet**](docs/UserEventApi.md#userEventGet) | **GET** /userEvent | Get your user events


## Documentation for Models

 - [APIKey](docs/APIKey.md)
 - [AccessToken](docs/AccessToken.md)
 - [Affiliate](docs/Affiliate.md)
 - [Announcement](docs/Announcement.md)
 - [Chat](docs/Chat.md)
 - [ChatChannel](docs/ChatChannel.md)
 - [CommunicationToken](docs/CommunicationToken.md)
 - [ConnectedUsers](docs/ConnectedUsers.md)
 - [Error](docs/Error.md)
 - [ErrorError](docs/ErrorError.md)
 - [Execution](docs/Execution.md)
 - [Funding](docs/Funding.md)
 - [GlobalNotification](docs/GlobalNotification.md)
 - [IndexComposite](docs/IndexComposite.md)
 - [InlineResponse200](docs/InlineResponse200.md)
 - [Instrument](docs/Instrument.md)
 - [InstrumentInterval](docs/InstrumentInterval.md)
 - [Insurance](docs/Insurance.md)
 - [Leaderboard](docs/Leaderboard.md)
 - [Liquidation](docs/Liquidation.md)
 - [Margin](docs/Margin.md)
 - [Order](docs/Order.md)
 - [OrderBookL2](docs/OrderBookL2.md)
 - [Position](docs/Position.md)
 - [Quote](docs/Quote.md)
 - [QuoteFillRatio](docs/QuoteFillRatio.md)
 - [Settlement](docs/Settlement.md)
 - [Stats](docs/Stats.md)
 - [StatsHistory](docs/StatsHistory.md)
 - [StatsUSD](docs/StatsUSD.md)
 - [Trade](docs/Trade.md)
 - [TradeBin](docs/TradeBin.md)
 - [Transaction](docs/Transaction.md)
 - [User](docs/User.md)
 - [UserCommissionsBySymbol](docs/UserCommissionsBySymbol.md)
 - [UserEvent](docs/UserEvent.md)
 - [UserPreferences](docs/UserPreferences.md)
 - [Wallet](docs/Wallet.md)
 - [XAny](docs/XAny.md)


## Documentation for Authorization

Authentication schemes defined for the API:
### apiExpires

- **Type**: API key
- **API key parameter name**: api-expires
- **Location**: HTTP header

### apiKey

- **Type**: API key
- **API key parameter name**: api-key
- **Location**: HTTP header

### apiSignature

- **Type**: API key
- **API key parameter name**: api-signature
- **Location**: HTTP header


## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author

support@bitmex.com

