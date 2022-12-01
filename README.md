# webapp3
You can configure an Amazon S3 bucket to function like a website. 

## Create bucket:
1. Sign in to the AWS Management Console and open the Amazon S3 console at https://console.aws.amazon.com/s3/.
2. Choose Create bucket.
3. Enter the Bucket name (for example, example.com).
4. Choose the Region where you want to create the bucket (eu-west-1).
5. To accept the default settings and create the bucket, choose Create.

## Enable static website hosting:
In to the AWS Management Console and open the Amazon S3 console
1. In the Buckets list, choose the name of the bucket that you want to enable static website hosting for.
2. Choose Properties.
3. Under Static website hosting, choose Edit.
4. Choose Use this bucket to host a website.
5. Under Static website hosting, choose Enable.
6. In Index document, enter the file name of the index document, typically index.html.
7. Choose save changes.
8. uder static website hosting, note the endpoint
The Endpoint is the Amazon S3 website endpoint for your bucket. After you finish configuring your bucket as a static website, you can use this endpoint to test your website.

## Edit Block Public Access settings
By default, Amazon S3 blocks public access to your account and buckets. If you want to use a bucket to host a static website, you can use these steps to edit your block public access settings.

1. Choose the name of the bucket that you have configured as a static website.
2. Choose Permissions.
3. Under Block public access (bucket settings), choose Edit.
4. Clear Block all public access, and choose Save changes.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AmazonS3/latest/userguide/images/edit-public-access-clear.png)

 ## Add a bucket policy that makes your bucket content publicly available
After you edit S3 Block Public Access settings, you can add a bucket policy to grant public read access to your bucket. When you grant public read access, anyone on the internet can access your bucket.

1. Under Buckets, choose the name of your bucket.
2. Choose Permissions.
3. Under Bucket Policy, choose Edit.
4. To grant public read access for your website, copy the following bucket policy, and paste it in the Bucket policy editor.
5. Choose Save changes.

## Configure an index document
1. Download webapp3 project from github.
2. Copy the content of webapp3 in your s3 bucket

## Test your website endpoint
After you configure static website hosting for your bucket, you can test your website endpoint.

1. Under Buckets, choose the name of your bucket.
2. Choose Properties.
3. At the bottom of the page, under Static website hosting, choose your Bucket website endpoint.
Your index document opens in a separate browser window.
