---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphdevicemanagement "github.com/microsoftgraph/msgraph-beta-sdk-go/devicemanagement"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphdevicemanagement.NewAssignPostRequestBody()


cloudPcProvisioningPolicyAssignment := graphmodels.NewCloudPcProvisioningPolicyAssignment()
id := "b0c2d35f-3385-46c8-a6f5-6c3dfad7708b_64ff06de-9c00-4a5a-98b5-7f5abe26ffff"
cloudPcProvisioningPolicyAssignment.SetId(&id) 
target := graphmodels.NewCloudPcManagementAssignmentTarget()
additionalData := map[string]interface{}{
	"groupId" : "64ff06de-9c00-4a5a-98b5-7f5abe26ffff", 
}
target.SetAdditionalData(additionalData)
cloudPcProvisioningPolicyAssignment.SetTarget(target)

assignments := []graphdevicemanagement.Objectable {
	cloudPcProvisioningPolicyAssignment,

}
requestBody.SetAssignments(assignments)
additionalData := map[string]interface{}{
}
requestBody.SetAdditionalData(additionalData)

graphClient.DeviceManagement().VirtualEndpoint().ProvisioningPolicies().ByProvisioningPolicieId("cloudPcProvisioningPolicy-id").Assign().Post(context.Background(), requestBody, nil)


```