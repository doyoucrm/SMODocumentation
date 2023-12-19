# First Time: Creating Segments

[comment]: <> (Export To: `../Web/02_07_CreatingSegments.html`)

**In this article**
    <br>[About Marketing Segments](#about-marketing-segments)
    <br>[Create Marketing Segments](#create-marketing-segments)
    <br>[Use Segment Insights](#use-redirect-url-insights)

## About Marketing Segments

Marketing segments in Dynamics 365 Customer Insights are a way to define groups of customers based on specific criteria. Segments are essential for targeting and personalizing marketing initiatives such as email campaigns and customer journeys. There are two types of segments in Dynamics 365 Customer Insights: dynamic segments and static segments.

* **Dynamic Segments:** Dynamic segments are defined by a set of rules and conditions and are constantly updated based on the information in your database. They automatically include customers who meet the defined criteria. For example, you can create a dynamic segment for "construction customers who have rented front loaders from us in the past 6 months" or "contacts who visited our booth at last month's conference". Dynamic segments are ideal for targeting specific customer groups with tailored marketing messages.
* **Static Segments:** Static segments are manually populated by adding contacts explicitly, one at a time. Unlike dynamic segments, static segments do not update automatically based on database information. Static segments can be useful when you want to create a fixed group of contacts for a specific purpose.

Marketing segments can consist of blocks of queries that are based on profiles, interactions, or other segments.  Query blocks are used to define the criteria for a segment. There are two types of query blocks in Dynamics 365 Customer Insights:

* **Profile Blocks:** Profile blocks query the profile records stored in the marketing-insights service. These profile records you work with in the Dynamics 365 UI, such as contacts, accounts, leads, and others. The profile records are synchronized between your Dynamics 365 organizational database and the marketing-insights service. By querying the profile records, you can create segments based on customer attributes and characteristics, such as demographics or firmographics. Profile blocks are ideal for targeting specific groups of customers based on their profile information, such as age, location, or industry affiliation.
* **Behavioral Blocks:** Behavioral blocks query the interaction records stored in the marketing-insights service. These interaction records are automatically generated and capture customer interactions, such as opening an email, clicking an email link, submitting a form, or registering for an event. Behavioral blocks enable you to target customers who have taken specific actions or engaged with your marketing content. For example, you can create a segment of customers who have clicked on a particular product link in an email, or who have visited a particular web page.

> > ###### Note
> > It's important to note that profile blocks query the synced profile records, which include entities like contacts, accounts, and leads. On the other hand, behavioral blocks query the interaction records generated in response to customer interactions, but these records are not synced to the Dynamics 365 organizational database.
<br>

You can combine these blocks of queries based on profiles, interactions, or other segments. By utilizing both profile and behavioral blocks, you can create targeted segments that consider both customer attributes and engagement behavior. These segments will enable you to deliver personalized and tailored marketing messages to specific groups of customers, optimizing your marketing efforts as a John Deere dealership marketing admin.

## Create Marketing Segments

In this section, you will learn how to create marketing segments in Dynamics 365 Customer Insights. You will create a dynamic segment based on profile information and a static segment based on a list of contacts.

### Create a Dynamic Segment
Dynamic marketing segments allow you to group contacts based on specific criteria. Dynamic segments automatically update their membership as contacts meet or no longer meet the set criteria. Follow the instructions below to create your first dynamic segment.

#### Step 1: Create a New Dynamic Segment

1. In **Real-time marketing**, navigate to **Segments** under the "Audience" section.
2. Click on "New" to start creating a new segment.
3. Choose "Dynamic segment" from the options. This allows you to create a segment based on logical expressions and queries, which will automatically update as contacts meet the criteria.

#### Step 2: Choose a Segment Template (Optional)

1. A "Segment template" dialog box will appear, showing a list of available templates. These templates provide predefined or partially defined queries designed for specific purposes.
2. Select a template to read more about it in the information panel. You can use the "Filter" and "Search" features to find the desired template.
3. Click "Select" to load a template, or click "Cancel" to build a new segment from scratch.

#### Step 3: Design Your Dynamic Segment

1. If you selected a template, it will load, and you can skip this step. If you chose "Cancel" in the previous step, a blank designer will open.
2. Begin by selecting a query block (e.g., profile block, interaction block, or another segment). You can add other blocks and choose the relationship between the blocks (e.g., "or," "and also," "but not").
3. Name your segment at the top of the segmentation canvas.

> > ###### Note
> > As you work with segments, you may find that you want to create a segment based on some kind of interaction your customers have with your marketing content. For example, you may want to create a segment of customers who have clicked on a particular link in an email. You can easily do this by choosing a behavioral block when setting up your marketing segment, and then selecting the specific interaction you want to track.
<br>

#### Step 4: Save Your Segment

1. Click "Save" on the toolbar to save your newly created segment.

#### Step 5: Define Your Segment Membership Criteria

1. Use the tools provided in the designer to establish your segment membership criteria. For example, you may want to target contacts living in a specific city or those who have shown interest in a particular product.

#### Step 6: Go Live with Your Segment

1. Once you have designed your segment, click "Go live" on the toolbar. This will start running the segment, find all its members, and make it available for use in customer journeys.
2. After going live, you can check the "Members" tab to see which contacts are part of the segment.

### Create a Static Segment

A static marketing segment is a fixed list of contacts that you manually select, rather than a dynamic segment that automatically updates based on certain criteria. Follow the steps below to create your first static segment:

#### Step 1: Create a new static segment

1. In **Real-time marketing**, navigate to **Segments** under the "Audience" section.
2. Click on "New" to create a new segment.
3. Choose "Static segment" from the options presented.

#### Step 2: Set up basic segment information

1. A quick create panel will appear, prompting you to provide a name for your new static segment.
2. You can also add an optional description to help you remember the purpose of this segment.
3. Select the appropriate time zone for your segment.
4. Click on "Save" at the bottom of the quick create panel to save your new static segment.

#### Step 4: Add members to the static segment

1. With your static segment created, you can now add contacts to it.
2. Open the record (if it needs to be opened), then go to the "General" tab in the static segment designer.
3. Click the "Add" button to search for and select individual contacts to include in your segment.
4. Alternatively, use the "Add by Query" button to create a query that filters your contacts based on certain criteria. This will display a list of contacts that match your query.
5. Select the contacts you want to add to your segment from the query results, and click "Add selected." If you want to include all contacts from the query, click "Add all."

#### Step 5: Remove members from the static segment (optional)

1. If needed, you can also remove contacts from your static segment.
2. Click the "Remove by Query" button and create a query to filter the contacts you want to remove.
3. From the list of contacts generated by the query, select the contacts you want to remove, and click "Remove selected." To remove all contacts from the query, click "Remove all."

#### Step 6: Go live with your segment

1. Once you've added all the desired contacts to your static segment, click "Go live" in the toolbar.
2. This will make your segment available for use in customer journeys.

## Use Segment Insights

Marketing Segment Insights provide an analytical view of how the membership of a specific segment changes over time. Segments are groups of contacts that share common characteristics or behaviors, which can be used for targeted marketing campaigns. With Marketing Segment Insights, you can track and measure the effectiveness of your marketing efforts by understanding how your audience responds to your initiatives.

Marketing Segment Insights gathers data on your segment membership and presents it in an easy-to-understand format within Dynamics 365 Marketing. This allows you to monitor membership changes, identify trends, and make informed decisions for your marketing campaigns.

To see your Segment Insights, follow these steps:

1. In **Real-time marketing**, click on **Segments** in the "Audience" section.
2. Choose the segment you want to analyze by clicking on its name in the list of available segments.
3. Once you've opened the segment record, click on the "Insights" tab to access the Marketing Segment Insights.
4. You will now see a graphical representation of how the membership of your selected segment has changed over time. Use this information to understand trends and the impact of your marketing initiatives on the segment.
5. To analyze the data more thoroughly, use the date range filter at the top of the Insights tab. You can set the "From" and "To" dates to focus on a specific time frame.
6. Explore different aspects of your segment insights by hovering your mouse pointer near the value you're interested in. An info icon will appear, and when you hover on this icon, a tooltip with a description of that value will be displayed.

By following these steps, you can leverage Marketing Segment Insights to better understand your audience and make data-driven decisions for your segment-driven marketing campaigns and journeys.