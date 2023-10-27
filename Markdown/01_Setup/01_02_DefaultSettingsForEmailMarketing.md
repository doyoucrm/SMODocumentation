# System Setup: Default Settings (for Email Marketing)

[comment]: <> (`Export To: Web/01_02_EmailDefaultSettings.html`)

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
		(img)

## Understanding the Default Settings record

The following section will guide you through the types of settings contained in the Default Settings record(fn).

For a quick guide on which settings need to be setup to make use of the app's email marketing capabilities, jump down to the section [Steps to get started].

### Default Content Settings

The default content settings record(fn) is where your marketing emails will look to automatically populate some key information about your business.

To edit the default content settings, click on the "Marketing email" tab, and then click "Default Content Settings" to open it.

To make changes to this record, you may need to click the "Stop" button in the command bar (i.e., the bar of buttons above the form).

Here are the default content settings that you can change here:

* **Address main**:  This is the physical address of your business, which is is something most marketing email whitelists and spam filters will look for to help them verify the legitimacy of the email and its sender.  This value is required.
* **Address line 2**:  A second address line that can be included in emails along with the main address.  This could be used for things like mailing addresses if different than the main address.
* **Social Media URLs**:  These are links to your company's social media pages.  If you populate these values here, they can automatically be added to your marketing emails (as hyperlinks or as buttons).
* **Subscription center**:  This should already contain a default value, which might appear in the following format:  `{{msdyncrm_marketingpage(uniqueid)}}`.  This is an example of a dynamic tag, which are used throughout the Marketing app which enables the system to grab values from elsewhere in the system, rather than require you to set a permanent value.

> > ###### Note
> > The subscription center is covered in more detail in [System Setup: Opting In Contacts to Marketing Communications].

If you stopped the record so that you could make changes, save the record and then click the "Go live" button in the command bar when finished.  The system will validate the record before taking it live again, and will alert you in the record's notification area if any problems are detected.

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

This is setting is used specifically by customer journeys (i.e., marketing automation) for timing when emails should be sent out or on automated timers for triggering steps.

### Global Level Double Opt-In

Click on the "Global level double opt-in" tab to view the following global double opt-in settings:

* **Enable double opt-in**:  Enables or disabled double opt-ins for email marketing globally.  This toggle is set by default to "No".  
* **Subscriptions**:  A lookup field that points to a marketing email record.  When this value is set, and when the global "Enable double opt-in" value is "yes", the specified email will be sent automatically when contacts subscribe to newsletters, etc.
* **Consent**:  Similar to the "Subscriptions" lookup, this points to a marketing email record used for confirming changes in a contact's level of consent(fn).
* **Use marketing pages for thank you**:  Indicates whether you want contacts redirected to custom "Thank You" pages after a confirmation step.  This toggle is set by default to "Yes".
* **Thank-you page for subscriptions**:  A lookup field to the specific marketing page record that you would like to use as a landing page to thank contacts for confirming their subscriptions.  This value is blank by default.
* **Thank-you page for consent**:  A lookup field to the specific marketing page record that you would like to use as a landing page to thank contacts for confirming their consent-level changes.  This value is blank by default.

### Bypass Email Deduplication
Click on the "Bypass email deduplication" tab to view this setting.  This value is set by default to "No".

When this value is set to "No", the Marketing app will do its best to try and prevent contacts from receiving the same marketing email messages twice.  For example, if a contact has 2 different email addresses in Dynamics, and both email addresses were somehow pulled into an email campaign, the system would likely catch this and only send the marketing email once to the contact.

This involves a bit of business intelligence that looks at many other vectors besides just the recipient's email address.  As such, it might not catch duplicates 100% of the time, but it is still extremely effective.

Preventing duplicates is generally the preferred behavior, but if you are having experience an issue where multiple contacts are reporting that they are not receiving an automated marketing email, you can toggle this value to "Yes" to bypass email deduplication and see if this corrects the issue.

## Quickstart Steps

**Important!**  These other steps should be completed before making changes to your Default Settings record:

* [Authenticate at least one custom domain]
* [Configure global or form-based opt-in settings]

### 1. Confirm a Content Settings record exists
Ordinarily, this step will not be required and you can go directly on to **step 3**.  This is because the Marketing app usually comes with a single Content Settings record already created (which should be preconfigured with your app's default Subscription Center).

However, there are certain scenarios which may cause the Marketing app to skip creating the Content Settings record, so you may want to follow the steps below to confirm that the record exists.

1. Click into the search bar at the top of the app; then click "Search for rows in a table using advanced filters".  A panel should open titled "Select a table to search".
2. In the panel's search field, type "Content" (without quotes).
3. The tables should be filtered to only show a few options.  Select "Content settings" from the options displayed and click the "Continue" button at the bottom of the panel.
4. A view will load into the main part of the window, and a new panel will automatically be opened titled "Edit filters: Content settings".  Click "Cancel" to dismiss this new panel and to view the view of Content Settings records.

If a Content Settings record already exists in your system, you will see it in the view you just opened.  If it exists, you can go on to step 2.  Otherwise, to create a new record:

6. Click the "New" button.  A blank Content Settings record will be displayed.
7. The new record cannot be saved unless the required fields ("Name", "Address main", and "Subscription center") have been filled in.
8. When finished, save and close the record.

> > ###### Note
> > See **step 2** for details on configuring Content Settings field values.  Then go on to **step 3**.

### 2. Update the Default Content Settings record
Most of the fields in a Content Settings record have a special button that give you the option specify either **dynamic** or **static** values.

### 3. Locate or create a new Default Settings record
1. Navigate to the Settings area of the Marketing app.
2. Click on "Default Settings" in the left-hand navigation (located under the "Email marketing" header).
3. If the records list is empty, click "New" to create a new record.  When the form is displayed, give your new Default Settings record a name.  (Choose any name you like, as it won't affect the Marketing app's functionality.)
4. If the record's list is **not** empty, open records until you find the one where the "Default" value is "Yes".

> > ###### Note
> > You can also fill in the social media URLs if you like, but the above items are required to get your marketing app up and running.
<br>

### 3. Update the Default Sending Domain
1. Complete the steps required to [authenticate your domain].
2. Update the "Default sending domain" value so that it points to your authenticated domain.

### 4. Update the Default Time Zone
1. Navigate to the "Customer Journey" tab.
2. Click into the "Default time zone" field and select your time zone from the list.

### 5. Configure Double Opt-In
1. Navigate to the "Global level double opt-in" tab.
2. If your dealership is located in the US, or your local laws do not required you to enabled double opt-in by default, set the "Enable double opt-in" toggle to "No".

> > ###### Note
> > You may want to eventually enable double opt-in, but it is not required to get your marketing app up and running.
<br>