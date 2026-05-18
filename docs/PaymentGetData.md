

# PaymentGetData


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  |
|**amount** | **Integer** |  |  |
|**phoneNumber** | **String** |  |  |
|**passCode** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**environmentId** | **UUID** |  |  |
|**paymentRequestId** | **UUID** |  |  |
|**configurationId** | **UUID** |  |  |
|**referenceId** | **String** |  |  |
|**metadata** | **Object** |  |  |
|**payoutId** | **UUID** |  |  |
|**completedAt** | **OffsetDateTime** |  |  |
|**createdAt** | **OffsetDateTime** |  |  |
|**updatedAt** | **OffsetDateTime** |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| COMPLETED | &quot;completed&quot; |
| FAILED | &quot;failed&quot; |
| CANCELLED | &quot;cancelled&quot; |



