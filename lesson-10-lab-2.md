#Lesson 10 lab 2
## Get your packages installed on the server (20 mins)
1. Install (in order) the following yum packages (OS-level software that python needs in order to install the Python packages in step 2):
	- `sudo yum install gcc`
	- `sudo yum install gcc-c++`
	- `sudo yum install libpng-devel`
	- `sudo yum install freetype-devel`
	- while they're installing, take a look at the AWS docs for their package manager: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/install-software.html
2. Install (in order) the following pip packages: 
	- `sudo pip install jupyter`
	- `sudo pip install pandas`
	- `sudo pip install --no-cache-dir matplotlib`
3. Flag me for any issues! 