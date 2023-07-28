

Install sshpass for ansible controller to connect to the target machines via ssh
wget http://sourceforge.net/projects/sshpass/files/sshpass/1.05/sshpass-1.05.tar.gz/download # on your amazon instance, to download using command line / terminal; this will get you a file named "download"

$ mv download sshpass-1.05.tar.gz # note this is the name as in the URL above

$ gunzip sshpass-1.05.tar.gz
$ tar xvf sshpass-1.05.tar

$ cd sshpass-1.05

$ sudo yum groupinstall "Development Tools" # in case configure & make (next 2 commands) does not work, else dont run this command

$ sudo ./configure

$ sudo make install

$ sudo -s
# which sshpass #sudo -s and check if sshpass is in the path; on amazon RHEL, for me the root did not have /usr/local/bin in its path; so you may want to set the path appropriately (echo $PATH), or copy sshpass to one of the $PATH directories
   
