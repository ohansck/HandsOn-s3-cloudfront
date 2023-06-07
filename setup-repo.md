# Setting up GitHub and AWS CodeCommit repositories

## Setting up GitHub repo

To get started with this project, follow these steps:

1. Clone the repository to your local machine using the following command:
   ``` bash
   git clone https://github.com/ohansck/handson-s3-cloudfront.git
   ```
2. Change into the project directory:
   ``` bash
   cd handson-s3-cloudfront
   ```
3. Initialize a git repo
   ``` bash
   git init
   ```
4. Create a new repo on github, copy the HTTPS clone link

5. Connect git to a remote repo:
   ``` bash
   git remote add origin https://github.com/your-name/repo-name.git
   ```
6. Commit and switch to a main branch, make modifications if needed then push to origin:
   ``` bash
   git commit -m "your-message"
   git checkout -B main
   git push -u origin main
   ```
## Setting up AWS CodeCommit

1. Log in to the AWS Management Console.
2. Open the AWS CodeCommit service.
3. Click on the "Create repository" button.
4. Enter a name for your repository. Choose a descriptive and meaningful name.
5. (Optional) Provide a description for your repository to provide additional context.
6. (Optional) Add tags to your repository for better organization and resource management.
7. Click on the "Create repository" button to create your AWS CodeCommit repository.
8. Once the repository is created, you can access it from the repository page. Here, you can find the repository URL, clone command, and other relevant information.
9. On the HTTPS tab, copy the repo URL and repeat step 5 and 6 from Setting up GitHub repo above

## (Optional) Setting user credentials for AWS CodeCommit

1. If you are prompted for a username and password, execute steps 3 and 4 of the [Generate Git Credentials](https://docs.aws.amazon.com/console/codecommit/connect-gc-np) article.