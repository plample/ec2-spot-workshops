---
title: "Attach the IAM role to your Workspace"
chapter: false
weight: 40
---

## Create an IAM role for your Workspace

1. Follow [this deep link to create an IAM role with Administrator access.](https://console.aws.amazon.com/iam/home#/roles$new?step=review&commonUseCase=EC2%2BEC2&selectedUseCase=EC2&policies=arn:aws:iam::aws:policy%2FAdministratorAccess)
1. Confirm that **AWS service** and **EC2** are selected, then click **Next** to view permissions.
1. Confirm that **AdministratorAccess** is checked, then click **Next: Tags** to assign tags.
1. Take the defaults, and click **Next: Review** to review.
1. Enter **nextflow-workshop-admin** for the Name, and click **Create role**.
![createrole](/images/nextflow-on-aws-batch/prerequisites/createrole.png)

## Attach the IAM role to your Workspace

1. Follow [this deep link to find your Cloud9 EC2 instance](https://console.aws.amazon.com/ec2/v2/home?#Instances:tag:Name=aws-cloud9-.*workshop.*;sort=desc:launchTime)
1. Select the instance, then choose **Actions / Instance Settings / Attach/Replace IAM Role**
![c9instancerole](/images/nextflow-on-aws-batch/prerequisites/c9instancerole.png)
1. Choose **eksworkshop-admin** from the **IAM Role** drop down, and select **Apply**
![c9attachrole](/images/nextflow-on-aws-batch/prerequisites/c9attachrole.png)