# Setting up AWS S3 bucket

In this section, you create a pipeline with the following actions:

A source stage with a CodeCommit action where the source artifacts are the files for your website.
A deployment stage with an Amazon S3 deployment action.

1. Sign in to the AWS Management Console and [open the CodePipeline console](http://console.aws.amazon.com/codesuite/codepipeline/home).
2. On the **Welcome** page, **Getting started** page, or **Pipelines** page, choose **Create pipeline**.
3. In **Step 1: Choose pipeline settings**, in **Pipeline name**, enter a name of your choice.
4. In the **Service role** section, choose an existing service role or choose **New service role** to allow CodePipeline to create a service role in IAM.
5. Leave the settings under **Advanced settings** at their defaults, and then choose **Next**.
6. In **Step 2: Add source stage**, in **Source provider**, choose **AWS CodeCommit** or **GitHub (V2)**. In Repository name, choose the name of the CodeCommit repository you created earlier. In **Branch name**, choose the name of the branch that contains your latest code update.
After you select the repository name and branch, the Amazon CloudWatch Events rule to be created for this pipeline is displayed.
Choose **Next**. If Github, click on the **Connect to GitHub** button and authorize AWS CodePipeline to access your GitHub repositories.
7. In **Step 3: Add build stage**, choose **Skip build stage**, and then accept the warning message by choosing **Skip** again.
Choose **Next**
8. In Step 4: Add deploy stage: <ol>
    <li>In Deploy provider, choose Amazon S3.</li>
    <li>In Bucket, enter the name of your public bucket.</li>
    <li>Select Extract file before deploy. Choose Next.</li>
    </ol>
9. In **Step 5: Review**, review the information, and then choose **Create pipeline**.
10. After your pipeline runs successfully, open the Amazon S3 console and verify that your files appear in your bucket
11. Once the pipeline is created, CodePipeline will automatically detect changes in your GitHub repository and trigger pipeline executions.
