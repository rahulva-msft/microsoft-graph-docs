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


requestBody := graphmodels.NewExtension()
additionalData := map[string]interface{}{
	"extensionName" : "com.contoso.roamingSettings", 
	"theme" : "dark", 
	"color" : "purple", 
	"lang" : "Japanese", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().Extensions().Post(context.Background(), requestBody, nil)


```