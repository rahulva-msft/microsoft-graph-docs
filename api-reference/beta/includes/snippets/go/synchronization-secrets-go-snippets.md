---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphserviceprincipals "github.com/microsoftgraph/msgraph-beta-sdk-go/serviceprincipals"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphserviceprincipals.NewSynchronizationSecretKeyStringValuePair()
additionalData := map[string]interface{}{


 := graphmodels.New()
key := "BaseAddress"
.SetKey(&key) 
value := "user@domain.com"
.SetValue(&value) 
 := graphmodels.New()
key := "SecretToken"
.SetKey(&key) 
value := "password-value"
.SetValue(&value) 
 := graphmodels.New()
key := "SyncNotificationSettings"
.SetKey(&key) 
value := "{\"Enabled\":false,\"DeleteThresholdEnabled\":false}"
.SetValue(&value) 
 := graphmodels.New()
key := "SyncAll"
.SetKey(&key) 
value := "false"
.SetValue(&value) 

	value := []graphmodels.Objectable {
		,
		,
		,
		,

	}
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.ServicePrincipals().ByServicePrincipalId("servicePrincipal-id").Synchronization().Secrets().Put(context.Background(), requestBody, nil)


```