# Prerequisites for Vbox Ununtu

1) go to http://dlc-cdn.sun.com/virtualbox/4.3.26/index.html and grab the latest version of virtualbox 4.3.26-98988 for your os and the extention pack for 4.3.26-98988. also grab the VBoxGuestAdditions_4.3.26.iso.

2) go to http://releases.ubuntu.com/14.04/ and click on the decktop image download, or find it below in the server directory.

3) install virtualbox and the extensions pack.

4) create a system FIXED partition for ubuntu. once done close virtual box

5) navigate to virtual box directory (in windows its in the user directory, dont know where it is for mac...) open up the folder that is titled after the virtualbox machine you just made. 

6) open the vbox set up file (the small one, 7kb or so, its blue) in notpadd++ or sublime and scroll down until you see VRAMsize. change that to 256, save and exit

7) launch virtual box, check to make sure that the system image has 256 vram in the display tab in the settings menu, also make sure the enable 3D acceleration option is checked. mount the ubuntu iso you downloaded into the empty drive slot under storage in settings menu and click ok.

8) launch the virtual box and install ubuntu. 

9) go grab a coffee

# Setting up Ubuntu Environment with scripts

0) start ubuntu and follow the steps from within the vbox image

1) go to https://github.com/iliabenson/comp424s and click download Zip on the right

2) unzip the folder and take all the scripts and put them into a new file called Scripts in your home directory. this is important, the new folder has to be in your home directory and it has to be called Scripts a with a capitol S.

3) open up a terminal in your by pressing CTRL+ALT+T and type "cd ./Scripts"

4) from there type "ls -l -a"

5) for each script type "chmod u+x NAME" where NAME is the name of the script that was displayed from step 4.

6) first execute the vbox_unity_setup by typeing "./vbox_unity_setup" there are on screen instructions and it requires some manual entering of information but it is quick

7) next run the ubuntu_setup script by typing "./ubuntu_setup" this script is automated and it will restart your vbox image after completion.

8) go grab a coffee, this script might take a minute

9) once ubuntu is up and running again it should be full screen, if not contact the idiot who wrote this tutorial. 

10) if all is well then cd back into Scripts directory, then run the lamp_stack script byt typing "./lamp_stack" this script is not automated, follow the instructions and say yes to everything, we will configure lamp stack properly later.

# Configure ubuntu

1) search for gufw, its the firewall configuration. originally, iptables was just a network configuration command line program which was complicated as all hell, it then bacame managed by ufw, which stands for uncomplicated firewall. it too is a command line program but way better. gufw is the gui verion of ufw. once it opens just turn status to "on" and set profile to "public". and we are done with firewall for now. 

2) check if apache is running, type "service apache2 status" if it is running open up browser and go to localhost/info.php you should see php info page. if apache is not running start it (type "service apache2 start") and then go to localhost/info.php.

3) configure the lamp stack, soon

4) snort, soon
