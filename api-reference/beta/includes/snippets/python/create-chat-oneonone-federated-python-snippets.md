---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

// THE PYTHON SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
client =  GraphServiceClient(request_adapter)

request_body = Chat()
request_body.chattype(ChatType.OneOnOne('chattype.oneonone'))

members_conversation_member1 = ConversationMember()
members_conversation_member1.@odata_type = '#microsoft.graph.aadUserConversationMember'

members_conversation_member1.Roles(['owner', ])

additional_data = [
'user@odata_bind' => 'https://graph.microsoft.com/v1.0/users(\'8b081ef6-4792-4def-b2c9-c363a1bf41d5\')', 
];
members_conversation_member1.additional_data(additional_data)



membersArray []= membersConversationMember1;
members_conversation_member2 = ConversationMember()
members_conversation_member2.@odata_type = '#microsoft.graph.aadUserConversationMember'

members_conversation_member2.Roles(['owner', ])

additional_data = [
'user@odata_bind' => 'https://graph.microsoft.com/v1.0/users(\'82af01c5-f7cc-4a2e-a728-3a5df21afd9d\')', 
'tenant_id' => '4dc1fe35-8ac6-4f0d-904a-7ebcd364bea1', 
];
members_conversation_member2.additional_data(additional_data)



membersArray []= membersConversationMember2;
request_body.members(membersArray)





result = await client.chats.post(request_body = request_body)


```