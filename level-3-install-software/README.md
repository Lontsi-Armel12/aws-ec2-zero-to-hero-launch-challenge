## LEVEL 3: Install Software on Your EC2

**Objective:** Deploy a web server to the internet.

---

### 🌐 Install Apache

**While connected via SSH**, run:

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

---

### 📄 Create Webpage

```bash
echo "Welcome to my Zero-to-Hero EC2 Challenge!" | sudo tee /var/www/html/index.html
```

---

### 🧪 Test in Browser

Visit: `http://<Public-IP-or-DNS>`

---

### ⚠️ Page Not Loading?

**CRITICAL LESSON!**  
Your server is running, but AWS is protecting it by default. When you launch your EC2 server, AWS protects it by default, so web traffic (like visitors using a browser) can’t reach your server until you allow it. 


1. **Open the AWS EC2 Console**  
   Go to the [AWS EC2 Console](https://console.aws.amazon.com/ec2) and find the **Security Groups** section.

2. **Find Your Security Group**  
   Look for the security group named **zth-security-group** (this controls the network rules for your server).

3. **Edit Inbound Rules**  
   Click on **Inbound Rules**, then click the **Edit** button to change the rules.

4. **Add a New Rule to Allow HTTP Traffic**  
   - For **Type**, select **HTTP** (this automatically sets the port to 80).  
   - For **Source**, choose **Anywhere (0.0.0.0/0)** — this means anyone on the internet can access your web server.

5. **Save Your Changes**  
   Click **Save** to apply the new rule.

6. **Test Your Website**  
   Go back to your browser and refresh the page at your EC2 instance’s public IP or DNS address. You should now see your web page!

💡 **Key Lesson:**  
*"Cloud isn't insecure. It's secure by default."*

---

### 📸 Required Screenshots

Save in this folder:

- **01-apache-install.png**  
  Terminal showing Apache installation

- **02-security-group-before.png**  
  Security group rules BEFORE adding HTTP

- **03-security-group-after.png**  
  Security group rules AFTER adding HTTP

- **04-webpage-working.png**  
  Browser showing your custom message

---

### 📝 Also create `web-server-notes.txt` and fill:

```
Apache Install Status: Success/Failed
Security Group Rule Added: Yes/No
Webpage URL: http://_______________
Key Lesson Learned: _______________
```

---

### 📤 Submission

```bash
git add level-3-install-software/
git commit -m "Complete Level 3: Deploy Web Server"
git push origin main
```

---

### ✅ Completion Checklist

- [ ] Apache installed
- [ ] Custom message displays in browser
- [ ] HTTP rule added to security group
- [ ] 4 screenshots saved
- [ ] Notes file created
- [ ] Files committed

---

fill out this form to get your badge:https://forms.gle/4MQWPnAY2z7PaPM4A

**Next:** → [Level 4](https://github.com/awssccuba/aws-ec2-zero-to-hero-launch-challenge/blob/main/level-4-ebs-volumes/README.md)
