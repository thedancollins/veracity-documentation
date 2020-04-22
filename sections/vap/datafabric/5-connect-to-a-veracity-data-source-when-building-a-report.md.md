---
author: Veracity adapter for Power BI
description: VAP tutorial - Connect to Veracity data source when building your Power BI report
---

# Connect to Veracity data source when building your Power BI report
[Previous - Veracity file url](4-veracity-file-url.md)

There are two ways to connect to Veracity Data Fabric from Power BI, either ‘Web’ or use ‘OData feed’. 

1. [Alternative 1: Get data from Web](#Alternative-1:-Get-data-from-Web)
2. [Alternative 2: OData Feed](#Alternative-2:-OData-Feed)

## Alternative 1: Get data from Web
Before we create the connection to the data, we need to create a parameter - this will for the data inside the file to change over time.

Click the <i>Edit Queries</i> dropdown in Power BI and hit <i>Edit Queries</i> in the dropdown.

<figure>
	<img src="assets/edit-queries.png"/>
	<figcaption>Step-by-step guide: Edit queries</figcaption>
</figure>

Next, select <i>New Parameter</i>. Define a Parameter and add the file URL from the previous section in the field named <i>Current Value</i>. You can give the parameter a name of your choice, preferably something that describes the content of the file as it will be the default name on your data table. Set other options as in below image.

<figure>
	<img src="assets/edit-queries-2.png"/>
	<figcaption>Step-by-step guide: Edit queries</figcaption>
</figure>

Save your parameter and click <i>Close & Apply</i>. We are now ready to connect to the data and start building the report. 

Select ‘Get data’, then ‘Web’ and <i>Parameter</i>: 

<figure>
	<img src="assets/from-web.png"/>
	<figcaption>Step-by-step guide: Get data from web</figcaption>
</figure>

From the dropdown menu you will find your newly created parameter. Select the parameter and click ‘OK’. 

<figure>
	<img src="assets/from-web-2.png"/>
	<figcaption>Step-by-step guide: Get data from web</figcaption>
</figure>

Finally make sure <i>Anonymous</i> is selected and then <i>Connect</i>. 

<figure>
	<img src="assets/from-web-3.png"/>
	<figcaption>Step-by-step guide: Get data from web</figcaption>
</figure>

You have successfully connected to the file in the Veracity Data Fabric when you see the values on-screen and hit <i>Load</i> to bring them into your workspace. 

<figure>
	<img src="assets/from-web-4.png"/>
	<figcaption>Step-by-step guide: Get data from web</figcaption>
</figure>

If you have multiple files in Veracity you want to connect to, repeat all steps for each file. 

You can now build your visuals as usual and save the file as .pbix. Next we will see how to upload the file to VAP when using a Veracity Data Fabric storage as a data source.



## Alternative 2: OData Feed
OData solves one problem for us, and that is that the content type can be changed over time. The exception fom this is when working with text or CSV files. Then the content type cannot change by default. 

### Solution to the change content type og text/csv when using OData
Open Microsoft Azure Storage Explorer to check your file. If the Content Type is not application/octet-stream, modify the file. Click the file you will be working on, then select Properties. 
<figure>
	<img src="assets/modify-content-type.png"/>
	<figcaption>Step-by-step guide: Modify Content-Type</figcaption>
</figure>
Change the <i>ContentType</i> property to application/octet-stream, and then click the Save button.
<figure>
	<img src="assets/modify-content-type-2.png"/>
	<figcaption>Step-by-step guide: Modify Content-Type</figcaption>
</figure>

## OData connection
To bring the data in to Power BI using OData, go to the Get Data panel, and select <i>OData feed</i>. In the case that OData Feed is not visible in the drop-down, you should find it under <i>More...</i>

<figure>
	<img src="assets/odata-feed.png"/>
	<figcaption>Step-by-step guide: Get data - OData feed</figcaption>
</figure>

Now, paste the url from Data Fabric into the URL field and click <i>OK</i>. The URL you obtained in the previous section, [Veracity file URL](4-veracity-file-url).

<figure>
	<img src="assets/odata-feed-2.png"/>
	<figcaption>Step-by-step guide: Get data - OData feed</figcaption>
</figure>

It’s successfully set up if you can see the data. Click <i>Load</i> to start working on the data.  

You can now build your visuals as usual and save the file as .pbix. Next we will see how to upload the file to VAP when using a Veracity Data Fabric storage as a data source.

[Next](5-manage-users.md)


