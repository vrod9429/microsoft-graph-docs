---
title: "Update alert"
description: "Update the properties of alert object."
localization_priority: Normal
author: ""
ms.prod: ""
doc_type: "apiPageType"
---

# Update alert

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of alert object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
|:---------------------------------------|:--------------------------------------------|
| Delegated (work or school account)     | Not supported. |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Not supported. |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
PATCH /Security/alerts/{id}
```

## Request headers

| Name       | Description|
|:-----------|:-----------|
| Authorization | Bearer {code} |

## Request body

In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance, don't include existing values that haven't changed.

| Property     | Type        | Description |
|:-------------|:------------|:------------|
|activityGroupName|String||
|assignedTo|String||
|azureSubscriptionId|String||
|azureTenantId|String||
|category|String||
|closedDateTime|DateTimeOffset||
|cloudAppStates|cloudAppSecurityState collection||
|comments|String collection||
|confidence|Int32||
|createdDateTime|DateTimeOffset||
|description|String||
|detectionIds|String collection||
|eventDateTime|DateTimeOffset||
|feedback|string| Possible values are: `unknown`, `truePositive`, `falsePositive`, `benignPositive`, `unknownFutureValue`.|
|fileStates|fileSecurityState collection||
|historyStates|alertHistoryState collection||
|hostStates|hostSecurityState collection||
|lastModifiedDateTime|DateTimeOffset||
|malwareStates|malwareState collection||
|networkConnections|networkConnection collection||
|processes|process collection||
|recommendedActions|String collection||
|registryKeyStates|registryKeyState collection||
|severity|string| Possible values are: `unknown`, `informational`, `low`, `medium`, `high`, `unknownFutureValue`.|
|sourceMaterials|String collection||
|status|string| Possible values are: `unknown`, `newAlert`, `inProgress`, `resolved`, `dismissed`, `unknownFutureValue`.|
|tags|String collection||
|title|String||
|triggers|alertTrigger collection||
|userStates|userSecurityState collection||
|vendorInformation|securityVendorInformation||
|vulnerabilityStates|vulnerabilityState collection||

## Response

If successful, this method returns a `200 OK` response code and an updated [alert](../resources/alert.md) object in the response body.

## Examples

### Request

The following is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/beta/Security/alerts/{id}
Content-type: application/json

{
  "activityGroupName": "activityGroupName-value",
  "assignedTo": "assignedTo-value",
  "azureSubscriptionId": "azureSubscriptionId-value",
  "azureTenantId": "azureTenantId-value",
  "category": "category-value",
  "closedDateTime": "datetime-value"
}
```

### Response

The following is an example of the response.

> [!NOTE]
> The response object shown here might be shortened for readability. All the properties will be returned from an actual call.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "activityGroupName": "activityGroupName-value",
  "assignedTo": "assignedTo-value",
  "azureSubscriptionId": "azureSubscriptionId-value",
  "azureTenantId": "azureTenantId-value",
  "category": "category-value",
  "closedDateTime": "datetime-value"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update alert",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->