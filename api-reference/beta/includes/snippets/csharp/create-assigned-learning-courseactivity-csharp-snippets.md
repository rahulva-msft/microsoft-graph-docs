---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new LearningCourseActivity
{
	OdataType = "#microsoft.graph.learningAssignment",
	CompletedDateTime = null,
	CompletionPercentage = 20,
	ExternalCourseActivityId = "12a2228a-e020-11ec-9d64-0242ac120002",
	LearningContentId = "57baf9dc-e020-11ec-9d64-0242ac120002",
	LearningProviderId = "01e8f81b-3060-4dec-acf0-0389665a0a38",
	LearnerUserId = "7ba2228a-e020-11ec-9d64-0242ac120002",
	Status = CourseStatus.NotStarted,
	AdditionalData = new Dictionary<string, object>
	{
		{
			"assignedDateTime" , "2021-05-11T22:57:17+00:00"
		},
		{
			"assignmentType" , "required"
		},
		{
			"assignerUserId" , "cea1684d-57dc-438d-a9d1-e666ec1a7f3d"
		},
		{
			"dueDateTime" , new 
			{
				DateTime = "2022-09-22T16:05:00.0000000",
				TimeZone = "UTC",
			}
		},
		{
			"notes" , new 
			{
				ContentType = "text",
				Content = "required assignment added for user",
			}
		},
	},
};
var result = await graphClient.EmployeeExperience.LearningProviders["{learningProvider-id}"].LearningCourseActivities.PostAsync(requestBody);


```