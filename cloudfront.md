# Setting up a cloudfront distribution

1. Sign in to the AWS Management Console and [open the CloudFront console](https://console.aws.amazon.com/cloudfront/).
2. Open the **CloudFront** service.
3. Choose **Create a CloudFront distribution** button.
4. In the **Origin domain** field, enter/select the domain name of your S3 bucket from the dropdown menu.
5. For **Origin Access**, select **Origin access control settings (recommended)**.
6. For **Origin access control**, select an existing OAC, or choose the **Create Control** setting.
7. In the dialogue box, name your control setting. It's a best practice to keep the default setting as **Sign requests (recommended)**. Then, choose **Create**.
8.  For **Settings**, in **Default root object**, enter the index file. "index.html"
9. Choose to enable or not enable **Web Application Firewall (WAF)**
10. Choose **Create Distribution**
11. For **S3 bucket Access**, apply the bucket policy on the S3 bucket. Select **Copy policy**, and go to your S3 bucket permission.
12. In the [Amazon S3 console](https://s3.console.aws.amazon.com/s3/buckets?region=us-east-1), from your list of buckets, choose the bucket that's the origin of the CloudFront distribution.
13. Choose the **Permissions** tab.
14. Under Bucket Policy, click edit, and paste the copied policy from the CloudFront distribution setup. confirm that you see a statement similar to the following:
``` json
    {
        "Version": "2008-10-17",
        "Id": "PolicyForCloudFrontPrivateContent",
        "Statement": [
            {
                "Sid": "AllowCloudFrontServicePrincipal",
                "Effect": "Allow",
                "Principal": {
                    "Service": "cloudfront.amazonaws.com"
                },
                "Action": "s3:GetObject",
                "Resource": "arn:aws:s3:::bucket-name/*",
                "Condition": {
                    "StringEquals": {
                      "AWS:SourceArn": "arn:aws:cloudfront::111122223333:distribution/ED7JWL22RRKBI"
                    }
                }
            }
        ]
    }
```
15. You must add the preceding statement to allow **CloudFront OAC** to read objects from your bucket.
16. The distribution creation process may take a few minutes. Once the status changes from **In-progress** to **Deployed**, the CloudFront distribution is ready.
17. To test your CloudFront distribution, open a web browser and access your content using the CloudFront domain name. For example: `https://your-cloudfront-domain.cloudfront.net`.