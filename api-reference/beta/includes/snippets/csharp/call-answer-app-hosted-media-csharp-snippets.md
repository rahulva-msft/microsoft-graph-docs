---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Microsoft.Graph.Beta.Communications.Calls.Item.Answer.AnswerPostRequestBody
{
	CallbackUri = "https://bot.contoso.com/api/calls",
	AcceptedModalities = new List<Modality?>
	{
		Modality.Audio,
	},
	MediaConfig = new MediaConfig
	{
		OdataType = "#microsoft.graph.appHostedMediaConfig",
		AdditionalData = new Dictionary<string, object>
		{
			{
				"blob" , "<Media Session Configuration Blob>"
			},
		},
	},
};
await graphClient.Communications.Calls["{call-id}"].Answer.PostAsync(requestBody);


```