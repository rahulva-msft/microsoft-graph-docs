---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestConfiguration = new AppConsentRequestRequestBuilderGetRequestConfiguration();
$queryParameters = AppConsentRequestRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->filter = "userConsentRequests/any(u:u/status eq 'InProgress')";
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->identityGovernance()->appConsent()->appConsentRequests()->byAppConsentRequestId('appConsentRequest-id')->get($requestConfiguration);


```