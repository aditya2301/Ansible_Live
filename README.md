# Ansible_Live
<a href="mailto:aditya_ag2301@yahoo.in"> ![Ask Me Anything](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg?longCache=true&style=plastic)</a>&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;<a href="https://github.com/boudhayan-dev/Automatic-Waste-Segregator/tree/v.01"><img src="https://img.shields.io/badge/Version-0.1-brightgreen.svg?longCache=true&style=for-the-badge"></a>
<br>

Remotely creating an ec2 instance on AWS cloud and host webpage with personalized content

<p>

### Requirements
yum update -y
sudo amazon-linux-extras install epel -y
yum install -y $(cat yum_require.txt)
pip install -r pip_require.txt

#### Generate key to be shared on Master Server
ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/root/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /root/.ssh/id_rsa.
Your public key has been saved in /root/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:R8qZi1G2QuT59mORnaH+rmU+e5BgJnxidudEolP/a9o root@ip-172-31-95-0.ec2.internal
The key's randomart image is:
+---[RSA 2048]----+<br>
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


#### Add AWS cloud Programatic Access credentials
aws configure
AWS Access Key ID [None]: AKIAJFQBB3NT2BITL3FA
AWS Secret Access Key [None]: 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
Default region name [None]: us-east-1
Default output format [None]:

##### In ansible.cfg uncomment the following parameter
host_key_checking = False

##### Test working on the Ansible
ansible localhost -m ping
localhost | SUCCESS => {
    "changed": false,
    "ping": "pong"
}

</p>


<br>


© All rights reserved.
