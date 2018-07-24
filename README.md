# The-Data-Science-Toolkit/Steps Required to Configure a new Jupiter Data Science Notebook Server on Amazon Website

## Registering for Amazon AWS AND SSH KEYS
1.	Register for Amazon Aws for free or paid account which, if paid result to 8.00 per month
2.  Create SSH key 
3. An SSH key consists of two types of files. The private key, which should never be shared with anyone. The public key which allows you to log into the containers and VMs you provision. 
To generate the SSH key , enter command “ ssh-keygen -t rsa” in the Terminal. This starts the key generation process. When you execute this command, the ssh-keygen utility prompts you to indicate where to store the key.
Press the ENTER key to accept the default location. The ssh-keygen utility prompts you for a passphrase.
Your private key is saved to the id_rsa file in the .ssh directory and is used to verify the public key you use belongs to the same Triton Compute Service account.
Your public key is saved to the id_rsa.pub;file and is the key you upload to your Triton Compute Service account. You can save this key to the clipboard
4. Type `pbcopy < ~/.ssh/id_rsa.pub`
5. After you copy the SSH key to the clipboard, return to your account page
6. Choose to Import Public Key and paste your SSH key into the Public Key field
7. In the Key Name field, provide a name for the key. Note: although providing a key name is optional, it is a best practice for ease of managing multiple SSH keys
8. Add the key. It will now appear in your table of keys under SSH

## SECURITY GROPUP, EC2 INSTANCE AND DOCKER
1. On Amazon E2 ,Create security group
2. Launch a new Ec2 Instance
3. Provision a new instance with Docker 
Install Docker. In git bash, using command *curl -sSl https://get.docker.com | sh* to get docker, then using 
 command *sudo usermod -aG docker ubuntu*, reconnect/SSH to AWS using command *Docker -v*
4. Pull the data science notebook image
Use command *Docker pull jupyter/datascience-notebook* to obtain the correct imag
5. Run a data science notebook container
command *docker run -p 80:8888 -v /home/ubuntu:/home/jovyan jupyter/datascience-notebook* and then copy and paste token to ip:443 to open jupyter
6. Get the token and use on Jupiter
Security: notebook uses token to authenticate requests

## BUDGET FOR RUNNING A JUPYTER DATA SCIENCE NOTEBOOK SERVER FOR THREE MONTHS 

#a. m4.10xlarge cost $2.00 per hour and $4,320 for three months 
#b. m4.xlarge cost $0.20 per hour and $432 for three months
#c. m4.4xlarge cost $0.80 per hour and $1728 for three months

![alt text](https://github.com/samson77766/The-Data-Science-Toolkit/blob/master/Data%20science%20toolkit.jpg)
