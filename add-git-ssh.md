#Commands

#Step 1: Generate Your SSH Key
Make sure Git Bash is open. To generate an SSH key use the following command. Be sure to replace the fake email with your real email address.

$ ssh-keygen -t rsa -b 4096 -C "example@example.com"

#Step 2: Use the Key
Now that the key is generated, we need to put it to use. Start by starting the ssh agent.

$ eval $(ssh-agent -s)

Then add the key we just generated. If you selected a different path than the default, be sure to replace that path in the command.

$ ssh-add ~/.ssh/id_rsa

#Step 3: Add the SSH Key on GitHub
Now that we have the ssh key setup on our computer, we need to set it up on the GitHub website. First, we will use a command to copy it to our clipboard and then paste it on to GitHub.

$ clip < ~/.ssh/id_rsa.pub

Next, go ahead and open GitHub in your web browser. Navigate to Settings (under your picture), then click SSH and GPG Keys. Click New SSH Key and give it a title. Then paste your key into the Key box. If it wasn’t copied properly, go back and open the file and then copy it or try the command again.