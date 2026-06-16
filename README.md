Step 1: Clone the Repository
Pull this project down to your local Linux environment:


git clone [https://github.com/Tushar-Shillarkar/terraform-s3-static-website.git](https://github.com/Tushar-Shillarkar/terraform-s3-static-website.git)
cd terraform-s3-static-website

Step 2: Initialize Terraform
This command prepares your working directory by downloading the necessary AWS and Random provider plugins required to execute the code.

terraform init

Step 3: Validate and Plan
Before building anything, run a plan. This allows you to safely preview the exact changes Terraform will make to your AWS account without actually provisioning any resources yet. Add access_key and secret_key in provider.tf

terraform plan

Step 4: Execute the Deployment
Apply the configuration. Terraform will build the S3 bucket, attach the security policies, and upload the web assets.

terraform apply -auto-approve

Step 5: View the Live Website
Once the deployment finishes successfully, Terraform will output a green variable in your terminal called website_endpoint.

Click or copy that URL into your web browser to view the live website hosted directly from your new AWS S3 bucket!

🧹 Infrastructure Teardown (Cleanup)
To prevent any unexpected charges on your AWS account, it is best practice to destroy the infrastructure when you are done testing. You can cleanly wipe out the S3 bucket and all associated policies with a single command:


terraform destroy -auto-approve
