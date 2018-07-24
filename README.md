# The-Data-Science-Toolkit/Steps Required to Configure a new Jupiter Data Science Notebook Server on Amazon Website
##1.	Register for Amazon Aws for free or paid account which, if paid result to 8.00 per month
##2.  2.	Create SSH key 
An SSH key consists of two types of files. The private key, which should never be shared with anyone. The public key which allows you to log into the containers and VMs you provision. 
###1.	To generate the SSH key , enter command “ ssh-keygen -t rsa” in the Terminal. This starts the key generation process. When you execute this command, the ssh-keygen utility prompts you to indicate where to store the key.
##2.  Press the ENTER key to accept the default location. The ssh-keygen utility prompts you for a passphrase.
##3.  Your private key is saved to the id_rsa file in the .ssh directory and is used to verify the public key you use belongs to the same Triton Compute Service account.
##4.  Your public key is saved to the id_rsa.pub;file and is the key you upload to your Triton Compute Service account. You can save this key to the clipboard
##5.  Type “pbcopy < ~/.ssh/id_rsa.pub
##6.  After you copy the SSH key to the clipboard, return to your account page
##7.  Choose to Import Public Key and paste your SSH key into the Public Key field
##8.  In the Key Name field, provide a name for the key. Note: although providing a key name is optional, it is a best practice for ease of managing multiple SSH keys
##9.  Add the key. It will now appear in your table of keys under SSH
##10. On Amazon E2 ,Create security group
##11. Launch a new Ec2 Instance
##12. Provision a new instance with Docker
##13. Pull the data science notebook image
##14. Run a data science notebook container
##15. Get the token and use on Jupiter
#Budget of the costs of running a Jupyter Data Science Notebook Server for three months using at least three different kinds of EC 2 instances
#a. m4.10xlarge cost $2.00 per hour and $4,320 for three months 
#b. m4.xlarge cost $0.20 per hour and $432 for three months
#c. m4.4xlarge cost $0.80 per hour and $1728 for three months
