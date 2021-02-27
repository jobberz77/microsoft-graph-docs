---
title: "Update connectionOperation"
description: "Update the properties of a connectionOperation object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update connectionOperation
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [connectionOperation](../resources/connectionoperation.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /connectionOperation
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [connectionOperation](../resources/connectionoperation.md) object.

The following table shows the properties that are required when you update the [connectionOperation](../resources/connectionoperation.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|status|connectionOperationStatus|**TODO: Add Description**. Possible values are: `unspecified`, `inprogress`, `completed`, `failed`.|
|error|[publicError](../resources/synchronization-publicerror.md)|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [connectionOperation](../resources/connectionoperation.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_connectionoperation"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/connectionOperation
Content-Type: application/json
Content-length: 154

{
  "@odata.type": "#microsoft.graph.connectionOperation",
  "status": "String",
  "error": {
    "@odata.type": "microsoft.graph.publicError"
  }
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.connectionOperation",
  "id": "03088408-8408-0308-0884-080308840803",
  "status": "String",
  "error": {
    "@odata.type": "microsoft.graph.publicError"
  }
}
```
