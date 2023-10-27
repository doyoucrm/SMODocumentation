# First Time: Creating Redirect URLs

[comment]: <> (Export To: Web/02_06_CreatingRedirectUrls.html)

**In this article**
    <br>[About Redirect URLs and Tracking Scripts](#about-redirect-urls-and-tracking-scripts)
    <br>[Create a Redirect URL](#create-a-redirect-url)
    <br>[Use Redirect URL Insights](#use-redirect-url-insights)

## About Redirect URLs and Tracking Scripts

Redirect URLs and Tracking Scripts are powerful tools in Dynamics 365 Marketing that help you track and analyze the performance of your marketing efforts. By using Redirect URLs to monitor link clicks and Tracking Scripts to observe user behavior on your website, you can make data-driven decisions that ultimately improve the effectiveness of your marketing campaigns for your John Deere dealership.

### Redirect URLs

Redirect URLs are special links that pass through your Dynamics 365 Marketing server before directing the user to the actual content they are interested in. When a user clicks on a Redirect URL, Dynamics 365 Marketing logs the click, records details about the user (such as their physical location), and then redirects the user to the target page.

Redirect URLs can help you track the effectiveness of your marketing efforts by measuring how many people clicked on each link and which channels, such as social media posts or banner ads, drove the most traffic. This data helps you understand which channels are having the greatest impact and informs you on areas that need improvement or should be abandoned.

Unlike Tracking Scripts, Redirect URLs do not require any additional setup on your website. Instead, you can simply copy and paste the generated link into your marketing content.

### Tracking Scripts

Tracking Scripts are snippets of JavaScript code that you add to your website pages to enable Dynamics 365 Marketing to monitor user activity on your site. By adding Tracking Scripts to your website, you can collect valuable data on how users interact with your site, which pages they visit, and how long they spend on each page.

To use Tracking Scripts effectively, you need to first create a Marketing Website record (which will automatically generate a tracking script for you) add then add the JavaScript code generated by Dynamics 365 Marketing to each page on your website that you want to track. This can be done by inserting the code into the page templates in your Content Management System (CMS).  If you are not familiar with JavaScript or HTML, you may need to consult with your web developer to ensure that the code is properly added to your website.

Also, see the article on [marketing websites](02_04_CreatingMarketingWebsites.html) article for more information on creating a Marketing Website record.

### Why this is only an Outbound feature

In Dynamics 365 Marketing, the features are divided into two main areas: Outbound Marketing and Real-time Marketing. The primary reason for this separation is the difference in their approach and focus when it comes to marketing activities.

Outbound Marketing focuses on traditional marketing methods, such as email campaigns, marketing pages, and social media posts, which are usually targeted at a broader audience. Redirect URLs and Tracking Scripts are a part of Outbound Marketing because they are designed to track user engagement with these broader marketing initiatives. They help you measure the effectiveness of your campaigns, monitor link clicks, and analyze user behavior on your website.

Since Redirect URLs and Tracking Scripts are designed to track user engagement with broader marketing initiatives rather than real-time, personalized interactions, they are not available in the Real-time Marketing area.

## Create a Redirect URL

To create your first Redirect URL in Dynamics 365 Marketing:

1. Navigate to **Marketing** > **Internet Marketing** > **Redirect URLs**. This will display the current list of Redirect URLs set up in the system.
2. To create a new Redirect URL, click on "New" on the command bar.
3. A new Redirect URL record will open. Fill out the required information and settings:
    * **Name:** Enter a name for the Redirect URL record. Use a descriptive name that reflects how and where you plan to use the link, such as "Facebook Fall Promotion."
    * **Original URL:** Enter the URL of the page or download that should open when someone clicks on the Redirect URL (after being logged and forwarded from the Dynamics 365 Marketing server).
4. Click "Save" to save your work and generate the Redirecting URL.
5. You will now see a field called "Redirecting URL." This is the Redirect URL generated by Dynamics 365 Marketing. Copy the URL and use it wherever you want to post the link (e.g., social media posts, email campaigns, or banner ads).

By following these steps, you have successfully created your first Redirect URL in Dynamics 365 Marketing. Now, you can use this Redirect URL to track the effectiveness of your marketing efforts across different channels and gain insights into how users interact with your promotional content.

## Use Redirect URL Insights

Redirect URL Insights is a feature in Dynamics 365 Marketing that helps you track and analyze how people interact with the redirect URLs in your marketing campaigns. This feature provides you with an overview of where people were when they clicked on the redirected link and a detailed timeline of each click.

Follow these step-by-step instructions to access and utilize redirect URL insights in Dynamics 365 Marketing:

1. Navigate to **Outbound marketing** > **Redirect URLs**.
2. Choose a specific redirect URL record that you would like to analyze by clicking on it.
3. Open the "Insights" tab located within the redirect URL record.

Here, you will see two categories:

* Overview: This section displays a map that shows the geographical locations of people when they clicked on the redirected link. This information can help you understand the regional interest in your campaigns and target your marketing efforts accordingly.
* Timeline: This section shows a table with details about each time the redirect URL was clicked. You can view the date, time, and location of each click, helping you identify trends and patterns in user behavior.

By analyzing this data, you can gain valuable insights into how your target audience interacts with your marketing campaigns and adjust your strategies accordingly.