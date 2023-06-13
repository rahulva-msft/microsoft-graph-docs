---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphcommunications "github.com/microsoftgraph/msgraph-beta-sdk-go/communications"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphcommunications.NewRecordResponsePostRequestBody()
bargeInAllowed := true
requestBody.SetBargeInAllowed(&bargeInAllowed) 
clientContext := "d45324c1-fcb5-430a-902c-f20af696537c"
requestBody.SetClientContext(&clientContext) 


prompt := graphmodels.NewPrompt()
additionalData := map[string]interface{}{
mediaInfo := graphmodels.New()
uri := "https://cdn.contoso.com/beep.wav"
mediaInfo.SetUri(&uri) 
resourceId := "1D6DE2D4-CD51-4309-8DAA-70768651088E"
mediaInfo.SetResourceId(&resourceId) 
	prompt.SetMediaInfo(mediaInfo)
}
prompt.SetAdditionalData(additionalData)

prompts := []graphcommunications.Promptable {
	prompt,

}
requestBody.SetPrompts(prompts)
maxRecordDurationInSeconds := int32(10)
requestBody.SetMaxRecordDurationInSeconds(&maxRecordDurationInSeconds) 
initialSilenceTimeoutInSeconds := int32(5)
requestBody.SetInitialSilenceTimeoutInSeconds(&initialSilenceTimeoutInSeconds) 
maxSilenceTimeoutInSeconds := int32(2)
requestBody.SetMaxSilenceTimeoutInSeconds(&maxSilenceTimeoutInSeconds) 
playBeep := true
requestBody.SetPlayBeep(&playBeep) 
stopTones := []string {
	"#",
	"1",
	"*",

}
requestBody.SetStopTones(stopTones)

result, err := graphClient.Communications().Calls().ByCallId("call-id").RecordResponse().Post(context.Background(), requestBody, nil)


```