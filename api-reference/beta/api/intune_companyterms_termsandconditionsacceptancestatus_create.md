﻿# Create termsAndConditionsAcceptanceStatus
Create a new [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md) object.
### Prerequisites
One of the following **scopes** is required to execute this API:

*DeviceManagementServiceConfiguration.ReadWrite.All*
### HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
```http
POST /termsAndConditions/<id>/acceptanceStatuses/<id>
```

### Request headers
|Header|Value|
|---|---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

### Request body
In the request body, supply a JSON representation of a termsAndConditionsAcceptanceStatus object.
The following table shows the properties that are required when you create a termsAndConditionsAcceptanceStatus.

|Property|Type|Description|
|---|---|---|
|id|String|Key of the entity.|
|userDisplayName|String|The name of the user that this acceptance status is for.|
|acceptedVersion|Int32|The version of the terms that were accepted. 0 if never accepted.|
|acceptedDateTime|DateTimeOffset|The date and time that the terms were accepted.|



### Response
If successful, this method returns a `201 Created` response code and a [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md) object in the response body.

### Example
##### Request
Here is an example of the request.
```http
POST https://graph.microsoft.com/beta/termsAndConditions/<id>/acceptanceStatuses/<id>
Content-type: application/json
Content-length: 211

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "userDisplayName": "User Display Name value",
  "acceptedVersion": 15,
  "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
}
```

##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
```http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 260

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "id": "a045ce1a-ce1a-a045-1ace-45a01ace45a0",
  "userDisplayName": "User Display Name value",
  "acceptedVersion": 15,
  "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
}
```



