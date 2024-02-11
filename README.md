# Running Terraform to provision MultiCloud infrastructure in AWS and Google Cloud

Step One - Execute the following commands to provision infrastructure resources
    
    - cd ~/mission1/en/terraform/
    - terraform init
    - terraform plan
    - terraform apply

Attention: The provisioning process can take between 15 to 25 minutes to finish. Keep the CloudShell open during the process. If disconnected, click on Reconnect when the session expires (the session expires after 5 minutes of inactivity by default).

# Appendix I - Destroying the environment and starting over

In case you have encountered any problem/error and want to reset the environment to start over, follow the step-by-step instructions below to remove the entire MultiCloud environment.
   
    - [Google Cloud] Delete VPC Peering
    - [Google Cloud] Delete remaining resources w/ Terraform - Cloud Shell
        - cd ~/mission1/en/terraform/
        - terraform destroy
    - Clean the Cloud Shell in AWS and Google Cloud
        - AWS
          - cd ~
          - rm -rf mission*
        - Google Cloud
          - cd ~
          - rm -rf mission*
          - rm -rf .ssh

## Security Tips

- For production environments, it's recommended to use only the Private Network for database access.
- Never provide public network access (0.0.0.0/0) to production databases. ⚠️
