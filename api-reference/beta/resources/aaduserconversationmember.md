---
title: "aadUserConversationMember resource type"
description: "Represents a user in a conversation."
localization_priority: Priority
author: "nkramer"
ms.prod: "microsoft-teams"
---

# aadUserConversationMember resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents an Azure Active Directory user in a [chat](chat.md). 
This type inherits from [conversationMember](conversationmember.md).

## Methods

| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|[List Chat members](../api/conversationmember-list.md) | [conversationmember](conversationmember.md) collection | Get the list of all users in the chat.|
|[Get Chat member](../api/conversationmember-get.md) | [conversationmember](conversationmember.md) | Get a single user in the chat.|

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|id|String| Read-only. Unique ID of the user.|
|displayName| string | The display name of the user. |
|roles| string collection | The roles for that user. |
|userId| string | The guid of the user. |
|email| string  | The email address of the user. |

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.aadUserConversationMember"
}-->

```json
{
  "id": "string (identifier)",
  "displayName" : "string",
  "roles" : ["string"],
  "userId" : "string",
  "email" : "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "aadUserConversationMember",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
