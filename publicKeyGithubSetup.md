Whenever getting error message: Permission denied(publickey) when performing operation in github.

You can follow below steps in Mac or Linux-
1. Check for existing keys-
   ls -al ~/.ssh

2. Create key if does not exist-
   Paste the text below, substituting in your GitHub email address.
   ssh-keygen -t ed25519 -C "your_email@example.com"

   When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

   At the prompt, type a secure passphrase.

3. Adding your SSH key to the ssh-agent-
   Fire up the SSH agent and add the key
   
   eval `ssh-agent -s`
   
   ssh-add ~/.ssh/id_ed25519

4. Adding key to Github account-
   Pull up the key and add to Github account
   cat ~/.ssh/id_ed25519.pub
   Navigate to Github account and add key

Hooray! now you should be able to push files to Github account.
