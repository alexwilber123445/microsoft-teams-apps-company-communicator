# Company Communicator App Template

| [Documentation](https://github.com/cristianoag/microsoft-teams-apps-company-communicator/wiki) | [Deployment guide](https://github.com/cristianoag/microsoft-teams-apps-company-communicator/wiki/Deployment-Guide) | [Deployment guide powershell](https://github.com/cristianoag/microsoft-teams-apps-company-communicator/wiki/Deployment-guide-powershell)  | [Architecture](https://github.com/cristianoag/microsoft-teams-apps-company-communicator/wiki/Solution-overview) |
| ---- | ---- | ---- | ---- |

Company Communicator is a custom Teams app that enables corporate teams to create and send messages intended for multiple teams or large number of employees over chat allowing organization to reach employees right where they collaborate. Use this template for multiple scenarios, such as new initiative announcements, employee onboarding, modern learning and development, or organization-wide broadcasts. 

The app provides an easy interface for designated users to create, preview, collaborate and send messages. It's also a foundation for building custom targeted communication capabilities, such as custom telemetry on how many users acknowledged or interacted with a message.

![Company Communicator compose message screen](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki/images/CompanyCommunicatorCompose.png)

### Key features
* **Message creation:** Easily create messages by using a team tab where team members who are permissioned can collaborate and create messages.
* **Audience selection:** Pick from four options to target audience. Send to general channel of selected teams, send in 1:1 chat to members of selected teams, send to all users who have the app installed or send to M365 groups, distribution lists or security groups.
* **Message metrics:** Export messages delivery report.
* **Localization:** Supports multiple locales.
## Get started

Begin with the [Solution overview](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/wiki/Solution-overview) to read about what the app does and how it works.

When you're ready to try out Company Communicator, or to use it in your own organization, you can choose to follow one of the below guides.
* [Deployment guide powershell](https://github.com/cristianoag/microsoft-teams-company-communicator-app/wiki/Deployment-guide-powershell).
    * **Recommended** Use this option to deploy the Company Communicator v5.0 using powershell script. The entire set-up is done by the powershell script.
* [Deployment guide](https://github.com/cristianoag/microsoft-teams-company-communicator-app/wiki/Deployment-guide).
    * Use this option to deploy the Company Communicator v5.0 with client secrets.
* [Deployment guide certificate](https://github.com/cristianoag/microsoft-teams-company-communicator-app/wiki/Deployment-guide-certificate).
    * Use this option to deploy the Company Communicator v5.0 with certificates.

## Migration 

If you already have older version of Company Communicator installed, then please use this [v5 migration guide](https://github.com/OfficeDev/microsoft-teams-apps-company-communicator/wiki/v5-migration-guide). Please note that deploying the major version update, like Company Communicator version 5.0 involves more than syncing the App Service and Azure Functions, so plan to review the migration guide before migrating to latest. 

Migrating to newer versions. 

 * [v5 migration guide](https://github.com/cristianoag/microsoft-teams-apps-company-communicator/wiki/v5-migration-guide)
 * [v4 migration guide](https://github.com/OfficeDev/microsoft-teams-apps-company-communicator/wiki/v4-migration-guide)
 * [v3 migration guide](https://github.com/OfficeDev/microsoft-teams-apps-company-communicator/wiki/v3-migration-guide)
 * [v2 migration guide](https://github.com/OfficeDev/microsoft-teams-apps-company-communicator/wiki/v2-migration-guide)

## Feedback

Thoughts? Questions? Ideas? Share them with us on [Teams UserVoice](https://microsoftteams.uservoice.com/forums/555103-public)!

Please report bugs and other code issues [here](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/issues/new).

## Legal notice

This app template is provided under the [MIT License](https://github.com/OfficeDev/microsoft-teams-company-communicator-app/blob/master/LICENSE) terms.  In addition to these terms, by using this app template you agree to the following:

- You, not Microsoft, will license the use of your app to users or organization. 

- This app template is not intended to substitute your own regulatory due diligence or make you or your app compliant with respect to any applicable regulations, including but not limited to privacy, healthcare, employment, or financial regulations.

- You are responsible for complying with all applicable privacy and security regulations including those related to use, collection and handling of any personal data by your app. This includes complying with all internal privacy and security policies of your organization if your app is developed to be sideloaded internally within your organization. Where applicable, you may be responsible for data related incidents or data subject requests for data collected through your app.

- Any trademarks or registered trademarks of Microsoft in the United States and/or other countries and logos included in this repository are the property of Microsoft, and the license for this project does not grant you rights to use any Microsoft names, logos or trademarks outside of this repository. Microsoft’s general trademark guidelines can be found [here](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general.aspx).

- If the app template enables access to any Microsoft Internet-based services (e.g., Office365), use of those services will be subject to the separately-provided terms of use. In such cases, Microsoft may collect telemetry data related to app template usage and operation. Use and handling of telemetry data will be performed in accordance with such terms of use.

- Use of this template does not guarantee acceptance of your app to the Teams app store. To make this app available in the Teams app store, you will have to comply with the [submission and validation process](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/deploy-and-publish/appsource/publish), and all associated requirements such as including your own privacy statement and terms of use for your app.

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Community Fork Changes

This is the log of changes implemented for Company Communicator.

**v5.13**
  - Reactions to messages sent by the bot are now tracked to the database. Reports can be created using Power BI connected directly to the Azure Storage Account or the CSV file with the information can be exported to be analized on Excel. 
  - The CSV report exported by authors now includes information on Reactions.

**v5.12**
  - The CSV report exported by authors now includes information on ReadStatus and ButtonTracking. That will make easier for author to create simple reports without PowerBI or accessing directly the database. 

**v5.11**
  - ATTENTION!!! - Merge of v5.1. If you have a deployment based on v4.XX you need to follow instructions [v5 migration guide](https://github.com/cristianoag/microsoft-teams-apps-company-communicator/wiki/v5-migration-guide) to update your setup.
  - Inclusion of the MasterAdminUpns and TargetingEnabled variables to the deployment template, those variables will be available during setup moving forward.

**v4.51**
- Fix for the fsevents issue
- Fix for the image expansion control when cards with buttons are created

**v4.5**
- Merge of PR to implement select/unselect buttons to control the inclusion of multiple Teams that are enabled for posting messages by setting-up the user bot.

**v4.45**
- Button urls with multiple parameters on the querystring were being stripped out when clicking on the buttons by the button tracking mechanism. Changed the code to encode the URL when sending the card and decoding it just before redirect inside the tracking code.
- Fix for the issue that was opening blank pages when clicking buttons during the message preview.

**v4.44**
- When uploading a CSV file and then a second one to replace the first, the upload box was staying in error state. Fix the error handling when uploading CSV files to allow uploading CSV files multiple times to replace previous versions. Cause by the changes on the way we account the image file size vs the card size. 

**v4.43**
- Fix to trail spaces after separators (, or ;) when specifying multiple masteradminupns in the app service configuration variable
- When upload blob storage is enabled, the size of the image was being accounted and blocking the upload of CSV files due to size restrictions. Now when enabling blob storage upload for images, the size of the image is not being discounted from the card size. That allows upload of CSV files up to the limit of the card (~30k).

**v4.42**
- Change to allow expansion of images in adaptive cards as described in https://devblogs.microsoft.com/microsoft365dev/five-new-features-enhancing-adaptive-cards-in-microsoft-teams/. This is to allow users better read content in high resolution images.
- Update to the CSV upload function to deal with files generated by excel (single column CSV files with tab delimiters instead of commas). CSV parser now validates files with tab or comma separators.

**v4.41**
- Fix to ensure the azure functions are using the right version of MSBuild. Avoid errors when compiling the code during sync process due to updates made to the AdaptiveCard library.

**v4.40**
- Implemented the App Service config variable DisableReadTracking to disable message read tracking. That is because we have some customers that installed CC in a S1/Small instance and that config doesn't support the additional load imposed by the read tracking mechanism.
- The read tracking code is now inside a try/catch to reduce the risk of crashing the App Service in resource depletion situations caused by running CC in S1/small App Service plans.
- https://tech-peanuts.com/2022/04/06/company-communicator-in-s1-small-app-service-plans/

**v4.32**
- Fixed a bug with URL encoding in mobile devices where button with names containing spaces were not working as expected.
- Customized the alert shown when messare are sent to have a localized message. Instead of the default sent card we now have custom messages in all supported languages.

**v4.31**
- Fixed bug for msg without buttons

**v4.30**
- Message tracking has been extended to include message button click tracking. 
- Updating the PBIX file to report on button click tracking.

**v4.23**
- Fix when deleting group associations. Due to the changes incorporated to support multiple associations for a specific groups the code to delete group associations was not working.

**v4.22**
- Fix for the error when saving messages with the targeting mode enabled.
- Fix for the radiobutton selection issue when targeting mode is enabled. Now authors in targeting mode will get the groups radion item selected by default.

**v4.21**
- Change to allow the selection of the same group in multiple instances of the authors app with targeting mode enabled.
