# Overview

A repo to explain the purpose of Terragrunt. The wordpress example is taken from: https://github.com/nholuongut/terraform-ec2-RDS-wordpress.

![](https://i.imgur.com/waxVImv.png)

# Roadmaps are now interactive, you can click the nodes to read more about the topics.

### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)

![](https://i.imgur.com/waxVImv.png)

## Instructions

### First Try Terraform Only

In the `Terraform_Only/environments/dev` folder create a private/public key pair with an empty passphrase:

```bash
ssh-keygen -f mykey-pair
sudo chmod 400 mykey-pair
```

In order to create a remote backend to store Terraform state files, you will need to create an S3 bucket and a Dynamo DB table. This is a good guide: https://www.golinuxcloud.com/configure-s3-bucket-as-terraform-backend/#:~:text=Configure%20S3%20bucket%20as%20Terraform%20backend%20%5BStep-by-Step%5D%201,Configure%20Terraform%20to%20point%20to%20this%20backend%20

Run Terraform commands

```bash
terraform init
terraform plan
terraform apply
```

### Finally Try Terragrunt

In the `Terragrunt/environments/dev` folder run the following command to create a private/public key pair with an empty passphrase:

```bash
ssh-keygen -f mykey-pair
sudo chmod 400 mykey-pair
```

Then run the following terragrunt commands:

```bash
terragrunt init
terragrunt plan
terragrunt apply
```

Terragrunt sets the AWS remote backend for you. It will create an S3 bucket and a Dynamo DB table.

## Clean Up

Terragrunt has a neat feature that allows you to run commands across multiple folders. In our case we will run the following command to destroy the dev and prod environments:

```bash
@nholuongut ➜ /workspaces/env0-terragrunt/Terragrunt/environments (main) $ terragrunt run-all destroy
```

I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](bitfield.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.
