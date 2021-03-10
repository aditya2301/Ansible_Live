# Ansible_Live
<a href="mailto:aditya_ag2301@yahoo.in"> ![Ask Me Anything](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg?longCache=true&style=plastic)</a>&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;<a href="https://github.com/boudhayan-dev/Automatic-Waste-Segregator/tree/v.01"><img src="https://img.shields.io/badge/Version-0.1-brightgreen.svg?longCache=true&style=for-the-badge"></a>
<br>

Remotely creating an ec2 instance on AWS cloud and host webpage with personalized content


### Requirements
##### To run on Ansible Master server
```
- yum update -y
- sudo amazon-linux-extras install epel -y
- yum install -y $(cat yum_require.txt)
- pip install -r pip_require.txt
```
### Setup
##### Step 1: Generate key to be shared on Master Server
<pre>
```
ssh-keygen
```
Generating public/private rsa key pair.
Enter file in which to save the key (/root/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /root/.ssh/id_rsa.
Your public key has been saved in /root/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:zzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz root@ip-172-31-95-0.ec2.internal
The key's randomart image is:

+---[RSA 2048]----+
|      .          |
|     o .  o .    |
|      +.oo.+.    |
|     . =O**++o   |
|      ooSO==oo   |
|       = = .+ .  |
|      . . = o. . |
|         . *..+  |
|          .o**E  |
+----[SHA256]-----+
</pre>

##### Step 2: Add AWS Cloud Programatic Access Credentials in place of xxxxx and yyyyy and enter region to work. (Here default North Virgina is chosen)
<pre>
```
aws configure
```
AWS Access Key ID [None]: xxxxxxxxxxxxxxxxxxxx
AWS Secret Access Key [None]: yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy
Default region name [None]: us-east-1
Default output format [None]:
</pre>

##### Step 3: In ansible.cfg uncomment the following parameter for disable ssh connectivity prompt
<pre>
host_key_checking = False
</pre>

##### Step 4: Test working on the Ansible
<pre>
```
ansible localhost -m ping
```
localhost | SUCCESS => {
    "changed": false,
    "ping": "pong"
}
</pre>


<br>


© All rights reserved.
