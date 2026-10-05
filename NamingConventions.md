# Marketing Cloud Naming Conventions Guide

## Overview

This guide establishes standardized naming conventions for all assets and objects within Salesforce Marketing Cloud. Following these conventions ensures consistency, readability, and maintainability across your marketing operations.

---

## Pascal Case Standard

All naming conventions in Marketing Cloud should follow **PascalCase** (also known as UpperCamelCase), where:
- The first letter of each word is capitalized
- No spaces or special characters are used (except where acronyms are present)
- Words are concatenated together

### Pascal Case Examples
✅ **Correct:**
- `CustomerSegmentation`
- `EmailCampaignQ4`
- `LeadScoringJourney`
- `ProductLaunchNotification`
- `API_DataSync` (acronym exception)
- `SMS_CampaignScheduler` (acronym exception)

❌ **Incorrect:**
- `customer_segmentation` (snake_case)
- `customerSegmentation` (camelCase)
- `Customer Segmentation` (spaces)
- `CUSTOMER_SEGMENTATION` (UPPER_SNAKE_CASE)

---

## 1. Email Names

Email templates and sends should use descriptive PascalCase names that indicate purpose and audience.

### Format
`[Purpose][Audience][Version/Date]`

### Examples
- `WelcomeEmailNewSubscriber`
- `WeeklyNewsletterEnterprise`
- `PasswordResetConfirmation`
- `PromotionalOfferPrimeMembers`
- `TransactionalOrderConfirmation`
- `ReEngagementCampaignInactiveUsers`
- `API_IntegrationNotification` (with acronym)

### Best Practices
- Include the email type (Welcome, Newsletter, Promotional, Transactional, etc.)
- Specify the audience segment when relevant
- Add version numbers or dates for A/B testing: `PromotionalOfferPrimeMembers_V2`
- Use underscores to separate acronyms from the rest of the name: `API_EmailNotification`, `SMS_Promotion`

---

## 2. List/Audience Names

Lists and audience segments should clearly identify their purpose and usage.

### Format
`[Segment Type][Criteria][Status]`

### Examples
- `EnterpriseAccountHolders`
- `HighValueCustomersActive`
- `LowEngagementSubscribersInactive`
- `FreemiumUsersConvertible`
- `VIPMembersLoyalty`
- `NewSignUpsLastThirtyDays`
- `API_ConnectedUsers` (with acronym)

### Best Practices
- Lead with the segment type
- Include key demographic or behavioral criteria
- Add status indicators when necessary (Active, Inactive, Pending)
- Avoid using generic names like `List1` or `Audience2`
- Use underscores when acronyms are at the beginning: `API_Subscribers`, `CRM_Contacts`

---

## 3. Journey/Automation Names

Marketing automation journeys and workflows should have clear, action-oriented names.

### Format
`[Action][Trigger/Content][Audience]`

### Examples
- `WelcomeJourneyNewSubscribers`
- `AbandonedCartRecoverySequence`
- `OnboardingFlowFreeTrialUsers`
- `ReActivationCampaignLapseMembers`
- `UpsellJourneyMidTierCustomers`
- `EventFollowUpAttendees`
- `API_DataSyncAutomation` (with acronym)

### Best Practices
- Use verbs that describe the journey purpose
- Include the trigger event or content type
- Specify the target audience
- Keep names concise but descriptive
- Use underscores to separate leading acronyms: `API_SyncWorkflow`, `CRM_UpdateJourney`

---

## 4. Data Extension Names

Data Extensions store custom data and should be named to reflect their content and purpose.

### Format
`[DataType][Purpose][TimeframeIfRelevant]`

### Examples
- `CustomerPurchaseHistory`
- `EventAttendeeInformation`
- `ProductReferenceData`
- `SurveyResponsesQ4`
- `WebsiteVisitorBehavior`
- `InventoryLevelsDaily`
- `CustomerPreferencesData`
- `API_IntegrationLog` (with acronym)

