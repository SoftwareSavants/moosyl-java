

# SubscriptionGetData


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  |
|**organizationId** | **UUID** |  |  |
|**customerId** | **UUID** |  |  |
|**priceId** | **UUID** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**nextBillingDate** | **OffsetDateTime** |  |  |
|**startedAt** | **OffsetDateTime** |  |  |
|**cancelledAt** | **OffsetDateTime** |  |  |
|**expiresAt** | **OffsetDateTime** |  |  |



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



