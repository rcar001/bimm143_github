## Core Unix Commands

Most Unix commands have super short nomenclature. Which, is time
 saving but requires you to KNOW the commands. 

Major file system related commands include:

pwd: Print working directory 
ls: list files and directory 
cd: change directory 
mkdir: make NEW directory
rm: remove files and directory (delete)
cp: Copy files (source > destination)
mv: Move files or dirs (basically re-name)
nano: A wee text editor (Basic and always available)

curl: Download files from the web or ftp
wget: Download files from the web
tar -zxvf: UnTar(unpakcage) Tar archive files
gunzip: Unzip files
$PATH: The directories to look for programs



## AWS EC2 Instance (Amazon Web Services)

Connect to my instance with: 
ssh -i ~/Downloads/BIMM143_CariasRD.pem ubuntu@ec2-44-251-230-215.us-west-2.compute.amazonaws.com

Above, Log in

Secure copy files btw machines, in this case from our instance to our laptop
scp -i ~/BIMM143_CariasRD.pem ubuntu@Downloads/ec2-44-251-230-215.us-west-2.compute.amazonaws.com:/home/ubuntu/work/bimm143_github/class016/results.txt .

Above, Copy

## Class 017

ssh -i ~/Downloads/BIMM143_CariasRD.pem ubuntu@ec2-16-147-217-77.us-west-2.compute.amazonaws.com

export KEY=~/Downloads/BIMM143_CariasRD.pem

export SERVER=ubuntu@ec2-16-147-217-77.us-west-2.compute.amazonaws.com

ssh -i $KEY $SERVER
scp -r -i $KEY $SERVER:~/*_quant .