### Best Practices
- Clearly indicate what data the extension contains
- Use plural nouns when appropriate (e.g., `CustomerPreferences`)
- Include frequency indicators if data refreshes regularly (Daily, Weekly, Monthly)
- Avoid abbreviations unless universally understood
- Use underscores for acronyms: `CRM_SyncData`, `API_ResponseLog`

---

## 5. Attribute/Field Names

Individual fields within Data Extensions and other objects should follow PascalCase naming.

### Format
`[DataType][Description]`

### Examples
- `FirstName`
- `EmailAddress`
- `LastPurchaseDate`
- `LifetimeCustomerValue`
- `PreferredLanguage`
- `OptInStatus`
- `AccountCreationDate`
- `API_KeyLastUpdated` (with acronym)

### Best Practices
- Use descriptive names that indicate the field's content
- Avoid single-letter field names
- Use compound names to indicate related fields: `FirstName`, `LastName`
- Include units when relevant: `OrderValueUSD`, `HeightCentimeters`
- Use underscores when acronyms are part of the field name: `SMS_OptInDate`, `API_SyncTimestamp`

---

## 6. Campaign/Initiative Names

High-level campaign names should be clear and aligned with business objectives.

### Format
`[CampaignType][Initiative][TimeframeIfRelevant]`

### Examples
- `BlackFridayPromotion2024`
- `SpringProductLaunchCampaign`
- `CustomerRetentionInitiativeQ3`
- `BackToSchoolSaleEvent`
- `HolidayGiftingSequence`
- `AnnualClearanceSale`
- `API_PartnerIntegrationCampaign` (with acronym)

### Best Practices
- Include the year for time-sensitive campaigns
- Use season or event identifiers
- Make names searchable and memorable
- Avoid special characters or numbers at the beginning
- Use underscores for acronyms: `API_MarketingCampaign`, `SMS_PromoEvent`

---

## 7. Folder/Organizational Structure Names

Folders used to organize campaigns, emails, and content should also follow PascalCase.

### Examples
- `MarketingCampaigns/`
- `CustomerSegments/`
- `TransactionalEmails/`
- `JourneysAndAutomations/`
- `ReportsAndAnalytics/`
- `TemplateLibrary/`
- `DataExtensions/`
- `API_Integrations/` (with acronym)

### Best Practices
- Create logical folder hierarchies
- Use consistent naming across folder levels
- Organize by function, audience, or time period
- Include metadata in folder descriptions
- Use underscores for acronym-based folders: `API_Logs/`, `SMS_Templates/`, `CRM_Syncs/`

---

## 8. Template Names

Reusable email templates should be named to indicate their purpose and intended use.

### Format
`[TemplateType][Purpose][UseCase]`

### Examples
- `EmailTemplateWelcomeBase`
- `NewsletterTemplateStandard`
- `PromotionalEmailBannerLayout`
- `TransactionalReceiptFormat`
- `SurveyInvitationTemplate`
- `EventInvitationLuxury`
- `API_ResponseEmailTemplate` (with acronym)

### Best Practices
- Clearly indicate it's a template
- Specify the template type (Email, SMS, Push, etc.)
- Include the intended use case
- Version control templates: `EmailTemplateWelcomeBase_V2`
- Use underscores for acronyms: `API_NotificationTemplate`, `SMS_RemainderTemplate`

---

## 9. Report Names

Reports and analytics should have descriptive names following PascalCase.

### Format
`[ReportType][Content][Frequency]`

### Examples
- `EmailCampaignPerformanceMonthly`
- `JourneyConversionMetricsWeekly`
- `ListGrowthTrendingAnalysis`
- `DeliveryRateByISPDaily`
- `CustomerLifecycleValueReport`
- `SenderReputationScoreTracking`
- `API_SyncPerformanceDaily` (with acronym)

### Best Practices
- Include the report frequency
- Indicate the metrics or data being analyzed
- Use clear, business-friendly language
- Add date ranges in report titles when applicable
- Use underscores for acronyms: `API_ErrorLog`, `SMS_DeliveryReport`

---

## 10. Preference/Subscription Center Names

Preference centers and subscription management tools should be clearly named.

