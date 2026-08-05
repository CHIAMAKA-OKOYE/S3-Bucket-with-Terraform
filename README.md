# ☁️ Terraform & AWS S3 Bucket

> **Infrastructure as Code** — create an S3 bucket and upload objects to it using Terraform.

<div align="center">

![Made with Terraform](https://img.shields.io/badge/IaC-Terraform-844FBA?style=for-the-badge&logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-S3-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-28A745?style=for-the-badge)

</div>

---

## 📋 Table of Contents

1. [Prerequisites](#-prerequisites)
2. [Step 1 — Install Terraform](#-step-1--install-terraform)
3. [Step 2 — Configure AWS CLI](#-step-2--configure-aws-cli)
4. [Step 3 — Write the Terraform Configuration](#-step-3--write-the-terraform-configuration)
5. [Step 4 — Initialize the Working Directory](#-step-4--initialize-the-working-directory)
6. [Step 5 — Generate the Execution Plan](#-step-5--generate-the-execution-plan)
7. [Step 6 — Create the S3 Bucket](#-step-6--create-the-s3-bucket)
8. [Step 7 — Upload an Object to the S3 Bucket](#-step-7--upload-an-object-to-the-s3-bucket)
9. [Step 8 — Apply the Object Upload](#-step-8--apply-the-object-upload)
10. [Step 9 — Verify the Uploaded Object](#-step-9--verify-the-uploaded-object)
11. [🧾 Commands Summary](#-commands-summary)

---

## 🔧 Prerequisites

- ✅ [Terraform CLI](https://www.terraform.io/downloads) installed
- ✅ [AWS CLI](https://aws.amazon.com/cli/) installed & configured
- ✅ An AWS account with S3 permissions

---

## 🛠️ Step 1 — Install Terraform

![Terraform installation](Pictures/Terraform%20installation.png)

Install Terraform and verify it's ready to use on your machine.

## 🔑 Step 2 — Configure AWS CLI

![Configured AWS CLI](Pictures/Configured%20AWS%20CLI.png)

Set up your AWS credentials so Terraform can authenticate with your AWS account.

## 📝 Step 3 — Write the Terraform Configuration

`main.tf` is the heart of the project — it defines all the infrastructure.

![Main.tf-content](Pictures/Main.tf-content%20.png)

The base configuration that declares the AWS provider, the S3 bucket, and the object to upload.

![Customized main.tf](Pictures/Customized%20main.tf.png)

Customized with your own bucket name and settings.

## 🚀 Step 4 — Initialize the Working Directory

![Terraform init](Pictures/Terraform%20init.png)

```bash
terraform init
```

Downloads the required provider plugins and initializes the project.

## 📊 Step 5 — Generate the Execution Plan

![Terraform plan](Pictures/Terraform%20plan.png)

```bash
terraform plan
```

Preview what Terraform will create — no changes are made yet.

## 🪣 Step 6 — Create the S3 Bucket

![Terraform apply](Pictures/Terraform%20apply.png)

```bash
terraform apply
```

Apply the configuration to create the bucket.

![S3 bucket created](Pictures/S3%20bucket%20created.png)

The bucket is now created!

![S3 bucket confirmation](Pictures/S3%20bucket%20confirmation.png)

Confirm it in the AWS S3 console.

---

## 📤 Step 7 — Upload an Object to the S3 Bucket

A second `main.tf` configuration defines an `aws_s3_object` resource to add an item to the bucket.

![Main.tf file for uploading an S3 object](Pictures/Main.tf%20file%20for%20uploading%20an%20S3%20object.png)

## ✅ Step 8 — Apply the Object Upload

![Terraform apply for adding the S3 object](Pictures/Terraform%20apply%20for%20adding%20the%20S3%20object.png)

Run `terraform apply` again to upload the object into the bucket.

## 🎉 Step 9 — Verify the Uploaded Object

![S3 objected uploaded](Pictures/S3%20objected%20uploaded.png)

Your file is now live as an object inside the S3 bucket!

---

## 📝 About `main.tf`

`main.tf` is where all the infrastructure is defined. It configures the AWS provider, sets up an S3 bucket, and defines the object that gets uploaded into it. You customize the bucket name and the file to upload in this file before running `terraform apply`.

---

## 🧾 Commands Summary

| Step | Command | Description |
| ---- | ------- | ----------- |
| 1 | `terraform init` | Initialize working directory |
| 2 | `terraform plan` | Preview changes |
| 3 | `terraform apply` | Create bucket / upload object |
| 4 | `terraform destroy` | Tear everything down (optional) |

> ⚠️ **Always review the plan before applying, and keep your state file safe.**

---

<p align="center">
  <strong>Made by Racheal</strong>
</p>
