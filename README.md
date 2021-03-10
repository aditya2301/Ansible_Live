# Ansible_Live
<a href="mailto:aditya_ag2301@yahoo.in"> ![Ask Me Anything](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg?longCache=true&style=plastic)</a>&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;<a href="https://github.com/boudhayan-dev/Automatic-Waste-Segregator/tree/v.01"><img src="https://img.shields.io/badge/Version-0.1-brightgreen.svg?longCache=true&style=for-the-badge"></a>
<br>

Remotely creating an ec2 instance on AWS cloud and host webpage with personalized content

<p>

### Requirements
```
- yum update -y
- sudo amazon-linux-extras install epel -y
- yum install -y $(cat yum_require.txt)
- pip install -r pip_require.txt
```

#### Generate key to be shared on Master Server
ssh-keygen<br>
Generating public/private rsa key pair.<br>
Enter file in which to save the key (/root/.ssh/id_rsa):<br>
Enter passphrase (empty for no passphrase):<br>
Enter same passphrase again:<br>
Your identification has been saved in /root/.ssh/id_rsa.<br>
Your public key has been saved in /root/.ssh/id_rsa.pub.<br>
The key fingerprint is:<br>
SHA256:zzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz root@ip-172-31-95-0.ec2.internal<br>
The key's randomart image is:<br>
+---[RSA 2048]----+<br>
|      .          |<br>
|     o .  o .    |<br>
|      +.oo.+.    |<br>
|     . =O**++o   |<br>
|      ooSO==oo   |<br>
|       = = .+ .  |<br>
|      . . = o. . |<br>
|         . *..+  |<br>
|          .o**E  |<br>
+----[SHA256]-----+<br>


#### Add AWS Cloud Programatic Access Credentials
aws configure<br>
AWS Access Key ID [None]: xxxxxxxxxxxxxxxxxxxx<br>
AWS Secret Access Key [None]: yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy<br>
Default region name [None]: us-east-1<br>
Default output format [None]:<br>

##### In ansible.cfg uncomment the following parameter
host_key_checking = False

##### Test working on the Ansible
ansible localhost -m ping<br>
localhost | SUCCESS => {<br>
    "changed": false,<br>
    "ping": "pong"<br>
}<br>

</p>


<br>


© All rights reserved.
