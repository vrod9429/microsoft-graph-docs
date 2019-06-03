---
title: "room resource type"
description: "Specifies the properties of a room in a tenant."
localization_priority: Normal
author: "vrod9429"
ms.prod: "outlook"
doc_type: "resourcePageType"
---

# room resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a room.

Derived from [place](place.md).

## Methods

| Method                              | Return Type                  | Description |
|:------------------------------------|:-----------------------------|:--------|
| [List places](../api/place-list.md) | [place](place.md) collection | Retrieve a list of place objects. |
| [Get place](../api/place-get.md)    | [place](place.md)            | Retrieve the properties and relationships of a place object. |

## Properties

| Property               | Type                                              | Description |
|:-----------------------|:--------------------------------------------------|:--|
| address                | [physicalAddress](physicaladdress.md)             | The address of the room. |
| audioDeviceName        | String                                            | Specifies the name of the audio device in the room. |
| bookingType            | [bookingType](#bookingtype-values)                | Type of room. Possible values are `standard`, `managed`, and `reserved`. |
| building               | String                                            | Specifies the building name or building number that the room is in. |
| capacity               | String                                            | Specifies the capacity of the room. |
| displayName            | String                                            | The name associated with the room. |
| displayDeviceName      | String                                            | Specifies the name of the display device in the room. |
| emailAddress           | String                                            | Email address of the room. |
| floorNumber            | Int32                                             | Specifies the floor number that the room is on. |
| geoCoordinates         | [outlookGeoCoordinates](outlookgeocoordinates.md) | Specifies the room location in latitude, longitude and (optionally) altitude coordinates. |
| id                     | String                                            | Unique identifier for the room. Read-only. |
| isWheelchairAccessible | Boolean                                           | Specifies whether the room is wheelchair accessible. |
| label                  | String                                            | Specifies a descriptive label for the room (for example, a number or name). |
| nickname               | String                                            | Specifies a nickname for the room (for example, conf room). |
| phone                  | String                                            | The phone number of the room. |
| tags                   | String collection                                 | Specifies additional features of the room (for example, details like the type of view or furniture type). |
| videoDeviceName        | String                                            | Specifies the name of the video device in the room. |

### bookingType values

| Value    | Description                                               |
|:---------|:----------------------------------------------------------|
| standard | The room can be reserved based on the other settings in this cmdlet. This is the default value. |
| managed  | The room is managed by a delegate                         |
| reserved | The room can't be reserved.                               |

## Relationships

None

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.room",
  "baseType": ""
}-->

```json
{
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "audioDeviceName": "String",
  "bookingType": "String",
  "building": "String",
  "capacity": "String",
  "displayName": "String",
  "displayDeviceName": "String",
  "emailAddress": "String",
  "floorNumber": 1024,
  "geoCoordinates": {"@odata.type": "microsoft.graph.outlookGeoCoordinates"},
  "id": "String (identifier)",
  "isWheelchairAccessible": true,
  "label": "String",
  "nickname": "String",
  "phone": "String",
  "tags": ["String"],
  "videoDeviceName": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "room resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->