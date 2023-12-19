# System Setup: Default Settings (for Email Marketing)

[comment]: <> (Export To: `../Web/01_02_EmailDefaultSettings.html`)

**In this article**
    <br>[Locate the Email Default Settings record](#locate-the-email-default-settings-record)
    <br>[Understanding the Email Default Settings record](#understanding-the-email-default-settings-record)
    <br>[Quickstart steps](#quickstart-steps)

Right out of the box, a number of settings will need to be set or updated in order to start getting the most out of Dynamics Marketing.  This guide will walk you through the Default Settings for email marketing in the Marketing app and how to adjust them for your dealership.

## Locating the Default Settings record

1. Navigate to the Settings area of the Marketing app.
2. Click on "Default settings" under the "Email Marketing" heading.  A records list will be displayed.  
	* If the Marketing app has **not** been configured before, this list will be empty.  If this is the case, clicking the "New" button will create a new default settings record for the app.
	* If the list is **not empty**, it will likely only contain one record.  If so, open it.  If there are multiple records, open them one at a time until you find the record where the "Default" value equals "Yes".

## Understanding the Default Settings record

The following section will guide you through the types of settings contained in the Default Settings record(fn).

For a quick guide on which settings need to be setup to make use of the app's email marketing capabilities, jump down to the section [Quickstart Steps](#quickstart-steps).

![](../Images/01_02_01_DefaultRecord.png)

### Default Sending Domain

The default sending domain (located on the "Marketing email" tab) is a lookup to an authenticated domain record.

> > ###### Note
> > The topic of authenticated domains and how to set them up is covered in more detail in [System Setup: Authenticate Your Domain].

The system provides you with a Domain record that is already authenticated.  However, this default domain is tied directly to the Dynamics Marketing services and is not suitable for production use.  If you have already created a Domain of your own and have verified its ownership, edit the "Default sending domain" value by clicking the search button (that appears when you hover your mouse over the field) and then choosing the Domain record you created.

### Default From Email and Default From Name

These two fields are used to configure how the "From" information should look to email recipients when they receive marketing emails.  The default sender is a hosted account that is baked into the Marketing app's services, and will not reflect your company information or brand in any way.  The "Default From Email" and "Default From Name" values masks this information.

Optimally, your "Default From Email" value should have a domain name that matches one of your [authenticated domains].

For example, if you setup an authenticated domain for the URL `https://www.bestdealerever.com` then your "Default From Email" might be set to `marketing@bestdealerever.com`.

### Default Time Zone

The option to set your time zone is located on the "Customer Journey" tab.  Clicking into the "Default time zone" field will allow you to select an option from a list global time zones.

This setting is used specifically by customer journeys (i.e., marketing automation) for timing when emails should be sent out or on automated timers for triggering steps.

### Bypass Email Deduplication
Click on the "Bypass email deduplication" tab to view this setting.  This value is set by default to "No".

When this value is set to "No", the Marketing app will do its best to try and prevent contacts from receiving the same marketing email messages twice.  For example, if a contact has 2 different email addresses in Dynamics, and both email addresses were somehow pulled into an email campaign, the system would likely catch this and only send the marketing email once to the contact.

This involves a bit of business intelligence that looks at many other vectors besides just the recipient's email address.  As such, it might not catch duplicates 100% of the time, but it is still extremely effective.

Preventing duplicates is generally the preferred behavior, but if you are having experience an issue where multiple contacts are reporting that they are not receiving an automated marketing email, you can toggle this value to "Yes" to bypass email deduplication and see if this corrects the issue.

## Quickstart Steps

**Important!**  These other steps should be completed before making changes to your Default Settings record:

* [Authenticate at least one custom domain]

### 1. Locate or create a new Default Settings record
1. Navigate to the Settings area of the Marketing app.
2. Click on "Default Settings" in the left-hand navigation (located under the "Email marketing" header).
3. If the records list is empty, click "New" to create a new record.  When the form is displayed, give your new Default Settings record a name.  (Choose any name you like, as it won't affect the Marketing app's functionality.)
4. If the record's list is **not** empty, open records until you find the one where the "Default" value is "Yes".

### 3. Update the Default Sending Domain
1. Complete the steps required to [authenticate your domain].
2. Update the "Default sending domain" value so that it points to your authenticated domain.

### 4. Update the Default Time Zone
1. Navigate to the "Customer Journey" tab.
2. Click into the "Default time zone" field and select your time zone from the list.