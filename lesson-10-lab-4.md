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
5. Back on the command line, run `jupyter notebook`. If successful, you should see something like this: 
```
[ec2-user@ip-172-31-36-223 ~]$ jupyter notebook
/usr/local/lib/python2.7/site-packages/widgetsnbextension/__init__.py:30: UserWarning: To use the jupyter-js-widgets nbextension, you'll need to update
    the Jupyter notebook to version 4.2 or later.
  the Jupyter notebook to version 4.2 or later.""")
[W 23:17:13.469 NotebookApp] WARNING: The notebook server is listening on all IP addresses and not using encryption. This is not recommended.
[W 23:17:13.469 NotebookApp] WARNING: The notebook server is listening on all IP addresses and not using authentication. This is highly insecure and not recommended.
[I 23:17:13.474 NotebookApp] Serving notebooks from local directory: /home/ec2-user
[I 23:17:13.474 NotebookApp] 0 active kernels 
[I 23:17:13.474 NotebookApp] The Jupyter Notebook is running at: http://[all ip addresses on your system]:8888/
[I 23:17:13.474 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
```
6. Bingo! In a browser, go to the public DNS name for the EC2 instance you launched in lab 1 with a trailing colon and 8888 in the url, and you should see your new notebook server running. EX: `http://ec2-52-39-178-176.us-west-2.compute.amazonaws.com:8888/` ![](https://raw.githubusercontent.com/coreym/DAT-35-class-10/master/assets/public_dns_name.png)
