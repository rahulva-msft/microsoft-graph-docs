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


requestBody := graphmodels.NewPlace()
additionalData := map[string]interface{}{
	"nickname" : "Conf Room", 
	"building" : "1", 
	"label" : "100", 
	"capacity" : int32(50) , 
	isWheelChairAccessible := false
requestBody.SetIsWheelChairAccessible(&isWheelChairAccessible) 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Places().ByPlaceId("place-id").Patch(context.Background(), requestBody, nil)


```