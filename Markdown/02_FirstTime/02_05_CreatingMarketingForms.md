# First Time: Creating Marketing Forms

[comment]: <> (Export To: Web/02_05_CreatingMarketingForms.html)

**In this article**
    <br>[About Marketing Forms](#about-marketing-forms)
    <br>[Create a Marketing Form](#create-a-marketing-form)
    <br>[Use Marketing Form Insights](#use-marketing-form-insights)

## About Marketing Forms

Marketing Forms are a key component of Dynamics 365 Marketing, designed to help you collect valuable information from your customers and prospects. These forms can be easily created and customized to suit your dealership's specific needs, such as gathering contact details for newsletter subscriptions, managing event registrations, or even collecting feedback on your products and services.

With Marketing Forms, you can engage with your audience in a more interactive way, enabling you to build stronger relationships and better understand their needs. This, in turn, can help you refine your marketing strategies and drive your dealership's growth.

### Form Types
The Marketing Forms can be configured to accommodate several use cases:

* **Landing Page:** This is a general-purpose form for collecting contact information on marketing pages that are not subscription centers or forwarding forms.
* **Subscription Center:** This form is used to collect contact information for newsletter subscriptions, or for managing contact preferences regarding existing subscriptions.
* **Forward to a Friend:** This form is used to collect contact information for forwarding a page to a friend or colleague.

### Embedded vs. Captured Forms

In Dynamics 365 Marketing, there are two ways that Marketing Forms can be configured:

#### Embedded Forms

Embedded forms are forms you build in Dynamics using a designer tool, which can then be integrated directly into your dealership's website or any other online platform. These forms can be styled to blend in with the rest of your web page's content and are fully customizable to match your dealership's branding and design. This seamless integration allows your customers to easily provide the information you need without navigating away from your website.

**Pros:**

* Seamless integration into your website, providing a consistent user experience
* Fully customizable to match your dealership's branding and design
* Can be used on multiple platforms, like your website, social media, or email campaigns

#### Captured Forms

Captured forms still use the Marketing Forms records in Dynamics Marketing, but rather than use the designer tool to create the form, you can use a wizard to capture an existing form from your dealership's website or another online platform. This allows you to use the same forms you already have in place, while still taking advantage of the Marketing Forms features, such as tracking and insights.

**Pros:**

* Easy to set up (but may require some assistance from your web developer)
* Allows you to track form submissions and gather insights on customer interactions on existing forms you may already have in place

### Other Features
Marketing Forms are extremely versatile and highly configurable.  Please check out [Microsoft's documentation](https://learn.microsoft.com/en-us/dynamics365/marketing/marketing-forms) for more information how to configure your Marketing Forms for a variety of scenarios.

### Why this is only an Outbound feature

Marketing Forms are designed to support outbound marketing activities, which primarily focus on reaching out to potential customers through various channels, like email, social media, and direct mail.  While not an outbound marketing activity in itself, form submissions drive outbound activity.

## Create a Marketing Form

Follow the guides below to set up your first embedded marketing form, and capture your first external marketing form in Dynamics 365 Marketing.

### Before you get started...

It would be a very good idea to already have your website's domain authenticated before getting started with Marketing Forms.  This is especially true if you want to setup captured forms, since you'll only be able to capture forms that are on a domain that has already been authenticated.

### Create a marketing form

#### Step 1: Create a new Marketing Form

1. Navigate to **Marketing** > **Marketing Forms**.
1. Click on the "New" button on the top of the "Marketing Forms" page.
1. A window will pop up, asking you to choose a template for your form. Select a template that best fits your needs or choose a blank template to create a form from scratch.
1. Choose "Landing Page" as the form type, and then click "Next."
1. Enter a name and description for your form, and click "Create."

#### Step 2: Design your form using the form designer

1. You'll now be in the form designer, where you can create and edit your form using design elements.
2. Drag fields and design elements from the "Toolbox" tab to the canvas to assemble your form.
3. Configure each element by selecting it and going to the "Properties" tab. For more information, refer to the Design elements reference.

#### Step 3: Ensure all required elements are included

1. Review the table in the documentation you provided earlier to make sure you've included all required elements for a 'Landing Page' type form.
2. Make sure to add a "Submit" button to your form as it is required for a 'Landing Page' type form.

#### Step 4: Validate your form

1. Once you're done designing your form, click on "Check for errors" to make sure you've included all the required content and settings.
2. If there are any errors, correct them and click on "Check for errors" again until the form passes validation.

#### Step 5: Publish your form

1. When you're ready to make your form available for use, click on "Go Live."
2. The form will be checked for errors, and if it passes, it will be moved to the live state, making it available for use on a marketing page or to be embedded on an external site.

#### Step 6: Add the form to a marketing page

1. To add your form to a landing page, navigate to "Marketing" > "Marketing Pages" and either create a new marketing page or edit an existing one.
2. Drag a "Form" element onto the page canvas, and then choose the form you just created from the list of available forms.
3. Save and publish your marketing page.

### Embed a marketing form on your website

Follow the steps below to embed your marketing form on an external web page:

1. **Locate the Form:** Find the marketing form you want to embed in the list of forms. If you've recently created it, it should be near the top. Click on the form to open it.
2. **Access the Embed Code:** Once the form is open, click on the "Embed" tab located in the top-right corner of the form designer. This will display the embed code that you'll need to copy.
3. **Copy the Embed Code:** Click on the "Copy to clipboard" button to copy the entire embed code. This code includes both the form-capture JavaScript and the HTML code for the form itself.
4. **Paste the Embed Code into Your External Web Page:** Open the HTML file or content management system (CMS) for the external web page where you want to embed the form. Locate the section of the page where you'd like the form to appear and paste the copied embed code into the HTML source.
5. **Save Your Changes:** Save the changes to your external web page. If you're using a CMS, you may need to publish or update the page to make your changes live.
6. **Test the Embedded Form:** Visit the external web page where you embedded the form to ensure that it appears and functions correctly. Fill out the form and submit it to verify that the information is captured and processed by Dynamics 365 Marketing.

### Capture a marketing form from your website

Follow the steps below to capture an existing external form's submissions using the form capture capability in Dynamics 365 Marketing:

#### Step 1: Check field mappings

1. Navigate to **Marketing** > **Marketing templates** > **Form fields**.
2. Ensure that all fields required by your external form are correctly mapped here. Add any missing fields if necessary.

#### Step 2: Set up form capture

1. Navigate to **Marketing** > **Internet marketing** > **Marketing forms**.
2. Click on the "Capture form" button to start the form capture wizard.

#### Step 3: Enter the form location

1. Input the URL of the external page containing the form you want to capture.
2. A new tab will open with the webpage; keep this tab open until you complete the form capture process.

> > ###### Note
> > In order for this to work, the URL you input must already belong to one of your authorized domains. If you haven't already done so, you'll need to add the domain to your list of authorized domains. See the article [Authenticate Your Domain](../../01_Setup/Web/01_01_AuthenticateYourDomain.html) for more information.
<br>

#### Step 4: Check for a tracking script

1. Click the button in the new tab to proceed.
2. If you need a new script, select "I need a new script" to generate a script for your website.
3. If you already have a script, use the dropdown list to find the appropriate script for the form's webpage.

#### Step 5: Place the script into your webpage

1. Copy the tracking script.
2. Add the script at the top of your webpage's HTML code or share it with your developer to do so.
3. Refresh the tab containing your webpage so the form capture wizard can detect the updated script.

#### Step 6: Choose the form

1. Refresh the webpage again; the available forms will be shown.
2. Select the form you want to capture.

#### Step 7: Map the fields

1. Map the fields from your external form to the Dynamics 365 fields to ensure proper data storage.

#### Step 8: Overview and go live

1. Review the mapped fields to ensure correctness.
2. Go to the "Summary" tab and configure the marketing form settings as needed (e.g., Name, record updating preferences, and matching strategies).
3. Click "Save" to save your marketing form.
4. Click "Go live" to activate your form capture, allowing it to accept data from your external form.

## Use Marketing Form Insights

Marketing Form Insights offer valuable data on how your contacts interact with your marketing forms. This data is combined across all instances where your form is used, but can be filtered by date range. By examining the insights, you can determine the total number of form submissions, new contacts created, and leads generated, among other key performance indicators (KPIs). This information can help you identify trends and make data-driven decisions to optimize your marketing efforts.

Follow these step-by-step instructions to access and use Marketing Form Insights for your John Deere dealership marketing forms:

1. Navigate to **Outbound marketing** > **Marketing forms**.
2. Choose the marketing form you want to analyze by clicking on its name.
3. Once the form is open, click on the "Insights" tab.

Here, you'll find the following categories of insights:

* Overview: Displays KPIs such as total form submissions, contacts created or updated, and leads created or updated by the form.
* Submissions: Shows a table with the full content of each submission made through the form, including metadata and important field values.

To better understand the insights and KPIs provided:

1. Hover your mouse pointer over a value in the table or graph.
2. An info icon will appear; hover your mouse pointer over this icon to view a tooltip with a description of that value.

By reviewing these insights, you can make data-driven decisions on how to optimize your marketing forms for increased customer engagement and conversions.