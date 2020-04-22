---
author: Veracity adapter for Power BI
description: VAP tutorial - Share access to vap service account
---

# Share access to vap service account
[Previous - Upload file to Data Fabric](2-upload-file-to-data-fabric.md)

You now have a file in a container, and we now will grant VAP access to work on your storage on your behalf. This way, VAP can make sure a valid key is  available at all times, and that data provided to the end-user is always the latest.
 
To allow VAP access you need to share access from your container to the VAP Service account VAP@veracity.com. Go to data.veracity.com and share access according to the image belove.

<figure>
	<img src="assets/share-access-service-account-1.png"/>
	<figcaption>Step-by-step guide: Share access to service account</figcaption>
</figure>

When sharing the key, please select 'Set key as recurring', set access level to 'Read and list' and set duration to 1hour. Then click Share. 

<figure>
	<img src="assets/share-access-service-account-2.png"/>
	<figcaption>Step-by-step guide: Share access to service account</figcaption>
</figure>


VAP will now be able to refresh your data in a secure way. We now need to get the refrence URL to the file we want to work with in Power BI. Lets do that now.

[Next](4-veracity-file-url.md)

