✅ LAB REPORT 2 — Configuring SSH Authentication for GitHub
Title:

Secure GitHub Access Using SSH Keys (Lab 02)

Date:
Friday 21 november 2025

Objective:

Enable secure, password-less authentication between Kali Linux and GitHub using SSH keys. This improves workflow, enhances security, and prepares the environment for future DevOps and cybersecurity projects.

1. SSH Key Generation

To create a modern and secure SSH key pair, I used the Ed25519 algorithm:

ssh-keygen -t ed25519 -C "bdounya01@gmail.com"


Result:

A private key was created at: ~/.ssh/id_ed25519

A public key was created at: ~/.ssh/id_ed25519.pub

2. Viewing the Public Key

To copy the public key for GitHub, I displayed it in the terminal:

cat ~/.ssh/id_ed25519.pub


This output was then copied and added to my GitHub SSH settings.

3. Adding the SSH Key to GitHub

I navigated to:

GitHub → Settings → SSH and GPG keys → New SSH key

I pasted the .pub file content and saved it.

4. Testing SSH Authentication

To verify that the connection was fully operational, I ran:

ssh -T git@github.com


Expected successful output:

Hi BRANDONDOUNYA! You've successfully authenticated, but GitHub does not provide shell access.


This confirmed that GitHub recognized my SSH key and accepted the connection.

5. Switching Repository from HTTPS to SSH

To avoid password prompts and use my SSH key automatically, I switched the Git remote URL:

cd ~/LABS
git remote set-url origin git@github.com:BRANDONDOUNYA/lab-notes.git


Pushing to GitHub now works seamlessly:

git push


No username/password required — SSH works perfectly.

Conclusion

This lab successfully established a secure SSH-based workflow between Kali Linux and GitHub.
I can now push, pull, and manage repositories without any authentication prompts.
This setup aligns with real-world cybersecurity and DevOps best practices, and strengthens both security and productivity.

