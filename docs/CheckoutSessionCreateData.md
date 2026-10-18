

# CheckoutSessionCreateData


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  |
|**paymentRequestId** | **UUID** |  |  |
|**environmentId** | **UUID** |  |  |
|**selectedConfigurationId** | **UUID** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**successUrl** | **String** |  |  |
|**cancelUrl** | **String** |  |  |
|**expiresAt** | **OffsetDateTime** |  |  |
|**completedAt** | **OffsetDateTime** |  |  |
|**createdAt** | **OffsetDateTime** |  |  |
|**updatedAt** | **OffsetDateTime** |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| OPEN | &quot;open&quot; |
| COMPLETED | &quot;completed&quot; |
| EXPIRED | &quot;expired&quot; |
| CANCELLED | &quot;cancelled&quot; |



