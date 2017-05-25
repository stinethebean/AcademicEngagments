# Azure Educator Portal For Professors & TAs #

**Updated May 2017**  Note, these are not in a particular order, but I hope they'll help. The Azure Educator Portal is in still in preview, hence a few workarounds to get ideal behavior. 

## Best practices for configuring on the Azure Educator Portal ##
1. Using Edge, Chrome or FireFox (usually in incognito/in-private mode) deems the best results when accessing https://www.microsoftazuresponsorships.com/ We have noticed irregular behavior when using Safari
2. As soon as you know how many subscriptions you'll need (usually one per student, or one per group) put in a request for bulk subscription creation. It's much easier to add users to subscriptions than it is to add more subscriptions. 
3. Create an email address for you and your TAs to use and share. Ideally you'll have created a new email address which the Azure grant is tied to. (Otherwise your personal email will get bombarded with Azure notifications) If you then add that email to each subscription, it'll make it easier for the staff to support students and see what's going on.
4. Have students give you their not @university.edu email addresses, and use those for their Azure Subscription. We find that ~7% of the students who used their @[university].edu account do not receive the inital invite email.

## Can I request a bulk creation of subscriptions? ##
Yes!
Fill out [the template](https://github.com/stinethebean/AcademicEngagments/blob/master/Azure_Educator_Services_Template.xlsx), you can find a [sample here](https://github.com/stinethebean/AcademicEngagments/blob/master/Azure_Educator_Services_sample.xlsx)

Then go to http://aka.ms/azdesk and file a ticket requesting subscription creation with the file attached.

## Some of my students haven't received the invite to Azure email ##
We ran into the same issue at Stanford, ~7% of the students who used their @[university].edu account did not receive the email. This is due to an Azure issue with organizational (i.e. Georgia Tech, Stanford) accounts. 

**Solution 1:** Many times we see spam and clutter filters eat the email.  Make sure students do a search for invites@microsoft.com in their inbox and spam folders.
              The email should look like this: 

 <img src="http://i.imgur.com/Pk2ikIy.jpg" width="300">    

 **Solution 2:** Have the students who didn't receive the email, give you a non-@university.edu account (@outlook.com, @gmail.com, etc.) and go back to the Azure Educator Portal and manually add that one.


## Azure Educator Portal Showing a zero-balance ##
If you've recently been granted an Azure Educator Grant, you might run into an issue where you see a $0 balance in the **Educator Portal**, but your full grant under **Balance.** 
For example:

at https://www.microsoftazuresponsorships.com/Manage you see
<img src="http://i.imgur.com/ESYgbJu.png" width="500">

and at https://www.microsoftazuresponsorships.com/Balance you see 
<img src="http://i.imgur.com/rueFI7p.png" width="500">

**How do you resolve this?**
1. Go to your email, and search for "Your Microsoft Azure sponsorship for email@address.com "
2. Find the **Activate** button and click it on again (ideally in an in-private/incognito window) 

<img src="http://i.imgur.com/3Yo6jDb.png" width="500">


## Educator Portal Showing Active while Azure Portal Shows Disabled ##
Sometimes we see a glitch in the matrix or a Schrodinger’s Azure Subscription, with a subscription showing Active in the Educator Portal and showing Disabled in the Azure Portal. (see images below)

https://www.microsoftazuresponsorships.com showing this:
<img src="http://i.imgur.com/Oyj7QhZ.jpg" width="500">

https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade showing this: 
<img src="http://i.imgur.com/RKoMsQr.jpg" width="500">

1.	In the Azure Educator Portal,  move the Subscription to canceled & SAVE
b.	Refreshed the page
2.	Verified in Azure Portal, that the subscription is still disabled there
a. You can do this by going to Subscriptions (on the right side, looks like a yellow key)
3.	In the Azure Educator Portal, move the subscription to Active & SAVE
a.	Refresh the page
c.	Verified that the subscription is still set to Active
d.	NOTE – at this point, the Azure Portal, might still showed it as disabled
4.	In the Azure Educator Portal
a.	Set the cap to at least $50 more than their current state & SAVE
b.	Refreshed the page
5.	Wait about 5 minutes
a.	Checked the Azure Portal again, and the subscription should as active and match the Educator Portal


## I'm seeing Duplicate Subscriptions & My students can't access them ##
If you're seeing something like the following image, where you have 2 instances of the same subscription in your Academic Educator Portal, don't be alarmed. This is a known bug. 
<img src="http://i.imgur.com/7uI7ftE.png" width="500"> 

File a ticket at http://aka.ms/azdesk with a screenshot, and the team will work to fix it for you.
