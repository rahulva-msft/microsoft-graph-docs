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


requestBody := graphmodels.NewBookingCustomerBase()
additionalData := map[string]interface{}{
	"displayName" : "Adele", 
	"emailAddress" : "adele@relecloud.com", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Solutions().BookingBusinesses().ByBookingBusinesseId("bookingBusiness-id").Customers().ByCustomerId("bookingCustomerBase-id").Patch(context.Background(), requestBody, nil)


```