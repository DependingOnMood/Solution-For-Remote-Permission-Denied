# Solution-For-Remote-Permission-Denied

solution for remote: Permission to githubuser1/gitrepo1.git denied to githubuser2.

This really take me a lot of time, and almost all anwsers on the web are not helpful. So I think that I should share my experience with this and hopefully wil convenience people.

I was trying to use terminal on my Mac to upload some code to GitHub using an account that was different to my usual one. I set the following three settings:

git config --global user.name "My Name"
git config --global user.email "myemail"
git config --global GitHub.user myusername

Sadly I kept receiving a 403 error saying my usual username couldn't access the repository with my usual account details.

I reset the whole SSH keys both in my usual accound and new, and it still didn't work.

Somehow I noticed it might because my username and password were being cached. Now I don't recall setting this up but somewhere along the line I used KeyChain to save my password. 

I found my old gitHub Username and password in the Keychain. So I deleted all of them. Now when I try to push from command line, it will prompt you for your username and password. Or if you didn't delete your new username and password in keychain and thats the only one left in Keychain for gitHub. It will work as you want.
