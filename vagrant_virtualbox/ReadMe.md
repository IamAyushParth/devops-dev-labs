#   Existing Infrastructure
1. Win 11
Ram : 16 GB
CPU : i5 12th Gen,
SSD : 500 GB

Ref Blog: https://sites.duke.edu/compsci316_01_f2016/help/vbvagrant/

2. Install Below Software from official website.
   2.1 : Install Virtual Box for Windows. 
     From    https://www.virtualbox.org/wiki/Downloads
   
   2.2 : Download and Install Vagrant for Windows AMD64 Architecture.
         2.2.1 : Ref URL : https://www.vagrantup.com/
3. Add Virtual Box Binary to System Path:
   3.1 Press the Windows key on your keyboard and type Environment Variables. Select Edit the system environment variables.
   3.2 Click the Environment Variables button.
   3.3 Under System Variables, scroll down and find the Path variable. Click Edit.
![image](https://github.com/IamAyushParth/devops-dev-labs/assets/153945547/b852604c-fd72-48f1-9c97-e06a8341c4eb)

4. Open CMD Terminal.
   4.1 :  vagrant --version
            Vagrant 2.4.0
   4.2 : vagrant box add ubuntu/focal64

   PS C:\External Datastore\linux-vm> vagrant box add ubuntu/focal64
==> box: Loading metadata for box 'ubuntu/focal64'
    box: URL: https://vagrantcloud.com/api/v2/vagrant/ubuntu/focal64
==> box: Adding box 'ubuntu/focal64' (v20231207.0.0) for provider: virtualbox
    box: Downloading: https://vagrantcloud.com/ubuntu/boxes/focal64/versions/20231207.0.0/providers/virtualbox/unknown/vagrant.box
Download redirected to host: cloud-images.ubuntu.com
    box:
==> box: Successfully added box 'ubuntu/focal64' (v20231207.0.0) for 'virtualbox'!

4.3 : vagrant plugin install vagrant-vbguest

4.4 : Move to New empty Directory. Note: There should not be any existing vagrantefile in that directory. 
      4.4.1: Create Vagrant file Using command
      vagrant init ubuntu/focal64

4.5 :  Create and Start VM
       vagrant up
      
4.6 : From your host shell, log into your VM:
vagrant ssh

To come out: exit from ssh session. 

4.7: Checking the VM status:
vagrant status

4.8 : Stopping the VM:
vagrant halt

4.9 : Destroying the VM:
vagrant destroy

##   Destorying VM's

PS C:\External Datastore> vagrant halt
==> default: Attempting graceful shutdown of VM...
PS C:\External Datastore> vagrant destroy
    default: Are you sure you want to destroy the 'default' VM? [y/N] y
==> default: Destroying VM and associated drives..


   
   

   
         
