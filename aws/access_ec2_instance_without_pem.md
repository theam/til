José Manuel Martínez & Sebastían Pérez

# How to access an EC2 instance if you don't own the PEM file

1. Log in AWS Console.

1. Go to EC2.

1. Launch a new instance with same region and VPC as the lost pem file instance and get its PEM file.

1. Now stop the lost pem file instance. Remember not to terminate instance but to stop it.

1. Go to Elastic Block Store volumes, select the root volume of the lost pem file instance and detach it.

1. Select the detached volume and attach it to the new instance. Since this new instance already has a root volume by default as /dev/sda1, the newly attached volume will be secondary (eg: /dev/sdf).

1. Log in the new EC2 instance with its pem file.

1. Execute below commands:

	```bash
	# mount /dev/xvdf1 /mnt
	# cp /root/.ssh/authorized_keys /mnt/home/ubuntu/.ssh/
	# umount /mnt
	```

1. Detach the secondary volume from the new EC2 instance. 

1. Attach again the volume back to our recovery instance. 

1. Start the instance. 

1. Terminate the new EC2 instance.

1. Use new EC2 instance PEM file to log into recovery instance.