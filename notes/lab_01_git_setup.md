Lab Report – Secure Shell (SSH) Basics & Git Workflow

Date: 2025-20-11
Author: Brandon Asilatsa Dounya
1. Objective

This lab introduces the fundamentals of Secure Shell (SSH) usage, why it matters in cybersecurity, and how to record terminal sessions for documentation. A secondary goal was practicing Git version control by creating, committing, and pushing lab files to a remote GitHub repository.
2. What I Learned
✔ What SSH Is

SSH (Secure Shell) is a protocol that allows secure access to remote systems.

It encrypts communication to prevent eavesdropping and man-in-the-middle attacks.

Used by system administrators, penetration testers, and DevOps engineers.

✔ Why SSH Matters in Cybersecurity

Provides encrypted remote administration.

Allows secure file transfer (SCP, SFTP).

Helps manage servers without physical access.

Critical for penetration testing (pivoting, tunneling, etc.).

Reduces risks associated with plaintext protocols like Telnet.
3. Commands Executed
3.1 Checking Open Ports
sudo ss -tulnp


Shows active TCP/UDP ports and listening services.
3.2 Recording a Terminal Session

Start recording:

script ssh_session_$(date +%F_%H%M).txt


Stop recording:

exit
3.3 Setting Up Git Configuration
git config --global user.name "ASILATSA DOUNYA BRANDON"
git config --global user.email "bdounya01@gmail.com"
git config --global credential.helper store
3.4 Initializing a Git Repository
git init
mkdir -p notes
echo "# Lab notes" > notes/README.md
git add .
git commit -m "Init LABS notes"
3.5 Connecting to GitHub
git remote add origin https://github.com/BRANDONDOUNYA/lab-notes.git
git branch -M main
git push -u origin main
4. Files Generated

notes/README.md → Documentation folder intro

notes/lab_ssh_2025-20-11.md → This report

notes/ssh_session_2025-20-11_xxxx.txt → Recorded terminal session

Other practice files created during the lab
5. Key Takeaways

SSH is essential for secure remote access.

Always verify your Git configuration before committing.

Personal Access Tokens (PATs) are required for GitHub authentication.

Maintaining clear documentation is part of being a cybersecurity professional.

Version control is non-negotiable in real-world engineering.
6. Next Steps

Practice SSH connections using a VM-to-VM setup.

Learn SSH key-based authentication.

Continue documenting each lab in the same repository.

Push all lab reports to GitHub for portfolio building.
