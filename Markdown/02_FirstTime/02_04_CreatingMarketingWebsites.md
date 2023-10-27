# First Time: Creating Marketing Websites

[comment]: <> (Export To: Web/02_04_CreatingMarketingWebsites.html)

**In this article**
    <br>[About Marketing Websites](#about-marketing-websites)
    <br>[Create a Marketing Website](#create-a-marketing-website)
    <br>[Use Marketing Websites Insights](#use-marketing-websites-insights)

## About Marketing Websites

Marketing Websites in Dynamics 365 Marketing allow you to monitor and analyze the online behavior of both known contacts and anonymous visitors on your website. This is achieved through the use of tracking scripts, which are unique JavaScript codes that you will need to add to each page of your website that you want to monitor. The tracking scripts use cookies to record each page request from individual browsers. For example, when a visitor submits a Marketing-enabled form or clicks a link in an email sent from Dynamics Marketing, they will no longer be anonymous, and the system can then link their browsing history to their contact record in Dynamics 365 Marketing.

## Create a Marketing Website

The following steps will guide you through the process of creating a Marketing Website in Dynamics 365 Marketing, retrieve a tracking script, and add it to your website.

### Before you get started...

Although not required, you may want to authorize your domain before creating a Marketing Website.  See the article [Authenticate Your Domain](../../01_Setup/Web/01_01_AuthenticateYourDomain) for more information.

### Create a website

1. Go to **Marketing** > **Internet Marketing** > **Marketing websites** to view the list of existing websites.
2. Click "New" to create a new Website record, and fill in the required fields, such as Name, URL, and Description. The Timeout setting determines the duration of inactivity before a new session starts for a given browser. The default of 20 minutes is typically sufficient.
3. Save the record.

### Setup tracking tokens

The previous steps will result in a Website record.  When these records are created, the system automatically generates a unique tracking script in the "JavaScript code" field for the new record.

To enable tracking on one or more of your website's pages, you will need to copy this code and share it with your webmaster to ensure it gets placed on the footer of the relevant pages of your website where you would like tracking enabled.

## Use Marketing Website Insights

Marketing Website Insights are part of the Dynamics 365 Marketing platform, which helps you track and analyze visitor interactions on your website. These insights provide data on the most popular pages on your site, visitor locations, page visits, form visits, and form submissions. By understanding this information, you can make data-driven decisions to optimize your website and marketing efforts, ultimately increasing engagement and lead generation.

To use Marketing Website Insights, you must have a Marketing Website created and published. For more information, see [Create a Marketing Website](#create-a-marketing-website).  Then follow these steps:

1. Navigate to **Outbound marketing** > **Marketing websites**.
2. Find and select the website record you want to analyze. This will take you to the website record details page.
3. Open the "Insights" tab located at the top of the page.

Now that you have accessed the Marketing Website Insights, you should be able to explore the following areas:

* Overview: This section provides a list of the most popular website pages that are tracked by Dynamics 365 Marketing, as well as a map displaying the geographic locations of your visitors. Use this information to understand which pages are generating the most interest and where your audience is based.
* Visits: In this section, you will find a table displaying details about each time a page with a Dynamics 365 Marketing script was loaded. This information can help you identify trends in visitor engagement and track the performance of specific pages.
* Form visits: This table lists each time a contact (known or anonymous) opened a page on your website containing an embedded or captured marketing form. Analyzing form visits can help you understand which forms are attracting more attention and where they are located on your site.
* Form submissions: This section shows a table listing each time a contact submitted an embedded or captured marketing form from your website. By hovering your mouse pointer over a value in the Form submissions column, you can view the values sent with any listed submission. Use this data to track the effectiveness of your forms and identify potential areas for improvement.  Form submission insights can also be viewed from the form record details page. For more information, see [Creating Marketing Forms](#02_05_creatingmarketingforms.html).

As a John Deere dealership marketing admin, you can use this information to make data-driven decisions and improve the overall effectiveness and performance of your marketing website.