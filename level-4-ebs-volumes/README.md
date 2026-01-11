## LEVEL 4: EBS Volume Challenge

**Objective:** Attach external storage to your EC2 instance.  
**Concept:** EBS volumes = Detachable hard drives for the cloud.

### 💻 Requirements Before You Start

- Open the project folder with your preferred code editor or IDE (e.g., VS Code).
- Open the integrated terminal within your editor/IDE to run the commands below.
- Move to the current task directory:
  ```bash
  cd level-4-ebs-volumes
  ```
---

1. **Open the AWS EC2 Console**  
   Log in to your AWS account and go to the **EC2 Dashboard**.

2. **Go to the Volumes Section**  
   In the left-hand menu, find and click on **Volumes** under the **Elastic Block Store** section.
   <img width="1860" height="914" alt="image(4)" src="https://github.com/user-attachments/assets/ed681ea1-130e-410f-a43c-bae9d1ee7202" />

4. **Create a New Volume**  
   Click the **Create Volume** button.  
   <img width="568" height="101" alt="image" src="https://github.com/user-attachments/assets/3e634a57-1e02-4816-a53c-06612c20bcfb" />  


6. **Set Up Your Volume**  
   - **Size:** Enter **2 GB**  
   - **Volume Type:** Choose **gp3** (a fast and cost-effective option)  
   - **Availability Zone:** Make sure to select the **same Availability Zone** where your EC2 instance is running. This is important because volumes can only be attached to instances in the same zone.

7. **Create the Volume**  
   Click **Create Volume** to finish.  
   if successful:  
   <img width="1617" height="237" alt="image(4)" src="https://github.com/user-attachments/assets/7b640580-9a17-4426-b5c4-4e465baa73ae" />

9. **Attach the Volume to Your Instance**  
   - Find the volume you just created in the list.  
   - Select it, then click **Actions → Attach Volume**.  
   - In the popup, select your EC2 instance named **ZeroToHero-EC2-{Your Name}** from the dropdown list.  
   - For the **Device** field, enter `/dev/sdf`. (On your EC2 instance, this will show up as `/dev/xvdf`.)  
   - Click **Attach** to connect the volume to your instance.  
     <video width="1617" height="237" alt="image(4)" src="https://github.com/user-attachments/assets/c9700dfe-8c8e-4f41-bbf5-a2490424f4b5" />

   If successful:  
   <img width="1619" height="258" alt="image(4)" src="https://github.com/user-attachments/assets/4cf226f2-c877-4d3a-ae20-461c65139582" />



**Tip:** If you don’t see your instance in the list, double-check that the volume and your instance are in the same Availability Zone.
This process adds extra storage to your EC2 server, like plugging in an external hard drive — but in the cloud!

---

### 💾 Format and Mount

[SSH into your EC2 instance](../level-2-connect-ssh/README.md#run) and run:

```bash
# Format the volume with the XFS filesystem
sudo mkfs -t xfs /dev/xvdf

# Create a mount point directory
sudo mkdir /mydata

# Mount the volume to the directory
sudo mount /dev/xvdf /mydata

# Verify the mount
df -h
```

---

### 🧪 Test Storage

Run these commands to test your new storage:

```bash
# Create a test file on the mounted volume
sudo touch /mydata/test.txt
echo "EBS Volume Working!" | sudo tee /mydata/test.txt

# Verify the file contents and listing
cat /mydata/test.txt
ls -la /mydata
```

---

### 📸 Required Screenshots

Save these screenshots in your project folder:

- **01-volume-created.png**  
  EBS volume visible in AWS Console (status: Available)

- **02-volume-attached.png**  
  Volume attached to your instance (status: In-use)

- **03-format-mount.png**  
  Terminal showing `mkfs` and `mount` commands running

- **04-df-output.png**  
  Output of `df -h` showing `/mydata` mounted

---

### 📝 Also create `storage-notes.txt` and fill:

```
Volume ID: vol-xxxxxxxxxxxxx
Size: 2 GB
Mount Point: /mydata
File System: xfs
Test File Created: Yes/No
```

---

### 📤 Submission

```bash
git add level-4-ebs-volumes/
git commit -m "Complete Level 4: EBS Volumes"
git push origin main
```

---

### ✅ Completion Checklist

- [ ] Volume created and attached
- [ ] Volume formatted with xfs
- [ ] Mounted to `/mydata`
- [ ] Test file created on volume
- [ ] 4 screenshots saved
- [ ] Notes file created
- [ ] Files committed

---

Fill out this form to collect your badge:https://forms.gle/aW6oFwNEZE3tZJ9V9

**Next:** → [Level 5](../level-5-security-groups/README.md) 
