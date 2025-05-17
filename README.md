# CLOUD-STORAGE-CREATION-S3-AND-LAUNCHING-AN-EC2-INSTANCE-IN-AWS-
# Ex.2: Cloud Storage Creation (S3) and Launching an EC2 Instance in AWS

## Aim
To create a Simple Storage Service (S3) bucket in AWS and to launch an EC2 instance in AWS.

---

## Procedure

### A) Steps to Create a First S3 Bucket

1. **Sign in to the AWS Management Console**  
   - Go to: [https://console.aws.amazon.com/s3](https://console.aws.amazon.com/s3)

2. **Open the S3 Service**  
   - In the AWS console, type **"S3"** in the search bar and select **S3** to open the service dashboard.

3. **Create Bucket**  
   - Click the **"Create bucket"** button.

4. **Configure Bucket Settings**  
   - **Bucket name**: Enter a globally unique name.  
   - **AWS Region**: Select the region where you want to store your data.

5. **Object Ownership**  
   - Choose between:  
     - **ACLs disabled (recommended)** – Bucket owner has full control.  
     - **ACLs enabled** – Control access via Access Control Lists.

6. **Block Public Access Settings**  
   - By default, all public access is blocked. Leave it as-is unless public access is required.

7. **Bucket Versioning (Optional)**  
   - Choose whether to enable versioning for objects in the bucket.

8. **Encryption (Optional)**  
   - Select encryption type:  
     - **SSE-S3** (default AWS-managed keys)  
     - **SSE-KMS** (customer-managed keys)  
     - **None**

9. **Advanced Settings (Optional)**  
   - Add tags, enable logging, etc.

10. **Create the Bucket**  
    - Click **"Create bucket"** at the bottom of the page.

---

### B) Steps to Launch an EC2 Instance

1. Go to the **EC2 Dashboard** in AWS Console.

2. Click on **"Launch Instance"**.

3. **Choose an Amazon Machine Image (AMI)**  
   - Example: **Amazon Linux AMI**

4. **Select an Instance Type**  
   - Example: **t2.micro** (eligible for Free Tier)

5. **Create or Choose a Key Pair**  
   - Required for SSH access.

6. **Configure Network Settings**  
   - Use default **VPC** and **subnet** unless otherwise specified.

7. **Configure Storage**  
   - Default root volume is sufficient for basic needs.

8. **Review and Launch**  
   - Verify all configurations and click **"Launch Instance"**.

9. **Instance Initialization**  
   - Wait for the instance to reach the **"running"** state.

---

### C) Connect to Your EC2 Instance

- **Linux Users**: Use SSH with your `.pem` key:
  ```bash
  ssh -i "your-key.pem" ec2-user@your-ec2-public-dns
