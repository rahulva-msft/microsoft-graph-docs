---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodelsediscovery "github.com/microsoftgraph/msgraph-beta-sdk-go/models/ediscovery"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodelsediscovery.NewNoncustodialDataSource()
applyHoldToSource := true
requestBody.SetApplyHoldToSource(&applyHoldToSource) 
dataSource := graphmodelsediscovery.NewDataSource()
additionalData := map[string]interface{}{
	"email" : "adelev@contoso.com", 
}
dataSource.SetAdditionalData(additionalData)
requestBody.SetDataSource(dataSource)

result, err := graphClient.Compliance().Ediscovery().Cases().ByCaseId("case-id").NoncustodialDataSources().Post(context.Background(), requestBody, nil)


```