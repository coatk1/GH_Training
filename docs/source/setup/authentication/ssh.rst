=================================
Cloning with SSH URLs (preferred)
=================================
SSH URLs provide access to a Git repository via SSH, a secure protocol. To use these URLs, you must generate an SSH keypair on your computer and add the public key to your GitHub account. For more information, see "Connecting to GitHub with SSH."

When you ``git clone``, ``git fetch``, ``git pull``, or ``git push`` to a remote repository using SSH URLs, you'll be prompted for a password and must provide your SSH key passphrase.


Check for existing keys
=======================

::
    
    $ ls -al ~/.ssh
    # Lists the files in your .ssh directory, if they exist
    
Check for a file ending in ``.pub``

If it does not exist, then you must generate a new SSH key.

Generating a new SSH key
========================
Paste below text and substitute your email.

::

    $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    
This creates a new ssh key, using the provided email as a label.

::

    > Generating public/private rsa key pair.

When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

::

    > Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]

When prompted for a passphrase, press Enter.

::

    > Enter passphrase (empty for no passphrase): [Press enter]
    > Enter same passphrase again: [Press enter]
    
Add SSH key to ssh-agent
========================
Start ssh-agent

::

    # start the ssh-agent in the background
    $ eval $(ssh-agent -s)
    > Agent pid 59566

Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.

::

    $ ssh-add ~/.ssh/id_rsa
    
Add SSH Key to GitHub account
=============================
Copy the SSH key to your clipboard.

If your SSH key file has a different name than the example code, modify the filename to match your current setup. When copying your key, don't add any newlines or whitespace.

::

    $ clip < ~/.ssh/id_rsa.pub
    # Copies the contents of the id_rsa.pub file to your clipboard

In GitHub, go to **Settings -> SSH and GPG keys -> New SSH key**

For Title, enter "GitHub"

For key, paste your public key.

Test SSH connection
===================
Enter the following in the command line:

::
    
    $ ssh -T git@github.com
    # Attempts to ssh to GitHub
    
.. note:: 
    If any warnings pop up, enter "yes"

You should see this

::

    > Hi username! You've successfully authenticated, but GitHub does not
    > provide shell access.
