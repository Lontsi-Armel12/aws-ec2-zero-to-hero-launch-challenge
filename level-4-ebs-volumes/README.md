LEVEL 4: EBS Volume Challenge
Objective: Attach external storage to your EC2 instance.
Concept: EBS volumes = Detachable hard drives for the cloud.

📦 Create & Attach Volume

EC2 Console → Volumes → Create Volume

   Size: 2 GB
   Volume Type: gp3
   Availability Zone: (same as your EC2)

Actions → Attach Volume

Select your ZeroToHero-EC2 instance
Device: /dev/sdf (will appear as /dev/xvdf)




💾 Format and Mount
SSH into your instance:
bash# Format the volume
sudo mkfs -t xfs /dev/xvdf

# Create mount point
sudo mkdir /mydata

# Mount the volume
sudo mount /dev/xvdf /mydata

# Verify
df -h

🧪 Test Storage
bash# Create test file
sudo touch /mydata/test.txt
echo "EBS Volume Working!" | sudo tee /mydata/test.txt

# Verify
cat /mydata/test.txt
ls -la /mydata

📸 Required Screenshots
Save in this folder:

01-volume-created.png

EBS volume in AWS Console (Available state)


02-volume-attached.png

Volume attached to instance (In-use state)


03-format-mount.png

Terminal showing mkfs and mount commands


04-df-output.png

Output of df -h showing /mydata mounted



Also create storage-notes.txt:
Volume ID: vol-xxxxxxxxxxxxx
Size: 2 GB
Mount Point: /mydata
File System: xfs
Test File Created: Yes/No

📤 Submission
bashgit add level-4-ebs-volumes/
git commit -m "Complete Level 4: EBS Volumes"
git push origin main

✅ Completion

 Volume created and attached
 Volume formatted (xfs)
 Mounted to /mydata
 Test file created
 4 screenshots saved
 Notes file created
 Files committed

🏆 Badge Earned: 🟫 Storage Handler
Next: Level 5 →
