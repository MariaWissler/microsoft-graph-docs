---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := msgraphsdk.NewTeam()
displayName := "My Class Team"
requestBody.SetDisplayName(&displayName)
description := "My Class Team’s Description"
requestBody.SetDescription(&description)
requestBody.SetChannels( []Channel {
	msgraphsdk.NewChannel(),
displayName := "Class Announcements 📢"
	SetDisplayName(&displayName)
isFavoriteByDefault := true
	SetIsFavoriteByDefault(&isFavoriteByDefault)
	msgraphsdk.NewChannel(),
displayName := "Homework 🏋️"
	SetDisplayName(&displayName)
isFavoriteByDefault := true
	SetIsFavoriteByDefault(&isFavoriteByDefault)
}
memberSettings := msgraphsdk.NewTeamMemberSettings()
requestBody.SetMemberSettings(memberSettings)
allowCreateUpdateChannels := false
memberSettings.SetAllowCreateUpdateChannels(&allowCreateUpdateChannels)
allowDeleteChannels := false
memberSettings.SetAllowDeleteChannels(&allowDeleteChannels)
allowAddRemoveApps := false
memberSettings.SetAllowAddRemoveApps(&allowAddRemoveApps)
allowCreateUpdateRemoveTabs := false
memberSettings.SetAllowCreateUpdateRemoveTabs(&allowCreateUpdateRemoveTabs)
allowCreateUpdateRemoveConnectors := false
memberSettings.SetAllowCreateUpdateRemoveConnectors(&allowCreateUpdateRemoveConnectors)
requestBody.SetInstalledApps( []TeamsAppInstallation {
	msgraphsdk.NewTeamsAppInstallation(),
	SetAdditionalData(map[string]interface{}{
		"teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.vsts')",
	}
	msgraphsdk.NewTeamsAppInstallation(),
	SetAdditionalData(map[string]interface{}{
		"teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('1542629c-01b3-4a6d-8f76-1938b779e48d')",
	}
}
requestBody.SetAdditionalData(map[string]interface{}{
	"template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('educationClass')",
}
result, err := graphClient.Teams().Post(requestBody)


```