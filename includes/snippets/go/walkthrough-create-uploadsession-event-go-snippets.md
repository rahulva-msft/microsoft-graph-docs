---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphusers "github.com/microsoftgraph/msgraph-sdk-go/users"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphusers.NewCreateUploadSessionPostRequestBody()
attachmentItem := graphmodels.NewAttachmentItem()
attachmentType := graphmodels.FILE_ATTACHMENTTYPE 
attachmentItem.SetAttachmentType(&attachmentType) 
name := "flower"
attachmentItem.SetName(&name) 
size := int64(3483322)
attachmentItem.SetSize(&size) 
requestBody.SetAttachmentItem(attachmentItem)

result, err := graphClient.Me().Events().ByEventId("event-id").Attachments().CreateUploadSession().Post(context.Background(), requestBody, nil)


```