### Format
`[CommunicationType]PreferenceCenter[Version]`

### Examples
- `EmailPreferenceCenter`
- `CommunicationPreferencesHub`
- `NotificationSettingsPortal`
- `SubscriptionManagementCenter_V2`
- `ChannelPreferenceSelector`
- `API_PreferenceCenter` (with acronym)

### Best Practices
- Clearly indicate the purpose
- Include version numbers for updates
- Make names user-friendly
- Consider the customer experience
- Use underscores for acronyms: `API_SettingsCenter`, `SMS_PreferenceHub`

---

## Naming Best Practices Summary

| Principle | Description |
|-----------|-------------|
| **Clarity** | Names should immediately convey the object's purpose |
| **Consistency** | Apply PascalCase uniformly across all assets |
| **Uniqueness** | Avoid duplicate or similar names within the same section |
| **Brevity** | Keep names concise while remaining descriptive |
| **Scalability** | Use naming schemes that work as your instance grows |
| **Documentation** | Add descriptions to complex objects |
| **No Abbreviations** | Spell out words unless they're universally known (API, SMS, etc.) |
| **Avoid Numbers** | Use descriptive text instead of version numbers when possible |
| **Version Control** | Use `_V1`, `_V2` suffixes for iterations |
| **Acronym Handling** | Use underscores to separate acronyms: `API_DataSync`, `SMS_Campaign` |

---

## Special Characters & Symbols

### Allowed
- **Underscores** for version control: `CampaignName_V2`
- **Underscores** when an acronym is part of the name: `API_Integration`, `CRM_Sync`, `SMS_Campaign`
- **Hyphens** when necessary (though underscores are preferred): `Campaign-Name`

### Not Allowed
- Spaces
- Special characters: `! @ # $ % ^ & * ( ) = + [ ] { } ; : ' " , . < > / ? \`
- Accented characters: `é, ñ, ü` (use English equivalents)
- Leading or trailing underscores (except for acronyms): `_CampaignName` or `CampaignName_`
- Multiple consecutive underscores: `Campaign__Name`

### Acronym Guidelines
When an acronym appears at the beginning or middle of a name:
- ✅ **Use underscores to separate**: `API_DataSync`, `CRM_Integration`, `SMS_Campaign`
- ❌ **Do NOT mix case within acronyms**: `Api_DataSync`, `Crm_Integration`
- ✅ **Keep the acronym in ALL CAPS**: `API`, `CRM`, `SMS`, `CDN`, `CDO`, `SFMC`
- Examples of acronyms: API, CRM, SMS, CDN, CDO, SFMC, ESP, ISP, KPI, ROI, CSV, JSON

---

## Maintenance & Governance

### Regular Audits
- Conduct quarterly reviews of naming conventions
- Identify non-compliant assets
- Create migration plans for legacy names

### Documentation
- Maintain an asset inventory with standardized names
- Document the purpose and audience for each asset
- Update documentation when assets are renamed

### Onboarding
- Train new team members on naming conventions
- Provide quick reference guides
- Include naming standards in project kickoff meetings

---

## Examples by Use Case

### Ecommerce Business
- `ProductAnnouncement[ProductName]`
- `CartAbandonment[RecoveryAttempt]`
- `OrderConfirmationTransactional`
- `LoyaltyRewardsMembersExclusive`
- `API_InventorySyncDaily`

### SaaS Company
- `FreeTrialOnboardingSequence`
- `ProductUpdateAnnouncement`
- `UpgradeJourneyFreemiumUsers`
- `ChurnPreventionCampaign`
- `API_UserDataSync`

### Enterprise B2B
- `AccountBasedMarketingCampaign[AccountName]`
- `IndustrySpecificWhitepaperPromotion`
- `ExecutiveIntelligenceBriefing`
- `PartnerEcosystemEngagement`
- `CRM_AccountSyncDaily`
- `API_PartnerIntegration`

---

## Questions & Support

For questions about naming conventions or to propose updates to this guide, please contact your Marketing Cloud Administrator or create an issue in this repository.

**Last Updated:** October 2026
**Version:** 1.1
