---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewMailFolder()
additionalData := map[string]interface{}{
	"filterQuery" : "contains(subject, 'Analytics')", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().MailFolders().ByMailFolderId("mailFolder-id").Patch(context.Background(), requestBody, nil)


```