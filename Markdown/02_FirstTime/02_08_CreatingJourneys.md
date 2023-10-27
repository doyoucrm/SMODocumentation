# First Time: Creating Journeys

[comment]: <> (Export To: Web/02_08_CreatingJourneys.html)

**In this article**
    <br>[About Marketing Journeys](#about-marketing-journeys)
    <br>[Create Marketing Journeys](#create-marketing-journeys)
    <br>[Use Journey Insights](#use-journey-insights)

## About Marketing Journeys

Marketing Journeys are automated, guided customer experiences that you can create using Dynamics 365 Marketing. These journeys can be designed to react to customer actions in real-time or target specific customer segments. They help you engage with your customers through personalized messages and offers, driving customer loyalty and increasing sales.

For example, you can create a Marketing Journey that sends an email to new customers, offering them a special discount on John Deere equipment. If the customer clicks on the offer, the journey can automatically send a follow-up email with more details or a reminder before the offer expires. These journeys can be as simple or complex as needed, allowing you to create tailored experiences for your customers.

## Create Marketing Journeys

Marketing journeys can be created in both Outbound and Real-time marketing. Follow these step-by-step instructions to create a Marketing Journey in Dynamics 365 Marketing.

### Before you get started...

Before you can create and use Marketing Journeys, there are a few key components that must be configured within Dynamics 365 Marketing:

1. **Segments:** Segments are groups of customers that share similar characteristics or behaviors. You'll need to create segments to target specific audiences in your Marketing Journeys. For example, you might create segments for new customers, customers who have purchased specific equipment, or customers who have shown interest in a particular service.
2. **Content:** Content includes the email messages, text messages, and other marketing materials that you'll use in your Marketing Journeys. You'll need to create and design the content that will be sent to your customers during each step of the journey. Make sure your content is engaging and relevant to your audience.
3. **Triggers:** Triggers are the events or actions that initiate a specific step in a Marketing Journey. For example, a trigger might be a customer clicking on a link in an email or signing up for a newsletter. There are many out-of-the-box triggers that you can use right away in your Marketing Journeys, or you can create custom triggers to fit your needs.

Once these components are configured, you'll be able to create and launch your Marketing Journeys.

### Create an Outbound Journeys

This step-by-step guide is designed to help a John Deere dealer marketing user or admin to create an outbound marketing journey using Dynamics 365 Marketing. The goal for this guide is to send out an email campaign to customers about a hypothetical special promotion for a specific tractor model.

#### Step 1: Create a segment
If you already have a marketing segment you want to use, you can skip this step. Otherwise, follow these steps to create a new segment:

1. Navigate to **Outbound marketing** and then click **Segments** under the "Customers" section of the navigation pane.
2. Click on "New segment" to create a new segment.
3. Name the segment (e.g., "Tractor Promotion Segment").
3. Define the segment conditions based on the audience you want to target, such as customers who have shown interest in tractors or customers in a specific geographic region.
4. Save and publish the segment.

#### Step 2: Create email content
If you already have an email template you want to use, you can skip this step. Otherwise, follow these steps to create a new email template:

1. Navigate to **Outbound marketing** and then click **Marketing emails** under the "Marketing execution" section.
2. Click on 'New email' to create a new email template.
3. Name the email (e.g., "Tractor Promotion Email").
4. Use the drag-and-drop email designer to create your email with the promotional content, including images, text, and links.
5. Include personalization, such as the customer's name, to make the email more engaging.
6. Save the email and change its status to "Ready to send".

#### Step 3: Create a segment-based journey

1. Navigate to **Outbound marketing** and click **Customer journeys** under the "Marketing execution" section.
2. Click on 'New journey' and select 'Segment-based journey'.
3. Name the journey (e.g., "Tractor Promotion Journey").
4. Set the journey start by selecting your "Tractor Promotion Segment" as the audience.
5. Choose a one-time journey frequency, as this is a single promotion.
6. Set the start date and time for when you want the journey to begin.

#### Step 4: Add email to the journey

1. On the journey canvas, click the plus sign (+) to add a new step.
2. Select 'Send an email' and choose the "Tractor Promotion Email" you created earlier.
3. For the 'Send to' field, select the attribute containing the customer's email address (e.g., "Email").

#### Step 5: Publish the journey

1. Review the journey to ensure all steps and content are correct.
2. Check that the email content is in the "Ready to send" state.
3. Click on 'Publish' to make the journey live.

#### Step 6: Monitor journey performance

1. Navigate to the journey analytics page in Dynamics 365 Marketing to track the performance of your journey.
2. Analyze metrics such as email opens, clicks, and conversions to understand the success of your campaign.

### Create a Real-Time Journeys

This step-by-step guide is designed to help a John Deere dealer marketing user or admin to create a real-time marketing journey using Dynamics 365 Marketing. The goal for this guide is to send out follow-up emails to a contact after they clicked a link in a marketing email.

1. Log in to Dynamics 365 Marketing:
Log in to your Dynamics 365 Marketing account using your credentials.

2. Navigate to Customer Journeys:
From the main menu, click on "Marketing" and then select "Customer Journeys."

#### Step 1: Create a new trigger-based customer journey
1. Navigate to **Real-time marketing** and then click **Journeys** under the "Engagement" section.
2. Click the "New" button on the top left-hand corner.
3. Name your new journey "Email Link Clicked Journey".
4. Ensure "Trigger-based Journey" is selected.
5. Click in the "Choose a trigger" field and select "Email Link Clicked".
6. Then click "Create".

#### Step 2: Add steps to your journey
Now that you've selected a trigger and created your new journey, you can begin adding steps. Use the plus sign (+) on the journey canvas to add individual steps such as sending an email, adding a condition, or waiting for a specific period.

For our example journey, we'll add the following steps:
1. Send an email: Select an email template promoting a John Deere mower and configure it with personalized content. Make sure to specify the attribute containing the customer's email address in the "Send to" field.
2. Add a condition: Check if the customer clicked the link in the email. If they did, proceed to the next step; otherwise, end the journey for that customer.
3. Wait: Add a waiting period, for example, 3 days, before sending a follow-up email.
4. Send a follow-up email: Send a follow-up email reminding customers of the promotion or offering additional information.

#### Step 3: Test your journey
Before making your journey live, test it with a small group of customers to ensure everything is working as expected.

#### Step 4: Publish and monitor your journey
Once you're satisfied with the setup, click the "Publish" button in the top right-hand corner. Your journey is now live and will be triggered by the specified event.

Check your journey's analytics page regularly to understand its performance and identify areas for improvement.

## Use Journeys Insights

Marketing Journey Insights are an integral part of Dynamics 365 Marketing that provide valuable information about your customer journeys, helping you identify how customers react to your marketing initiatives. You can analyze contact flow through the journey, see how many messages were delivered, and identify reasons for incomplete journeys or blocked emails. With this information, you can optimize your marketing strategies and improve customer engagement.

Follow these step-by-step instructions to access and use Marketing Journey Insights in Dynamics 365 Marketing:

1. In **Outbound marketing**, click on **Customer journeys** under the "Marketing execution" section of the navigation pane.  In **Real-time marketing**, click on **Journeys** under the "Engagement" section.
2. Select a customer journey from the list. Insights are only available for customer journeys that are (or have been) live.
3. View the Designer tab for a read-only version of your journey pipeline. Above each tile, you'll see an overview of how contacts flowed through that tile. Inspect these values for a quick understanding of how your contacts interacted with each part of the journey.
4. For more detailed information about a specific tile, select it from the pipeline and look at the Data panel. You'll see information such as the number of contacts processed, stopped, or in progress.
5. To view more detailed insights, switch to the Insights tab. Here, you'll find the Overview and Incomplete journeys sections.
    * Overview: This section shows basic email results and information about how many contacts interacted with the emails and marketing pages used by the journey.
    * Incomplete journeys: This section helps you identify reasons why contacts might fail to complete the journey, and lists each contact affected by these issues. You'll see two categories: Stopped contacts and Blocked emails. Stopped contacts are those who stopped in the middle of the journey due to various reasons, such as joining a suppression segment or lowering their consent level. Blocked emails are messages that the system didn't attempt to send, usually because of contact preferences or technical problems with the message.
6. To analyze stopped contacts or blocked emails, select a reason in the left column of the table, and you'll see a list of affected contacts in the right column.

By using Marketing Journey Insights, you'll be better equipped to understand and optimize your marketing efforts, leading to improved customer engagement and better results for your John Deere dealership.