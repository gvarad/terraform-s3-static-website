Step 2: Clone the Repository
Pull this project down to your local Linux environment:


git clone [https://github.com/YOUR_USERNAME/terraform-s3-static-website.git](https://github.com/YOUR_USERNAME/terraform-s3-static-website.git)
cd terraform-s3-static-website
Step 3: Initialize Terraform
This command prepares your working directory by downloading the necessary AWS and Random provider plugins required to execute the code.


terraform init
Step 4: Validate and Plan
Before building anything, run a plan. This allows you to safely preview the exact changes Terraform will make to your AWS account without actually provisioning any resources yet.


terraform plan
Step 5: Execute the Deployment
Apply the configuration. Terraform will build the S3 bucket, attach the security policies, and upload the web assets.

terraform apply -auto-approve
Step 6: View the Live Website
Once the deployment finishes successfully, Terraform will output a green variable in your terminal called website_endpoint.

Click or copy that URL into your web browser to view the live website hosted directly from your new AWS S3 bucket!

🧹 Infrastructure Teardown (Cleanup)
To prevent any unexpected charges on your AWS account, it is best practice to destroy the infrastructure when you are done testing. You can cleanly wipe out the S3 bucket and all associated policies with a single command:


terraform destroy -auto-approve
