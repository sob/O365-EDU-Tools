# List resources

List the resources associated with this submission.  The submissionResource object is a wrapper around the actual resource object the student is working on.  The wrapper also includes a pointer to the resource on the assignment if this was copied from the assignment during the assign process.  These resources should considered the "working" copy of the resources while the submittedResources are the resources that have been officially submitted to be graded.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  EduAssignments.ReadBasic, EduAssignments.ReadWriteBasic, EduAssignments.Read, EduAssignments.ReadWrite  |
|Delegated (personal Microsoft account) | Not supported.   |
|Application | Not supported. | 

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /educationClasses/assignments/<id>/submissions/<id>/resources
```
## Optional query parameters
This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.

## Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |

## Request body
Do not supply a request body for this method.
## Response
If successful, this method returns a `200 OK` response code and collection of [educationSubmissionResource](../resources/educationsubmissionresource.md) objects in the response body.
## Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_resources"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/<id>/assignments/<id>/submissions/<id>/resources
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSubmissionResource",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1045

{
  "value": [
    {
      "resource": {
        "displayName": "displayName-value",
        "createdDateTime": "datetime-value",
        "createdBy": {
          "application": {
            "displayName": "displayName-value",
            "id": "id-value"
          },
          "device": {
            "displayName": "displayName-value",
            "id": "id-value"
          },
          "user": {
            "displayName": "displayName-value",
            "id": "id-value"
          }
        },
        "lastModifiedDateTime": "datetime-value",
        "lastModifiedBy": {
          "application": {
            "displayName": "displayName-value",
            "id": "id-value"
          },
          "device": {
            "displayName": "displayName-value",
            "id": "id-value"
          },
          "user": {
            "displayName": "displayName-value",
            "id": "id-value"
          }
        }
      },
      "assignmentResource": {
        "@odataid": "odataid-value"
      },
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List resources",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->