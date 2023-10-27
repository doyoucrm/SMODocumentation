# First Time: Creating Text Messages

[comment]: <> (`Export To: Web/02_02_CreatingTextMessages.html`)

**In this article**
    <br>[About Text Messaging in Dynamics Marketing](#about-text-messaging-in-dynamics-marketing)
    <br>[Create Text Messages in Real-Time Marketing](#create-text-messages-in-real-time-marketing)
    <br>[Use Text Message Insights](#use-text-message-insights)

## About Text Messages in Dynamics Marketing

Dynamics 365 Marketing allows you to reach your customers directly on their mobile devices by sending them text messages.  This can be done by creating a text message in the Real-Time Marketing module, or by creating a text message activity in a customer journey, and insights on the performance of your text messages can be found in the Reports tab of the message.

## Create Text Messages in Real-Time Marketing

The following section will walk you through the process of creating a text message in the Real-Time Marketing module of Dynamics 365 Marketing.

### Before you get started...

Before you send your first text messages from Dynamics Marketing, you should complete the steps outlined in the article [Text Messaging Providers](../../01_Setup/Web/01_03_TextMessagingProviders.html).

### Create a text message

Navigate to **Real-time marketing** > **Channels** > **Text messages** and selecting **+New text message** in the top ribbon. This will take you to the text messaging editor.

To create a message[^1]:

1. Select the message sender. The **Text message sender** dropdown lets you choose from the sender phone numbers (Azure Communication Services preview, Twilio, or TeleSign) you’ve added.
2. Enter your message content. You can enter text, emojis, and [personalized content](https://learn.microsoft.com/en-us/dynamics365/marketing/real-time-marketing-outbound-text-messaging#personalize-text-messages).
3. Choose whether your message designation is **Commercial** or **Transactional**. A commercial message is one that is sent to recipients who have opted-in to receive messages. An example is a coupon sent to a group of customers who opted-in to receive promotional offers from your company. A transactional message is one that is sent in response to a transaction the recipient previously started with you. An example is a response to an email inquiry.

> > ###### Note
> > In the text messaging editor, the message designation is preselected as transactional for numbers that might be prone to carrier filtering if used for promotional or marketing messaging. To make sure your number isn't blocked by carriers, it's highly recommended to use this number for transactional messaging only.

Before sending your message, select the **Check content** button in the upper right. This will run an error check on the message, much like the error check functionality in the email designer.

Next, test your message by selecting the **Test send** button in the upper right. If you’re using an Azure Communication Services preview toll-free sender number, you can test send the message to any United States mobile number. If you’re using a Twilio or TeleSign sender number, you can send the message to a mobile device in any supported country. You can also add the message to a journey to see how it can be triggered by events.

### Personalize text messages

Personalizing text messages allows you to insert dynamic data that is unique to each message recipient. You might want to dynamically populate a name, an appointment time, a location, or any other unique data.

To personalize a text message:

1. Select the **Personalization**
2. button in the **Message** field.
3. Select **Select a data field** to choose a data source. Your data source can be based on an **Audience**, a **Trigger**, or **Compliance**.
4. After choosing the data source, you can search for the specific attribute or trigger you want.
5. Add a **Label** to quickly identify your token in the message content.

When you send the text message from a journey, it will automatically populate the token according to the attribute you selected.

### Add SMS keywords to a text message

Adding SMS keywords in your text message allows you to use them in your customer journey to branch it based on your customer’s response to your text messages.

To add a keyword to a text message:

1. Select the keyword icon.
2. Type the keyword that you’d like to add.
3. Select it from the list if it has been used previously in the journey or select the **New keyword** button to create it.

The following screenshot shows how to add SMS keywords in your text message.

All keywords created through the SMS editor are also added to the [SMS keywords page].

### Track your text message metrics from channel insights

You can see how customers react to your text messages by checking the text message analytics in the message itself and within journeys.

> > ###### Note
> > Delivery reports for text messages are received from different carriers in every country or region. This might result in false positives or negatives at times, depending on the carrier. Consider this when you check the delivery reports of your text messages.

[^1]: [Microsoft Docs: Real-Time Marketing Outbound Text Messaging](https://docs.microsoft.com/en-us/dynamics365/marketing/real-time-marketing-outbound-text-messaging)

## Use Text Message Reports

While Text Messaging does accommodate Insights analytics when used in a Journey, individual text message records do not have a report.  Instead, you can use the Text Messages Report to see how customers are responding to your text messages.  To use this feature:

1. Navigate to a text message record that has been sent.
2. Click on the "Reports" tab.
3. Here you will see delivery trends and delivery statuses.

To see detailed delivery and interaction information, do the following:

1. Click on the "Design" tab in your text message record.
2. See the "Text message analytics" panel on the right-hand side of the page.
3. If the panel contains an overview, there should also be a link at the bottom of the panel called "Delivery and interaction details".  Click on this link to see detailed delivery and interaction information.

The detailed delivery and interaction details will give you a report on the number of messages that were Sent and Delivered for this text message record, as well as detailed information on reasons why messages were either blocked or not delivered.