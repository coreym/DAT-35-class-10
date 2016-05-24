#Lesson 10 lab 4

##Configure and launch jupyter hub(15 mins)
Documentation link: http://jupyter-notebook.readthedocs.io/en/latest/public_server.html#notebook-public-server
1. In your SSH terminal, run jupyter notebook --generate-config 

```
MacBook-Air:assets corey$ ssh -i ~/.ssh/GAlab.pem ec2-user@ec2-52-39-178-176.us-west-2.compute.amazonaws.com
Last login: Tue May 24 20:03:33 2016 from cpe-67-245-249-239.nyc.res.rr.com

       __|  __|_  )
       _|  (     /   Amazon Linux AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-ami/2016.03-release-notes/
9 package(s) needed for security, out of 17 available
Run "sudo yum update" to apply all updates.
[ec2-user@ip-172-31-36-223 ~]$ jupyter notebook --generate-config
```

2. run `nano jupyter_notebook_config.py`
3. In the nano text editor you just launched, search for the following configuration directives (control-W for search):
	- set `c.NotebookApp.open_browser = False`
	- set `c.NotebookApp.port = 8888`
	- set `c.NotebookApp.open_browser = False`
	- set `c.NotebookApp.ip = '*'`
4. In nano, `control-x` to writeout (save) 
5. Back on the command line, run `jupyter notebook`
6. Bingo! In a browser, go to the public DNS name for the EC2 instance you launched in lab 1 with a trailing semicolon and 8888 in the url, and you should see your new notebook server running. EX: `http://ec2-52-39-178-176.us-west-2.compute.amazonaws.com:8888/` ![](https://raw.githubusercontent.com/coreym/DAT-35-class-10/master/assets/public_dns_name.png)