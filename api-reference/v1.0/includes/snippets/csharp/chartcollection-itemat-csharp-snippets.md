---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Microsoft.Graph.Drives.Item.Items.Item.Workbook.Worksheets.Item.Charts.Item.Chart
{
	AdditionalData = new Dictionary<string, object>
	{
		{
			"index" , 8
		},
	},
};
await graphClient.Drives["{drive-id}"].Items["{driveItem-id}"].Workbook.Worksheets["{workbookWorksheet-id}"].Charts["{workbookChart-id}"].PostAsync(requestBody);


```