# ubuntuserver

This project is about creating a domain controller using SAMBA and Ubuntu Server.

Hardware:

System76 Meerkat 
Dell 3630 

Questions:

Scope:

Need two (2) domain controllers on two different machines for redundancy.

So far:

Ubuntu Server installed on Meerkat
A whole section about Multipass

Need to install 'Multipass' to take tutorials. I believe this is just a VM that similates using Ubuntu Server, and I am not following along on my actual Server installation. https://ubuntu.com/server/docs/tutorial/welcome-to-the-terminal/#welcome-to-the-terminal
Prerequisite for Windows installation: 'Virtual Machine Platform' must be enabled.
Start -> Windows features -> Admin Password -> Features Window -- Verified enabled on my Windows 11 Laptop.
Downloaded and installed multipass on Win11 laptop.
Verified by opening CMD and typing: multipass version
multipass 1.17.0+win
multipassd 1.17.0+win
Launch multipass: multipass launch

To upgrade: Run the latest installer

Create the Virtual Machine:

multipass launch resolute --name tutorial
Response: Launched: tutorial in zone1

Once the above command has finished running, we can access the VM by running:

multipass shell tutorial
We will get a “Welcome to Ubuntu” message. Notice that when we run this command, the terminal username changes to ubuntu and the hostname changes to tutorial: ubuntu@tutorial:~ $

This shows that we are inside the VM, and this is where we will run all our commands. Now that our setup is complete, let’s carry on with the tutorial!

Other commands: whoami

ls

touch - creates a document

mkdir - Create a folder

mv - move files (deletes the old file) (rename)

mv # Move all the named files to this folder

mv *.txt my-folder - move all text files to the folder - Asterisk is wild card

mv file2.txt new-folder/file2.txt - move the target file into a different folder

mv file2-renamed.txt ../file2.txt - move the file back one folder and rename it

The cp command is not just for files. We can make backup copies of a whole directory (and all its contents) using the -a (or --archive) flag. This flag preserves all the file permissions:

cp -a new-folder/ new-folder-backup/

cp file1.txt file2.txt - copies file from 1 to 2 (does not delete old file)

cp file1.txt new-folder/ - moves the text into a folder

cd - change directory

pwd - print working directory

rmdir - remove directory (will only allow if folder is empty) (safe option)

rm - remove

rm -r my-folder - Will recursively delete the my-folder and all subdirectories

The rm command won’t let you delete a directory without the -r flag, but it also won’t stop you (or ask if you’re really, truly sure) when deleting a folder and all its contents
That's enough for tonight. Tomorrow I will reinstall Ubuntu Server on both boxes and name them meerkat and 3630.

Then I will continue with the tutorials.
