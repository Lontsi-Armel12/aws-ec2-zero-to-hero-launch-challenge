LEVEL 7: Cost Optimization
Objective: Learn to avoid surprise AWS bills.

💰 Answer These Questions
Create cost-optimization-answers.txt:
1. Why is t2.micro free tier eligible?
Answer: _______________________________________________
_______________________________________________

2. What's the difference between Stop vs Terminate?
Answer: _______________________________________________
_______________________________________________

3. When does EC2 cost money?
Answer: _______________________________________________
_______________________________________________

4. List 3 ways to avoid extra billing:
   a) _______________________________________________
   b) _______________________________________________
   c) _______________________________________________

🧾 Check Your AWS Bill

AWS Console → Billing Dashboard
Review Month-to-Date charges
Check Free Tier usage

Create billing-snapshot.txt:
Current Month-to-Date Charges: $_______
Free Tier EC2 Hours Used: _______/750
Free Tier EBS Storage Used: _______/30 GB
Any Unexpected Charges?: Yes/No

📸 Required Screenshots
Save in this folder:

01-billing-dashboard.png

AWS Billing Dashboard overview


02-free-tier-usage.png

Free Tier usage details




💡 Cost Saving Checklist
Before completing this challenge:

 Understand free tier limits (750 hrs/month)
 Know that stopped instances still cost (EBS storage)
 Know when to Stop vs Terminate
 Have checked billing dashboard
 Ready to terminate resources


🧹 Clean Up (FINAL STEP)
Now it's time to terminate your instance:

EC2 Console → Select ZeroToHero-EC2
Instance State → Terminate
Confirm termination
Go to Volumes → Delete the 2GB EBS volume
Go to Security Groups → (keep or delete zth-security-group)

Take a final screenshot: 03-resources-terminated.png

📤 Submission
bashgit add level-7-cost-optimization/
git commit -m "Complete Level 7: Cost Optimization - Challenge Complete!"
git push origin main

✅ Completion

 4 questions answered
 Billing dashboard checked
 Understand Stop vs Terminate
 3 screenshots saved
 Instance terminated
 EBS volume deleted
 Files committed

🏆 Badge Earned: 🟧 Cloud Economist

🎉 CHALLENGE COMPLETE!
🏆 All Badges Earned:
🟤 Cloud Explorer
🟡 Instance Launcher
🟨 Terminal Explorer
🟪 Cloud Developer
🟫 Storage Handler
🔵 Security Defender
🟩 Lifecycle Commander
🟧 Cloud Economist

🎓 What You've Mastered
✅ Launch and configure EC2 instances
✅ Connect via SSH
✅ Install and deploy web servers
✅ Manage EBS storage
✅ Configure security groups
✅ Control instance lifecycle
✅ Optimize costs and avoid bills

🚀 Next Steps

AWS Certification: Study for AWS Cloud Practitioner
Expand Skills: Learn S3, Lambda, RDS
Build Projects: Deploy your own applications
Join Community: Share your success on LinkedIn!


Share your completion:
🎉 Just completed the Zero-to-Hero EC2 Challenge!

Learned: EC2, SSH, Apache, EBS, Security Groups, Cost Optimization

#AWS #CloudComputing #EC2 #DevOps

Back to Main README
