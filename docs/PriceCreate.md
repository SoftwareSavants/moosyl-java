

# PriceCreate


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  [optional] |
|**productId** | **UUID** |  |  |
|**amount** | **Integer** |  |  |
|**interval** | [**IntervalEnum**](#IntervalEnum) |  |  |
|**active** | **Boolean** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



## Enum: IntervalEnum

| Name | Value |
|---- | -----|
| WEEKLY | &quot;weekly&quot; |
| MONTHLY | &quot;monthly&quot; |
| YEARLY | &quot;yearly&quot; |



