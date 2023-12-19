# First Time: Creating Marketing Emails

[comment]: <> (Export To: `../Web/02_02_CreatingMarketingEmails.html`)

**In this article**
    <br>[About Marketing Emails](#about-marketing-emails)
    <br>[Create Marketing Emails](#using-marketing-emails)
    <br>[Use Marketing Emails Insights](#use-marketing-emails-insights)

## About Marketing Emails

Marketing Emails in Microsoft Dynamics 365 Marketing are a powerful tool that allows businesses to communicate with their customers and prospects effectively. With this feature, businesses can create and send personalized and targeted emails to their customers, which can help them increase engagement and generate leads.

To create Marketing Emails in Microsoft Dynamics 365 Marketing, businesses can use a drag-and-drop editor that simplifies the process of designing and creating visually appealing emails. The editor includes a wide range of customizable templates and allows businesses to add images, videos, and dynamic content to their emails easily.

Moreover, Marketing Emails in Microsoft Dynamics 365 Marketing also provide advanced tracking and reporting capabilities. Businesses can track and analyze the performance of their emails, including open rates, click-through rates, and conversions. This information can help them make data-driven decisions and optimize their email marketing campaigns for better results. Overall, Marketing Emails in Microsoft Dynamics 365 Marketing is a valuable tool for businesses that want to engage their customers effectively and grow their business.

## Create Marketing Emails

The following section will guide you through the process of creating Marketing Emails in Microsoft Dynamics 365 Marketing.

### Before you get started...

Before you create your first Marketing Email record, you should complete the steps outlined in the article [Default Settings For Email Marketing](../../01_Setup/Web/01_02_DefaultSettingsForEmailMarketing.html).

### Real-time Journeys Emails

1. Navigate to the **Real-time journeys** area.  Then click on **Emails**.
2. Click "New".
3. A template picker will be displayed.  You can choose from one of the templates provided, or you can skip this step to start with a blank template.
4. After picking a template or choosing to start from a blank email, you will be taken to the email editor.  Here you can edit the email and add content to it.
    1. The main part of the email editor is the **Content** section.  This is where you can add content to your email.  You can add text, images, videos, and dynamic content to your email.
    2. On the right-hand side of the editor is the **Inspector** area, which will allow you to switch between multiple tool palettes:
        1. **Elements**:  This palette contains element blocks, such as _Text_, _Images_, _Buttons_, etc.  It also displays auto-formatting options for sections of your email.  You can drag and drop elements from this panel into the **Content** section.
        2. **Content Blocks**: This palette contains content blocks.  The default blocks are Email Footer and Social Media.
        3. **Content Ideas**:  This palette gives you the option to use AI to generate multiple text options for your email, which you can select to insert into your content blocks.  (Note: This feature is currently in preview but has been made available before it's official release so that customers may provide early feedback.  Preview features aren't intended for production use and may have limited or restricted functionality.  See [Microsoft's documentation](https://learn.microsoft.com/en-us/dynamics365/marketing/content-ideas) on this feature for more details.)
        4. **Personalize**:  This palette gives you the ability to configure content blocks so that they dynamically display content based on the recipient's information.  For example, you can use "Inline Conditions" to configure a content block to display the recipient's name, company, or other information; or you can use "Lists" to dynamically insert a list of items pulled from the recipient's contact record.
        5. **General Styles**:  This palette allows you to configure the overall style of your email, such as the background color, font, etc.
        6. **Email Header**:  This is an important palette that contains sender email address and company address information (which should default automatically to whatever was configured during the Marketing app's initial setup, but can be modified here on an email-by-email basis).  This section also includes email settings options for the template used, the message designation (e.g., Commercial vs. Transactional), the email content language, and the auto-generated plain text preview of the email's content.

## Use Marketing Email Insights

Marketing Email Insights provide comprehensive data on how your email recipients interact with your messages. It includes details such as open rates, click-through rates, and geographical data. These insights help you understand the overall effectiveness of your marketing emails and identify areas for improvement. You can also track the performance of individual links in your email messages and monitor delivery results, such as delivered, blocked, or bounced emails.

Follow these step-by-step instructions to access and use Marketing Email Insights in Dynamics 365 Marketing:

1. Navigate to **Real-time journeys** > **Emails**.
2. Select an email message from the list that is (or has been) live. Click on the message to open its details.
3. In the email message details, switch to the Insights tab to view the email insights.
4. You will see several categories within the Insights tab. Here's a brief overview of what each category provides:
    * Overview: A summary of key performance indicators (KPIs), top-10 links, responses over time, geographical data, and more.
    * Delivery: Detailed information about delivery results and affected contacts, along with a table of overall results by recipient domain.
    * Links: An analysis of each link in the message, including a heat map that highlights the most and least clicked links.
    * Interactions: A timeline and lists of recipients for various KPIs such as opens, clicks, and forwards.
5. To analyze a specific customer journey, use the filter settings at the top of the Insights tab. Choose the desired journey from the drop-down menu. If you don't select a journey, the information displayed will apply to all journeys where the message was used.
6. You can also filter email insights by date range using the "From" and "To" settings at the top of the Insights tab.

By following these steps, you can easily access Marketing Email Insights and use the data to optimize your email marketing strategies for your John Deere dealership. Remember to consistently review these insights to identify trends and make data-driven decisions to improve your campaigns.