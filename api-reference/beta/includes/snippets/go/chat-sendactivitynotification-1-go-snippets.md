---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphchats "github.com/microsoftgraph/msgraph-beta-sdk-go/chats"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphchats.NewSendActivityNotificationPostRequestBody()
topic := graphmodels.NewTeamworkActivityTopic()
source := graphmodels.ENTITYURL_TEAMWORKACTIVITYTOPICSOURCE 
topic.SetSource(&source) 
value := "https://graph.microsoft.com/beta/chats/{chatId}"
topic.SetValue(&value) 
requestBody.SetTopic(topic)
activityType := "taskCreated"
requestBody.SetActivityType(&activityType) 
previewText := graphmodels.NewItemBody()
content := "New Task Created"
previewText.SetContent(&content) 
requestBody.SetPreviewText(previewText)
recipient := graphmodels.NewTeamworkNotificationRecipient()
additionalData := map[string]interface{}{
	"userId" : "569363e2-4e49-4661-87f2-16f245c5d66a", 
}
recipient.SetAdditionalData(additionalData)
requestBody.SetRecipient(recipient)


keyValuePair := graphmodels.NewKeyValuePair()
name := "taskId"
keyValuePair.SetName(&name) 
value := "Task 12322"
keyValuePair.SetValue(&value) 

templateParameters := []graphchats.KeyValuePairable {
	keyValuePair,

}
requestBody.SetTemplateParameters(templateParameters)

graphClient.Chats().ByChatId("chat-id").SendActivityNotification().Post(context.Background(), requestBody, nil)


```