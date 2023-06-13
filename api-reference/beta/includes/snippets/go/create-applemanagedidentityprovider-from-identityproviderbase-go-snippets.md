---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewIdentityProviderBase()
displayName := "Sign in with Apple"
requestBody.SetDisplayName(&displayName) 
additionalData := map[string]interface{}{
	"developerId" : "UBF8T346G9", 
	"serviceId" : "com.microsoft.rts.b2c.test.client", 
	"keyId" : "99P6D879C4", 
	"certificateData" : "******", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Identity().IdentityProviders().Post(context.Background(), requestBody, nil)


```