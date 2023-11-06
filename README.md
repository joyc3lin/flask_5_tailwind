# flask_5_tailwind
This assignment will give you hands-on experience in video hosting, creating a Flask app styled with Tailwind CSS, and deploying it to a cloud platform. You'll leverage CDN services in Google Cloud or Azure to optimize video delivery, ensuring a seamless user experience for viewers worldwide.

# Video Creation or Procurement 

I chose to use a 12-second video I took in Japan of Koi fish swimming in a river. 

# Cloud CDN & Video Hosting

**To Create A New Storage Account**

+ The video is hosted on Azure's Content Delivery Network (CDN)
+ On Azure, go to "Storage Accounts" in the drop down menu on the left
+ Create a new storage account 
+ Select a subscription and resource group (may create a new one if needed) 
+ Create a storage account name and select a region based on current location 
+ Performance: Standard 
+ Reduncancy: Geo-redundant storage (GRS)
+ Review and Create 

**Video Hosting**

+ In created storage account, scroll down and go to "Security" 
+ In "Security", enable "Allow Blob anonymous access"
+ Save 

+ In the left menu bar of the storage account, go to "Data storage" and select "Containers"
+ Create a new container 
+ Name the container 
+ Anonymous access level: Container
+ Create

+ In newly created container, select upload
+ Drop or browse for the desired file 
+ Upload file 
+ Go into the newly uploaded file and copy the URL provided into a new tab

+ Go back to the storage account, under "Security + networking", go to "Front Door and CDN"
+ Create a new endpoint 
+ Service type: Azure CDN 
+ Create new profile with a profile name and endpoint name
+ Query string caching behavior: Ignore Query String 
+ Create 

+ In endpoints, click on the newly created host name and click on it again in the next page that loads 
+ It will then show a page with "Endpoint hostname" and "Origin hostname" 
+ Open the URL under "Endpoint hostname" 

+ From the URL pasted into the new tab from before, copy the part that comes after "-windows.net"
+ Paste it into the tab created after opening the "Endpoint hostname" URL
+ Press enter and refresh the page
+ Save the URL 

# Flask App with Tailwins CSS 

+ In Google shell, create a new <code>app.py</code> file and a templates folder with an <code>index.html</code> file 
+ In the <code>index.html</code> file, the code from the Professor's [example](https://github.com/hantswilliams/HHA_504_2023/blob/main/WK5/example_app/templates/index_tailwind.html) was pasted in and [edited](https://github.com/joyc3lin/flask_5_tailwind/blob/main/templates/index.html)
+ In the <code>app.py</code> file, 

# Cloud Deployment 

# Validate Asset Delivery 

# Errors

could not uolad .MOV file

quotation font error in index.html