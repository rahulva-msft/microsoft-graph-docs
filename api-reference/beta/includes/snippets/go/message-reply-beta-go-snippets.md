---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphusers "github.com/microsoftgraph/msgraph-beta-sdk-go/users"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphusers.NewReplyPostRequestBody()
message := graphmodels.NewMessage()


recipient := graphmodels.NewRecipient()
emailAddress := graphmodels.NewEmailAddress()
address := "samanthab@contoso.onmicrosoft.com"
emailAddress.SetAddress(&address) 
name := "Samantha Booth"
emailAddress.SetName(&name) 
recipient.SetEmailAddress(emailAddress)
recipient1 := graphmodels.NewRecipient()
emailAddress := graphmodels.NewEmailAddress()
address := "randiw@contoso.onmicrosoft.com"
emailAddress.SetAddress(&address) 
name := "Randi Welch"
emailAddress.SetName(&name) 
recipient1.SetEmailAddress(emailAddress)

toRecipients := []graphmodels.Recipientable {
	recipient,
	recipient1,

}
message.SetToRecipients(toRecipients)
requestBody.SetMessage(message)
comment := "Samantha, Randi, would you name the group please?"
requestBody.SetComment(&comment) 

graphClient.Me().Messages().ByMessageId("message-id").Reply().Post(context.Background(), requestBody, nil)


```