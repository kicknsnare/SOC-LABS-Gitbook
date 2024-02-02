# 100 Series Questions

The questions below are from the BOTSv2 dataset, questions 100-104. Some additional questions were added.&#x20;

In this task, we'll attempt to help guide you to each question's answer.

Note: The approach outlined in this task is not the only approach to tackle each question. \


Reading the questions below, the focus is on Amber Turing and her communication with a competitor.

Question 1

The first objective is to find out what competitor website she visited. What is a good starting point?

When it comes to HTTP traffic, the source and destination IP addresses should be recorded in logs. You need Amber's IP address.\


You can start with the following command, `index="botsv2" amber`, and see what events are returned. Look at the events on the first page.&#x20;

Amber's IP address is visible in the events related to PAN traffic, but it's not straightforward.&#x20;

To get her IP address, we can hone in on the PAN traffic source type specifically.&#x20;

Command: `index="botsv2" sourcetype="pan:traffic"`

From here, you should have Amber's IP address. You can build a new search query using this information.

It would be best if you used the HTTP stream source type in your new search query.&#x20;

Using Amber's IP address, construct the following search query.&#x20;

Command: `index="botsv2"`` `_`IPADDR`_` ``sourcetype="stream:HTTP"`

You must substitute IPADDR with Amber's IP address.

After this query executes, there are many events to sift through for the answer. How else can you narrow this down?

Look at the additional fields.

Another field you can add to the search query to further shrink the returned events list is the site field.

Think about it; you're investigating what competitor website Amber visited.

Expand the search query only to return the site field. Additionally, you can remove duplicate entries and display the results nicely in a table.&#x20;

Command: `index="botsv2"`` `_`IPADDR`_` ``sourcetype="stream:HTTP" |`` `_`KEYWORD`_` ``site |`` `_`KEYWORD`_` ``site`

You must substitute KEYWORD with the Splunk commands to remove the duplicate entries and display the output in a table format.

Note: The first KEYWORD is to remove the duplicate entries, and the second is to display the output in a table format.&#x20;

The results returned to show the URIs that Amber visited, but which website is the one that you're looking for?

To help answer these questions: Who does Amber work for, and what industry are they in?&#x20;

The competitor is in the same industry. The competitor website now should clearly be visible in the table output.

Extra: You can also use the industry as a search phrase to narrow down the results to a handful of events (1 result to be exact).&#x20;

Command: `index="botsv2"`` `_`IPADDR`_` ``sourcetype="stream:HTTP"`` `_`*INDUSTRY*`_` ``|`` `_`KEYWORD`_` ``site |`` `_`KEYWORD`_` ``site`

Note: Use asterisks to surround the search term.

Questions 2-7

Amber found the executive contact information and sent him an email. Based on question 2, you know it's an image.

Since you now know the competitor website, you can construct a more specific search query isolating the results to focus on Amber's HTTP traffic to the competitor website.&#x20;

Command: `index="botsv2"`` `_`IPADDR`_` ``sourcetype="stream:HTTP"`` `_`COMPETITOR_WEBSITE`_

Replace COMPETITOR\_WEBSITE with the actual URI of the competitor website.&#x20;

You can expand on the search query to output the specific field you want in a table format for an easy-to-read format, as we did for the previous objective. \


Based on the image, you have the CEO's last name but not his first name. Maybe you can get the name in the email communication.

You can now draw your attention to email traffic, SMTP, but you need Amber's email address. You should be able to get this on your own. :)

Once you have Amber's email address, you can build a search query to focus on her email address and the competitor's website to find events that show email communication between Amber and the competitor.&#x20;

Command: `index="botsv2" sourcetype="stream:smtp"`` `_`AMBERS_EMAIL`_ _`COMPETITOR_WEBSITE`_

Replace AMBERS\_EMAIL with her actual email address.&#x20;

With the returned results from the above search query, you can answer your own remaining questions. :)
