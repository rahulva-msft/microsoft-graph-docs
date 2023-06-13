---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphteamwork "github.com/microsoftgraph/msgraph-sdk-go/teamwork"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphteamwork.NewSendActivityNotificationToRecipientsPostRequestBody()
topic := graphmodels.NewTeamworkActivityTopic()
source := graphmodels.ENTITYURL_TEAMWORKACTIVITYTOPICSOURCE 
topic.SetSource(&source) 
value := "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps/{teamsAppId}"
topic.SetValue(&value) 
requestBody.SetTopic(topic)
activityType := "pendingFinanceApprovalRequests"
requestBody.SetActivityType(&activityType) 
previewText := graphmodels.NewItemBody()
content := "Internal spending team has a pending finance approval requests"
previewText.SetContent(&content) 
requestBody.SetPreviewText(previewText)


teamworkNotificationRecipient := graphmodels.NewTeamworkNotificationRecipient()
additionalData := map[string]interface{}{
	"userId" : "569363e2-4e49-4661-87f2-16f245c5d66a", 
}
teamworkNotificationRecipient.SetAdditionalData(additionalData)
teamworkNotificationRecipient1 := graphmodels.NewTeamworkNotificationRecipient()
additionalData := map[string]interface{}{
	"userId" : "ab88234e-0874-477c-9638-d144296ed04f", 
}
teamworkNotificationRecipient1.SetAdditionalData(additionalData)
teamworkNotificationRecipient2 := graphmodels.NewTeamworkNotificationRecipient()
additionalData := map[string]interface{}{
	"userId" : "01c64f53-69aa-42c7-9b7f-9f75195d6bfc", 
}
teamworkNotificationRecipient2.SetAdditionalData(additionalData)

recipients := []graphteamwork.TeamworkNotificationRecipientable {
	teamworkNotificationRecipient,
	teamworkNotificationRecipient1,
	teamworkNotificationRecipient2,

}
requestBody.SetRecipients(recipients)


keyValuePair := graphmodels.NewKeyValuePair()
name := "pendingRequestCount"
keyValuePair.SetName(&name) 
value := "5"
keyValuePair.SetValue(&value) 

templateParameters := []graphteamwork.KeyValuePairable {
	keyValuePair,

}
requestBody.SetTemplateParameters(templateParameters)

graphClient.Teamwork().SendActivityNotificationToRecipients().Post(context.Background(), requestBody, nil)


```