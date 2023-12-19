# First Time: Using Dynamic Content Tags

[comment]: <> (Export To: `../Web/02_01_UsingDynamicTags.html`)

**In this article**
<br>[What are Dynamic Content Tags?](#what-are-dynamic-content-tags)
<br>[Where are Dynamic Content Tags used?](#where-are-dynamic-content-tags-used)
<br>[Using the Dynamic Content Tags](#using-the-dynamic-content-tags)

## What are Dynamic Tags?

In Microsoft Dynamics 365 Marketing, Dynamic Content tags are used to insert personalized content or execute specific logic within email templates. These tags are enclosed in double braces ({{ and }}) and can represent standard field values or advanced programming constructs. By incorporating Dynamic Content tags, marketers can create more relevant and engaging content that is tailored to each recipients' specific details, preferences, and behaviors, which results in engagements and interactions which feel more targeted and individualized.

The Dynamic Content system in Dynamics Marketing supports conditional statements, comparisons, and loops.  When used, these allow marketing users to generate content and campaigns which can be highly dynamic.

To use dynamic tags in Microsoft Dynamics 365 Marketing app, you must first create a template that contains the placeholders for dynamic content. You can then merge this dynamic content for the correct fields using the appropriate marketing list. The merged data replaces the placeholders and creates an email message for each recipient with personalized and relevant information. The use of dynamic tags can help to personalize communication with customers and build better relationships.

To create a dynamic tag in the Microsoft Dynamics 365 Marketing app, follow these steps:

	1. Select the Email messages tab in the Dynamics 365 Marketing app.
	2. Select the message to which you want to add dynamic content.
	3. Click Content to edit the content of the selected message.
	4. Choose the location where you want the dynamic content to appear and click the dynamic content placeholder button.
	5. Select the type of content you want to place into the dynamic tag.
	6. Insert the dynamic tag into the message content and save the message.

Remember to select the appropriate marketing list to merge with the dynamic content. This will ensure that the right data is included in the message for each recipient.

## Where are Dynamic Tags used?

Dynamic Content tags are supported in the following areas of the Microsoft Dynamics 365 Marketing app:

	* Email messages
	* Landing pages
	* Web forms
	* Web pages
	* Web links
	* Web links in email messages
	* Web links in landing pages
	* Web links in web forms
	* Web links in web pages

## Using the Dynamic Tag wizard

At a very high level, create a dynamic tag in the Microsoft Dynamics 365 Marketing app basically involves the following steps:

	1. Select the Email messages tab in the Dynamics 365 Marketing app.
	2. Select the message to which you want to add dynamic content.
	3. Click Content to edit the content of the selected message.
	4. Choose the location where you want the dynamic content to appear and click the dynamic content placeholder button.
	5. Select the type of content you want to place into the dynamic tag.
	6. Insert the dynamic tag into the message content and save the message.

However, to fully leverage the Dynamic Content system, you a little basic understanding of scripting and programming will be required.  For example, **advanced dynamic content tags** might involve conditional statements, comparisons, and loops, which are programming concepts.  The below sections will provide a brief overview of these concepts.

### Conditional Statements and Comparisons

Conditional statements use "if-then-else" logic to display content based on whether expressions resolve to true or false. Use the following syntax for conditional statements:

```handlebars
{{#if (<operator> <value1> <value2>)}}
    Content displayed when the expression is true
{{else if (<operator> <value1> <value2>)}}
    Content displayed when the first expression is false and the second one is true
.
.
.
{{else}}
    Content displayed when all expressions are false
{{/if}}
```

Operators for conditional expressions include: eq (equal to), ne (not equal to), lt (less than), gt (greater than), lte (less than or equal to), and gte (greater than or equal to).

### For-Each Loops

For-each loops allow you to iterate through a collection of records related to a specific current record. Use the following syntax for for-each loops:

```handlebars
{{#each Entity.RelationshipName }}
    ...
    {{this.RelatedField1}}
    ...
    {{this.RelatedField2}}
    ...
{{/each}}
```

### Entering Advanced Dynamic Content

To enter advanced dynamic content in the designer, follow these tips:

* Use custom-code elements for better visibility and reliability.
* Remove extra spaces and carriage returns added by the designer that can break your code.
* Ensure dynamic-content code is contained within a set of start and end tags or within an HTML comment.
* Use the personalization feature to construct expressions that fetch values from your database.
* Test your dynamic content thoroughly before sending it to your audience to ensure it works as expected.