LEVEL 2: Connect to Your EC2 Instance
Objective: SSH into your server like a cloud engineer.

🔑 SSH Connection
Mac/Linux:
bashchmod 400 ../level-1-launch-ec2/zth-keypair.pem
ssh -i ../level-1-launch-ec2/zth-keypair.pem ec2-user@<Public-IP>
Windows (PowerShell):
powershellssh -i ..\level-1-launch-ec2\zth-keypair.pem ec2-user@<Public-IP>

🧪 Commands to Run
bashuname -a          # OS and kernel info
whoami            # Current user
ls -la            # List files

📸 Required Screenshots
Save in this folder:

01-ssh-connection.png

Successful SSH login message


02-commands-output.png

Output of all 3 commands (uname, whoami, ls)



Also create connection-notes.txt:
OS Version: _______________
Kernel: _______________
Username: _______________
SSH Command Used: _______________

📤 Submission
bashgit add level-2-connect-ssh/
git commit -m "Complete Level 2: SSH Connection"
git push origin main

⚠️ Troubleshooting
Permission denied?

Run: chmod 400 zth-keypair.pem
Verify username: ec2-user

Connection timeout?

Check security group allows SSH from your IP


✅ Completion

 Connected via SSH
 All 3 commands executed
 Screenshots saved
 Notes file created
 Files committed

🏆 Badge Earned: 🟨 Terminal Explorer
Next: Level 3 →
