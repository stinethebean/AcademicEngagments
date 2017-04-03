# Frequently Asked Questions #


## Setup/Non Technical ##
### How Do I Check My Credits? ###
**NOTE:** Azure doesn't bill on weekends, if you run VMs, etc over the weekend credits won't show up as being used until about 1am on Monday.

1. Navigate to [https://www.microsoftazuresponsorships.com/](https://www.microsoftazuresponsorships.com/ "https://www.microsoftazuresponsorships.com/") and click on Manage Academic Accounts. You must be logged in with the same email address your professor used to allocate credits
	![](http://i.imgur.com/TiMQcMD.jpg)

2. Here you'll be able to see your credits
	![](http://i.imgur.com/QDmjvER.png)

### My Group-mate can't access Azure, can I add them? ###
If you are working in groups (and students are owners in Azure) – they can add their teammates who are having trouble accessing Azure 
1. Go to http://portal.azure.com 
2. Go to Subscriptions (first make sure you’re in the proper directory), where they’ll see one subscription. 
3. Click on it, then go to Access Control, and +ADD the email addresses of their teammates. (Which will send an invite email)
	![](http://i.imgur.com/0PtmZgB.jpg)

### Why Won't the Azure Portal Load? OR The Azure Portal Seems Broken ### 
Try using Chrome or Firefox incognito/in-private browsing. Safari doesn't consistently work with Azure. Sometimes caching issues require you use in-private/incognito mode.

### Is it just me, or is Azure down? ###
You can check the status of Azure at https://azure.microsoft.com/en-us/status/

### If my subscription gets canceled (because I ran out of credits) what happens to my resources?###
If you get the following error, it means that you've run out of the credits which your professor allocated to you. Possibly due to accidentally leaving a VM running when you weren't using it.
>Error: The subscription 'SUBSCRIPTION_ID_IS_HERE' is disabled and therefore marked as read only. You cannot perform any write actions on this subscription until it is re-enabled.

You'll want to reach out to your teaching staff to get your subscription re-activated, and more credits added. 
When that's complete, when you log into Azure, all your resources will still be there. 
**ALERT** - This is what usually causes the **Stopped(still incurring charges)** state (see below) - once it's re-activated, make sure you go back and turn off the VM/other resources. 


## Technical ##

### How do I have my VM turn off automatically when it's not being used ###
1. Azure doesn't have this feature yet, but we encourage you to use Azure auto-shutdown https://azure.microsoft.com/en-us/blog/announcing-auto-shutdown-for-vms-using-azure-resource-manager/ 

### Is my VM off? (And not charging me) ###
> Just an FYI – there are two possible stopped states in Azure

**Stopped (still incurring compute charges)** - $1.24/hr

If this is showing, hit STOP one more time to move to deallocated. (This basically frees up your VM hardware for someone to use while you’re not running anything – otherwise you’ve claimed “dibs”). This can happen if you do a "sudo shutdown now" in your VM.
 
![](http://i.imgur.com/1A3GUQ7.jpg)

**Stopped (deallocated)** – only paying for storage, more like $.04/hr
![](http://i.imgur.com/PbfhnNS.jpg)

### How Do I Add Another SSH Account? ###
Also known as "why do I keep getting logged out of my SSH session?" If you're sharing a VM with another user, when they log in, you get logged out. You can work around this by creating additional users for each person.

1. Linux Directions: https://help.ubuntu.com/lts/serverguide/user-management.html 
2. Windows: https://ittutorials.net/microsoft/windows-server-2016/create-a-new-local-user-account-in-windows-server-2016/  

### How do I open ports on my Linux VM? ###
Follow these directions: https://docs.microsoft.com/en-us/azure/virtual-machines/windows/nsg-quickstart-portal 

### The IP address of my VM keeps changing, can I set it to be static? ###
Yes! You can follow these directions: https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-deploy-static-pip-arm-portal 