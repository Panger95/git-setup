# Installing Git and OpenSSL

<u>Windows:</u>
 1. Chocolatey (Package Manager)

	 a. Open Windows Powershell

	 b. Run the following command
	 
		choco install git openssl
		
	c. Proceed to [Creating SSH Key](#Creating-SSH-Key)
 2. Normal Installation (Recommended)

	 a. Go to: [Download Git](https://git-scm.com/download/win)

	 b. Download the latest version of git and install

	 c. Go to: [Download OpenSSL](https://slproweb.com/products/Win32OpenSSL.html)

	 d. Download and latest version of openssl and install

	 e. Proceed to [Creating SSH Key](#Creating-SSH-Key)
	 
<u>macOS:</u>
 1. HomeBrew (Package Manager) (Recommended)

	 a. Open Terminal

	 b. Run the following command

		brew install git openssl
		
	c. Proceed to [Creating SSH Key](#Creating-SSH-Key)
 2. Normal Installation

	 a. Go to: [Download Git](https://git-scm.com/download/mac)

	 b. Download the latest version of git and install

	 c. Go to: [Download OpenSSL](https://www.openssl.org/source/)

	 d. Download the latest version of openssl and build from source (do not recommend, advanced users only)

	 e. Proceed to [Creating SSH Key](#Creating-SSH-Key)

# Creating SSH Key

<u>Windows:</u>
 1. Open Windows Powershell
 2. Run the following command

		ssh-keygen
		
3. Press Enter to save your new key in your .ssh folder with the default name
4. Press Enter to save your new key with no password (Recommended)
5. Proceed to [Adding Key to GitHub](#Adding-Key-to-GitHub) or [Adding Key to GitLab](#Adding-Key-to-GitLab)
 
<u>macOS:</u>
1. Open Terminal
2. Run the following command

		ssh-keygen
		
3. Press Enter to save your new key in your .ssh folder with the default name
4. Press Enter to save your new key with no password (Recommended)
5. Proceed to [Adding Key to GitHub](#Adding-Key-to-GitHub) or [Adding Key to GitLab](#Adding-Key-to-GitLab)

# Adding Key to GitHub

<u>Windows</u>

 1. Open Windows Powershell
 2. Run the following command

		cd .ssh
		
3. Run the following command look for the filename that ends with `.pub`

		dir

4. Run the following command (replace `FILENAME` with the filename you just found)

		cat FILENAME.pub | clip

5. Go to https://www.github.com/ or your git website
6. Sign into your account
7. Top right click on your profile
8. Click on `Settings`
9. Click on `SSH and GPG keys`
10. Click on `New SSH key`
11. Name the key whatever you want
12. Select `Authentication Key`
13. Click on the text box and `Ctrl + v` or right click and paste
14. Click `Add SSH key`
15. Confirm any prompts
16. Click on `New SSH key`
17. Name the key whatever you want
18. Select `Signing Key`
19. Click on the text box and `Ctrl + v` or right click and paste
20. Click `Add SSH key`
21. Confirm any prompts
22. Proceed to [Setting Up Git](#Setting-Up-Git)

<u>macOS</u>

 1. Open Terminal
 2. Run the follow command

		
		cd .ssh
		
3. Run the following command look for the filename that ends with `.pub`

		ls

4. Run the following command (replace `FILENAME` with the filename you just found)

		cat FILENAME.pub | pbcopy

5. Go to https://www.github.com/ or your git website
6. Sign into your account
7. Top right click on your profile
8. Click on `Settings`
9. Click on `SSH and GPG keys`
10. Click on `New SSH key`
11. Name the key whatever you want
12. Select `Authentication Key`
13. Click on the text box and `Cmd + v` or right click and paste
14. Click `Add SSH key`
15. Confirm any prompts
16. Click on `New SSH key`
17. Name the key whatever you want
18. Select `Signing Key`
19. Click on the text box and `Cmd + v` or right click and paste
20. Click `Add SSH key`
21. Confirm any prompts
22. Proceed to [Setting Up Git](#Setting-Up-Git)

# Adding Key to GitLab

<u>Windows</u>

 1. Open Windows Powershell
 2. Run the following command

		cd .ssh
		
3. Run the following command look for the filename that ends with `.pub`

		dir

4. Run the following command (replace `FILENAME` with the filename you just found)

		cat FILENAME.pub | clip

5. Go to https://www.gitlab.com/ or your git website
6. Sign into your account
7. Top left click on your profile
8. Click on `Preferences`
9. Click on `SSH Keys`
10. Click on `Add new key`
11. Click on the text box and `Ctrl + v` or right click and paste
12. Name the key whatever you want
13. Select `Authentication & Signing`
14. Click the `x` to remove the Expiration date
15. Click `Add key`
16. Confirm any prompts
17. Proceed to [Setting Up Git](#Setting-Up-Git)

<u>macOS</u>

 1. Open Terminal
 2. Run the follow command

		
		cd .ssh
		
3. Run the following command look for the filename that ends with `.pub`

		ls

4. Run the following command (replace `FILENAME` with the filename you just found)

		cat FILENAME.pub | pbcopy

5. Go to https://www.gitlab.com/ or your git website
6. Sign into your account
7. Top left click on your profile
8. Click on `Preferences`
9. Click on `SSH Keys`
10. Click on `Add new key`
11. Click on the text box and `Ctrl + v` or right click and paste
12. Name the key whatever you want
13. Select `Authentication & Signing`
14. Click the `x` to remove the Expiration date
15. Click `Add key`
16. Confirm any prompts
17. Proceed to [Setting Up Git](#Setting-Up-Git)

# Setting Up Git

<u>Windows</u>

 1. Open Windows Powershell
 2. Run the following command (replace `YOUR NAME` with your name)

		git config --global user.name "YOUR NAME"

3. Run the following command (replace `YOUR@EMAIL.COM` with your preferred email address)

		git config --global user.email "YOUR@EMAIL.COM"

4. Proceed to [Learning Git](#Learning-Git)

<u>macOS</u>

 1. Open Terminal
 2. Run the following command (replace `YOUR NAME` with your name)

		git config --global user.name "YOUR NAME"

3. Run the following command (replace `YOUR@EMAIL.COM` with your preferred email address)

		git config --global user.email "YOUR@EMAIL.COM"

4. Proceed to [Learning Git](#Learning-Git)

# Learning Git

1. Keep one of the following cheat sheets handy [GitHub Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf) or [GitLab Cheat Sheet](https://about.gitlab.com/images/press/git-cheat-sheet.pdf)
2. Adding an existing repository to your system

	a. Open Windows Powershell or Terminal and go to your desired directory location

	b. Run the following command (obtain the download url from the existing repo) generally have to look for a button on the repo that says `Code` and then make sure to `Clone with SSH`

		git clone git@github.com:Panger95/using-git.git

3. Adding git to an existing directory

	a.  Open Windows Powershell or Terminal and go to your existing directory location

	b. Run the following commands (replace `COMMIT MESSAGE` with your commit message) and (replace `git@github.com:Panger95/using-git.git` with your git url you obtained from the url page) **WARNING: THIS WILL PUSH YOUR CODE TO THE MASTER BRANCH**

		git init
		git add .
		git commit -m "COMMIT MESSAGE"
		git remote add origin git@github.com:Panger95/using-git.git
		git push origin master

**Note** Git messages should generally be as concise and descriptive as possible

1. Pushing your files to the repo

	a. Open Windows Powershell or Terminal and go to your existing directory location

	b. Run the following commands (replace `COMMIT MESSAGE` with your commit message) **WARNING: THIS WILL PUSH YOUR CODE TO WHATEVER BRANCH YOU ARE CURRENTLY ON**

		git add .
		git commit -m "COMMIT MESSAGE"
		git push
		
**Note** Git messages should generally be as concise and descriptive as possible