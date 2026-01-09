 LEVEL 1: Launch Your First EC2 Instance
Objective: Create and run your first virtual computer in AWS.

🛠️ Steps

AWS Console → Search "EC2" → Click Launch Instance
Configure:

   Name: ZeroToHero-EC2
   AMI: Amazon Linux 2023 (Free tier)
   Instance Type: t2.micro

Create Key Pair:

Name: zth-keypair
Type: RSA
Format: .pem (Mac/Linux) or .ppk (Windows)
Download and save it to this folder!


Network Settings:

Create security group: zth-security-group
Allow: SSH (port 22) from "My IP"


Launch Instance


📸 Required Screenshots
Save these screenshots in this folder:

01-instance-running.png

Instance State: Running
Instance ID visible


02-instance-details.png

Instance ID
Public IPv4 address
Instance type (t2.micro)


03-launch-log.png (optional)

Initial launch confirmation



Also create instance-info.txt:
Instance ID: i-xxxxxxxxxxxxx
Public IPv4: xx.xx.xx.xx
Availability Zone: us-east-1x
Key Pair Name: zth-keypair

📤 Submission
bashgit add level-1-launch-ec2/
git commit -m "Complete Level 1: Launch EC2 Instance"
git push origin main

✅ Validation

 Instance state: Running
 Status checks: 2/2 passed
 Screenshots saved
 instance-info.txt created
 Files committed

🏆 Badge Earned: 🟡 Instance Launcher
Next: Level 2 →
