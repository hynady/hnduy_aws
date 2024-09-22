---
title : "Configure Bucket for Static Website"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 2.3 </b> "
---

- Enable static website hosting:
  - In the bucket, go to "Properties".
  - Scroll down to "Static website hosting" and click "Edit".
![Enable static website hosting](/image/done7.png)
![Static website hosting](/image/done8.png)

- Select "Enable" and enter the index document name (e.g., index.html).
![Click "Enable"](/image/done9.png)
- Click "Save".
![Save](/image/done10.png)

- Configure Public Access Permissions:
  - In the "Permissions" section, you will see a part named "Block public access (bucket settings)".
  - Click "Edit" and ensure that the options to block public access (Block all public access) are turned off (meaning your bucket will allow public access).
![Configure Public Access Permissions](/image/done11.png)

- After turning off the block public access feature, click "Save changes".
![Click "Save changes"](/image/done12.png)

- Still in the "Permissions" tab, scroll down to the Bucket Policy section.
- If there is no policy, you need to add a policy to allow public access to the files in the bucket.
- Click "Edit" in the Bucket Policy section and add the following code. Make sure to replace "my-static-website-lab" with your actual bucket name.
![Edit](/image/done13.png)
![Add the code Click "Save changes"](/image/done14.png)