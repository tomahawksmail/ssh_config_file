# ssh_config_file
ssh config template


```
# Special host
Host name
	HostName dns or IP
	User username
	Port 22

# host ending ".eu-west-1.compute.amazonaws.com"
Host *.eu-west-1.compute.amazonaws.com
	User ec2-user
	IdentityFile ~/.ssh/key1.pem

# host ending ".eu-east-2.compute.amazonaws.com"
Host *.eu-west-1.compute.amazonaws.com
	User ec2-user
	IdentityFile ~/.ssh/key2.pem

#for all hosts
Host *
	StrictHostKeyChecking no # no more fingerprint
	UserKnownHostsFile /dev/null # do not create known_hosts file
```
