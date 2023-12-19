# System Setup: Text Messaging Providers

**In this article**
<br>[How does text messaging work in Dynamics 365 Marketing?](#how-does-text-messaging-work-in-dynamics-365-marketing)
<br>[Setup Text Messaging](#setup-text-messaging)

[comment]: <> (Export To: `../Web/01_03_TextMessaging.html`)

## How does text messaging work in Dynamics 365 Marketing?

Microsoft Dynamics 365 Marketing offers a range of communication channels to engage with your customers, and one of them is text messaging. With this feature, you can send SMS messages to your customers directly from Dynamics 365 Marketing.

To start using text messaging in Dynamics 365 Marketing, you need to have a valid SMS provider account and set it up in your Dynamics 365 Marketing instance. Once you have set up your SMS provider, you can create SMS message templates, configure opt-in and opt-out settings, and target specific customer segments.

When you send an SMS message from Dynamics 365 Marketing, the system automatically tracks the delivery status and response rates of each message. This allows you to measure the effectiveness of your SMS campaigns and adjust your marketing strategies accordingly. Overall, text messaging in Dynamics 365 Marketing offers an effective way to reach your customers on their mobile devices and boost your marketing efforts.

### What kind of messages can be sent?
There are two types of SMS messages that can be sent from Dynamics:  Transactional and Commercial.

* **Transactional** messages are intended for notifications or status updates (such as appointment confirmations, links to account or statements, notification of a receipt of goods, etc.).
* **Commercial:** Unsolicited or solicited communications regarding products or services, for the purpose of guiding a contact through a marketing journey or for collecting marketing analytics.

>###### Note
> It is important to be mindful of these types of message designation when creating Text Messages for use in marketing journeys/campaigns.  There may be certain laws that may need to be adhered to that govern when _Commercial_ messages may be sent, while _Transactional_ messages are far less restricted as long as they are used appropriately.
<br>

## Setup Text Messaging

While Microsoft is investing in enabling Azure Communication Services to send and receive text messages in Dynamics 365, this capability is currently in beta.  In the future, this should provide a more turnkey way of handling the setup and billing for marketing text messages as a feature.  However, Dynamics Marketing can also be configured with _Custom Providers_ which allow you to integrate third-party providers like Twilio to enable these features.

The process of setting up Twilio and connecting it to Dynamics 365 involves the following steps:

1. Create a new Twilio account and get your API keys.
2. Configure a new SMS Provider in Dynamics and walk through the wizard.
3. Enable reply messages in Dynamics.
4. Create keywords in Dynamics.

### 1. Setup Twilio
1. Sign up for a Twilio account: Go to the [Twilio](https://www.twilio.com/try-twilio) website and sign up for a new account. You'll need to provide some basic information about yourself and your organization(fn).
2. Verify your account: Once you've signed up, you'll need to verify your account by clicking on the verification link that Twilio sends to your email address.
3. Get a Twilio phone number:  If you've just signed up for Twilio, you can request a trial phone number to use while getting everything else setup.  You can do this by heading to your [Twilio console](https://console.twilio.com/) and clicking the **Get a Trial Number** button.  Alternatively, may can [buy](https://console.twilio.com/us1/develop/phone-numbers/manage/search?frameUrl=%2Fconsole%2Fphone-numbers%2Fsearch%3Fx-target-region%3Dus1&currentFrameUrl=%2Fconsole%2Fphone-numbers%2Fsearch%3FisoCountry%3DUS%26searchTerm%3D%26searchFilter%3Dleft%26searchType%3Dnumber%26x-target-region%3Dus1%26__override_layout__%3Dembed%26bifrost%3Dtrue) a Twilio number or [port in](https://console.twilio.com/us1/develop/phone-numbers/port-host/port-number?frameUrl=%2Fconsole%2Fphone-numbers%2Fporting-requests%2Fport%3Fx-target-region%3Dus1) an existing phone number to the service.
4. Get your Twilio API credentials: In order to send text messages from Microsoft Dynamics 365 Marketing using Twilio, you'll need to obtain your Twilio API credentials. To do this, head to your Twilio console's **Account Info** section.  Here you will see your "Account SID" and "Auth Token" values, which you will use to setup an _SMS Provider_ in Dynamics 365 down below.

>###### Note
> If you buy or port a toll-free phone number in Twilio, you will not be able to send certain content (such as URLs and attachments) until your toll-free phone number has been verified(fn).
<br>

### 2. Setup an SMS Provider
1. In Dynamics Marketing, navigate to the Settings area, and then click on SMS Providers.
2. Click "New" to create launch the **New SMS Provider** wizard.
3. Choose "Twilio" and then click "Next".
4. **Settings**:
    1. Enter the following details:
        1. Name (whatever name you want for this provider)
        2. Description
        3. Account SID (which you can get from your Twilio dashboard)
        4. Auth Token (which you can get from your Twilio dashboard)
    2. Copy the **Incoming callback URL** value and paste it into the **Messaging Service** section of your Twilio dashboard.  This will enable you to receive text message responses from your contacts directly in Dynamics 365 Marketing.
    3. Click "Next" to continue.
5. **Phone Numbers**:
    1. Click "Add" to add a phone number.
    2. Enter the following details:
        1. Phone Number (which you can get from your Twilio dashboard)
        2. Friendly Name (which you can get from your Twilio dashboard)
    3. Click "Next" to continue.
6. **Test**:
    1. Click "Test" to test the connection to Twilio.
    2. If the test is successful, click "Finish" to complete the wizard.
    3. If the test fails, click "Back" to go back and check your settings.

### 3. Enable reply messages
1. Open the SMS Provider record you created in the previous steps.
2. Click the **Settings** tab.
3. Copy the "Incoming callback URL" value.
4. Log back into your [Twilio console](https://console.twilio.com/) and use the navigation panel on the left-hand side of the page, browse to **Develop** (the tab at the top) > **Phone Numbers** > **Manage** > **Active Numbers**.
5. Your phone number(s) will be displayed in a grid.  Click to open a phone number that has been also configured under a SMS Provider in Dynamics.
6. In the phone number's **Configure** tab, scroll down to the **Messaging** section and find the three fields under the label "A MESSAGE COMES IN".
7. Replace the default webhook URL with the "Incoming callback URL" value that you copied in step 3.
8. Click "Save".

### 4. Create keywords in Dynamics
SMS keywords may be required by messaging service providers (like Twilio) to prevent your messages from being classified as spam.  For example, failing to include a "STOP" keyword in certain scenarios can cause the message to get caught in a service provider's spam filter and the message.

To create a keyword:

1. In the Dynamics Marketing app, navigate to the Settings area, then click on SMS keywords.
2. Click the "New keyword" button.
3. In the pop-up window, enter a keyword (such as "STOP" without any spaces or special characters).
4. Click the "Create" button.

Once keywords are created, they can be added to marketing text messages in the Text Message designer.