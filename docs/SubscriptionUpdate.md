

# SubscriptionUpdate


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**priceId** | **UUID** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**nextBillingDate** | **OffsetDateTime** |  |  [optional] |
|**cancelledAt** | **OffsetDateTime** |  |  [optional] |
|**expiresAt** | **OffsetDateTime** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| TRIALING | &quot;trialing&quot; |
| ACTIVE | &quot;active&quot; |
| PAST_DUE | &quot;past_due&quot; |
| PAUSED | &quot;paused&quot; |
| CANCELLED | &quot;cancelled&quot; |
| EXPIRED | &quot;expired&quot; |
| PENDING_CANCELLATION | &quot;pending_cancellation&quot; |



