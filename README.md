# This Repo consists of steps to for vpc peering and seeing results via full stack application deployed in aws <br>
Here Rds is in private subnet in another vpc,ec2 is in another vpc with vpc peering it allows communication between these two resources <br>
![Screenshot (519)](https://github.com/user-attachments/assets/f4a22758-6f83-4133-b34a-98e54b014b11)
# Go to vpc,click peering connections 
Click Peering Connection <br>
Give the source vpc and receiver vpc,select region,account and click create
![Screenshot (520)](https://github.com/user-attachments/assets/81a2e076-bd15-4fbd-8fa2-e1b144f7d89c)
# Attach that peering connection in the both route tables ( Give the destinatioon vpc address or destination resource private ip and viceversa in order to allow communication )
![Screenshot (521)](https://github.com/user-attachments/assets/3f6f4c3a-d7d7-48c4-b8bf-23c12f24aa6e)
# Same did like above
![Screenshot (522)](https://github.com/user-attachments/assets/621ea2f9-be7a-43a5-9dce-1a105f405f0b)
# Here rds is private ( It is in private subnet and no ip address is attached )
![Screenshot (523)](https://github.com/user-attachments/assets/0c0a949c-a03f-4430-ba6a-d4469bca4da9)
# Specify the port number for listening the requests sent from source
![Screenshot (524)](https://github.com/user-attachments/assets/1b082275-f606-4df9-aa2d-94dbb3b3d255)
# Uploading ( Created ec2 
![Screenshot (525)](https://github.com/user-attachments/assets/0c97daa1-d83e-4a4f-b526-7831f75e54e2)
# Uploaded
![Screenshot (526)](https://github.com/user-attachments/assets/afe62740-8f95-4034-8189-774542e028f0)
# Uploaded file accessing through the link
![Screenshot (527)](https://github.com/user-attachments/assets/ee0e181e-5f55-4574-b65e-818828019d58)
# Fetching from rds like how many files uploaded in each time


-> Create an EC2 Instance:
Go to the EC2 service in the AWS Console. Click "Launch Instance", choose an Amazon Linux or Ubuntu AMI, select a t2.micro instance (free tier), and create a new key pair (or use an existing one). Configure the security group to allow ports like 22 (SSH), 5000 (Node.js), and 80 (HTTP). Launch the instance and note its public IP address.
<br>
Create an S3 Bucket:
Go to the S3 service and click "Create bucket". Enter a globally unique bucket name (e.g., my-app-uploads), choose the region closest to you (e.g., Asia Pacific - Mumbai), and leave default settings unless you need public access. Click "Create bucket".
<br>
Create an RDS Instance:
Go to the RDS service and choose "Create database". Select the MySQL engine, then pick a t2.micro instance (free tier eligible). Set a DB name, master username (e.g., admin), and password. Under connectivity, make sure to allow public access if you want to connect from outside EC2, and set the security group to allow port 3306 (MySQL).
