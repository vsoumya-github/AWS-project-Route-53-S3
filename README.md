# Deploy a Static Website on AWS using Route 53 and S3

                    
Project Overview:

In this project, I have launched a static website using two AWS services: Amazon S3 and Amazon Route 53. 
The landing page serves as an introduction, welcoming visitors to my website, which is now hosted on Amazon S3.

Steps for project:

STEP 1:

I started by creating a custom domain name using Route 53. To accomplish this, I navigated to the Amazon Route 53 dashboard and purchased a domain name. After confirming its availability, I added it to my cart and provided my contact details. Finally, I accepted the terms and conditions.
 
   ![image](https://github.com/vsoumya-github/AWS-projects/assets/137465090/c5f4277f-1c58-4fe4-a7fa-58a3b0de9503)


STEP 2:

Next, I created an Amazon S3 bucket to host the sample website. I went to the Amazon S3 page and clicked on "Create Bucket." I named the bucket after my chosen domain name and selected the region closest to me. To ensure public accessibility, I unchecked the "Block Public Access" option and proceeded while keeping the other settings as default.

  ![image](https://github.com/vsoumya-github/AWS-projects/assets/137465090/0808f638-f968-4f56-9e88-5700bc4884f9) 

  ![image](https://github.com/vsoumya-github/AWS-projects/assets/137465090/13ea18f6-6d0b-40e2-9061-9fdd21231b87)



STEP 3:

After creating the bucket, I uploaded the contents of my website, including the static website.html file. Once the upload was complete, I enabled static website hosting for the bucket. By accessing the "Properties" section, I scrolled down to the "Static Website Hosting" area, enabled it, and set the index document to "static website.html."

 ![image](https://github.com/vsoumya-github/AWS-projects/assets/137465090/28f143f5-084b-493c-ac41-126f797cd7bc)


STEP 4:

To grant public access to the website, I attached a bucket policy in the "Permissions" section. After clicking on "Edit," I added the necessary bucket policy, allowing viewers to access the sample website.

 ![image](https://github.com/vsoumya-github/AWS-projects/assets/137465090/7ed59f9b-b44c-4dac-9056-0bc255f111b8)


STEP 5:

At this point, I had successfully hosted the website on Amazon S3. However, the URL provided by Amazon was not my custom domain URL. To redirect my custom domain to the S3 bucket, I returned to Route 53. I accessed the hosted zone and my domain name, and I added an additional record to connect the bucket to the Route 53 domain name.

STEP 6:

To create the record, I clicked on "Create Record" and selected the simple routing policy. Then, I defined a simple record by setting the record type as "Alias to S3 website endpoint," choosing the appropriate region for my bucket, and selecting the S3 endpoint. After defining the record, I created it.

 ![image](https://github.com/vsoumya-github/AWS-projects/assets/137465090/fd119627-9375-4c2a-b486-7a1939c85cbb)


STEP 7:

It took a few minutes for the changes to propagate. Once the changes were implemented, my custom domain, such as "soumyaproject.click," pointed to the S3 bucket, and the website displayed the welcome message.

   ![image](https://github.com/vsoumya-github/AWS-projects/assets/137465090/f7e8c7e8-6064-414e-a21e-027f71c530b4)


In conclusion, I have completed the project by hosting a static website on Amazon S3 and connecting it to a custom domain using Amazon Route 53.


