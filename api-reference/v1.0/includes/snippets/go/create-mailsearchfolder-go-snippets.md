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
displayName := "Weekly digests"
requestBody.SetDisplayName(&displayName) 
additionalData := map[string]interface{}{
	includeNestedFolders := true
requestBody.SetIncludeNestedFolders(&includeNestedFolders) 
	sourceFolderIds := []string {
		"AQMkADYAAAIBDAAAAA==",

	}
	"filterQuery" : "contains(subject, 'weekly digest')", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().MailFolders().ByMailFolderId("mailFolder-id").ChildFolders().Post(context.Background(), requestBody, nil)


```