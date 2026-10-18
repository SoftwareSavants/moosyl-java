

# InvoiceGetData


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  |
|**customerId** | **UUID** |  |  |
|**organizationId** | **UUID** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**amount** | **String** |  |  |
|**dueDate** | **OffsetDateTime** |  |  |
|**paymentRequestId** | **UUID** |  |  |
|**createdAt** | **OffsetDateTime** |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| PAID | &quot;paid&quot; |
| VOID | &quot;void&quot; |
| REFUNDED | &quot;refunded&quot; |



