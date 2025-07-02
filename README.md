# AWS-Full-Stack-Deployment-using-S3-EC2-RDS
This Repo consists of steps to deploy a full stack application using s3,ec2 and rds with vpc peering <br>
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
# Here rds is private
![Screenshot (523)](https://github.com/user-attachments/assets/0c0a949c-a03f-4430-ba6a-d4469bca4da9)
# Specify the port number for listening the requests sent from source
![Screenshot (524)](https://github.com/user-attachments/assets/1b082275-f606-4df9-aa2d-94dbb3b3d255)
# Uploading 
![Screenshot (525)](https://github.com/user-attachments/assets/0c97daa1-d83e-4a4f-b526-7831f75e54e2)
# Uploaded
![Screenshot (526)](https://github.com/user-attachments/assets/afe62740-8f95-4034-8189-774542e028f0)
# Uploaded file accessing through the link
![Screenshot (527)](https://github.com/user-attachments/assets/ee0e181e-5f55-4574-b65e-818828019d58)
# Fetching from rds like how many files uploaded in each time


->  In the s3 create build,push to s3 and call the backend via ec2 instance url <br>
