#MHS Robotics Club: GIT#

<i>Modified from <a href="https://github.com/susanBuck/notes">Susan Buck's notes</a></i>

<b>Create an account at Github.com</b></br>
Visit [Github.com](http://github.com) and create an account if you don't already have one. 

<b>Generate SSH keys on your computer</b></br>
Via the command line, move into your `.ssh` directory:

Mac: 

```bash
$ cd /Users/YourName/.ssh
```

Windows:

```bash
$ cd C:\Users\YourName\.ssh
```
	
If this `.ssh` directory does not exist, it's okay&mdash; the next step will generate it for you.

Generate a new SSH key with the following command:

```bash
$ ssh-keygen -t rsa -C "your_email@example.com"
```
	
When it asks you for the filename, hit Enter (it will default it `id_rsa`).

```bash
Enter file in which to save the key (/Users/YourName/.ssh/id_rsa): [Press enter]
```

When it asks you for a passphrase you can either create one or leave it blank. Regardless, hit Enter when you're done. 
Same for when it asks you to confirm your passphrase.

It's up to you whether you want to use a passphrase. Entering a passphrase does have its benefits: the security of a key, no matter how encrypted, still depends on the fact that it is not visible to anyone else. Should a passphrase-protected private key fall into an unauthorized users possession, they will be unable to log in to its associated accounts until they figure out the passphrase, buying the hacked user some extra time. The only downside, of course, to having a passphrase, is then having to type it in each time you use the Key Pair.

At this point, if you list the contents in the `.ssh` directory you should see two new files: 

* `id_rsa` (private key)
* `id_rsa.pub` (public key).
	
(Mac users only) Add your new key to the ssh-agent:
 
```bash
$ ssh-add id_rsa
```




<b>Add SSH key at Github.com</b></br>
In Github.com, goto Account Settings (little screwdriver/wrench icon on the top right).

Find the SSH Keys section.

Click Add SSH Key.

In the *Title* field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key *"Personal MacBook Air"*.

For the *Key* field, you want to paste the contents of the `id_rsa.pub` file that was generated on your computer in the above step.

To quickly open this file to copy it's contents, use the following commands...

Mac:

```bash
$ edit id_rsa.pub
```

Windows:

```bash
$ notepad id_rsa.pub
```
	
*Copying the contents of id_rsa.pub on Windows:*
<img src='http://making-the-internet.s3.amazonaws.com/vc-copy-id-rsa-pub-on-windows.png?@2x' style='max-width:1153px; width:75%'>

With the contents of `id_rsa.pub` in your clipboard, paste the contents into the *Key field* on Github.
	
<img src='http://making-the-internet.s3.amazonaws.com/vc-github-save-new-ssh-key.png?@2x' style='max-width:664px; width:75%'>

Finally, click Add key.

To test your new SSH key, run the following command to connect to Github over SSH:

```bash
$ ssh -T git@github.com
```

You may see this warning:	

```bash
The authenticity of host 'github.com (207.97.227.239)' can't be established.
# RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
# Are you sure you want to continue connecting (yes/no)?
```
	
Type `yes` and hit enter.

If all went well, you should see this message:

```bash
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```
	
If that username is yours, you've successfully set up your SSH key.

If you receive a message saying access or permission is denied you can read [these instructions for diagnosing the issue](https://help.github.com/articles/error-permission-denied-publickey).




<b>Next Step: <a href="term.md">Terminology</a></b>