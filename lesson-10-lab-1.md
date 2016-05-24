# Lesson 10 Lab 1
## Stand up an EC2 server (15 mins)
1. Setup a billing alert using the instructions in this link so you are alerted if you somehow go over the free tier: https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/free-tier-alarms.html
2. Launch an EC2 instance using the default wizard - Amazon Linux AMI on a t2 micro. Click the Review and Launch button to get to the review screen. ![](https://raw.githubusercontent.com/coreym/DAT-35-class-10/master/assets/launch_instance_button.png)
3. On the review page - ensure your security group is open to the correct ports for the Jupyter notebook: ![](https://raw.githubusercontent.com/coreym/DAT-35-class-10/master/assets/edit_security_groups.png)![](https://raw.githubusercontent.com/coreym/DAT-35-class-10/master/assets/security_group_settings.png)
4. Create a new key pair when prompted and remember where you downloaded it! [](https://raw.githubusercontent.com/coreym/DAT-35-class-10/master/assets/key_pair_settings.png)
5. Attempt to connect to the box via SSH: 
  - *Mac instructions*:
	1. At the terminal, `cd` to the folder you downloaded your key pair. 
	2. Type `chmod 0400 keyname.pem` if you saved it with the name `keyname.pem`.
	3. Copy and paste the example SSH connection string from the 'connect' popup into the terminal and hit enter to run it. ![](https://raw.githubusercontent.com/coreym/DAT-35-class-10/master/assets/connect_link.png) ![](https://raw.githubusercontent.com/coreym/DAT-35-class-10/master/assets/example_ssh_connection_string.png)
  - *PC instructions*:
  - Option 1: Connect using the Putty instructions here: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/putty.html?icmpid=docs_ec2_console
  - Option 2: Use the Java-based in-browser SSH client option from the Connect dialog box if you can get that to work
6. If successful, you should see a connection message like this: 

```
Last login: Tue May 24 18:06:59 2016 from cpe-67-245-249-239.nyc.res.rr.com

       __|  __|_  )
       _|  (     /   Amazon Linux AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-ami/2016.03-release-notes/
9 package(s) needed for security, out of 17 available
Run "sudo yum update" to apply all updates.
```
7. Paste your public DNS name in the slack channel when you're done ![](https://raw.githubusercontent.com/coreym/DAT-35-class-10/master/assets/public_dns_name.png)
