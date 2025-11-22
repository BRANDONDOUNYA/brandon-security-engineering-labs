Lab 3 – File Permissions & Basic Command-Line Skills

Author: Brandon Asilatsa Dounya
Date: 22  November 2025
Course: Introduction to Linux & Cybersecurity Labs

1. Objectives

Create and manage files/directories.

Edit text files using Nano.

Apply secure file permissions with chmod.

Inspect files using basic Linux tools (ls, file, strings, grep).

2. Tasks Completed
2.1. Create Project Directory
mkdir lab3_project

2.2. Create secret.txt File
touch lab3_project/secret.txt
nano lab3_project/secret.txt


Content written:
Linux is the backbone of cybersecurity.

2.3. Apply Secure Permissions
chmod 600 lab3_project/secret.txt


This restricts the file so only the owner can read/write.

2.4. Verify Permissions
ls -l lab3_project/secret.txt

2.5. Inspect File Type
file lab3_project/secret.txt

2.6. Extract Printable Strings
strings lab3_project/secret.txt

2.7. Search Keyword in File
grep "cyber" lab3_project/secret.txt

3. Output Screenshots / Terminal Results

(Paste your terminal output here or describe it)

Permissions displayed as:
-rw-------

grep successfully found the keyword cyber.

4. What I Learned

How Linux file permissions work (especially 600).

How to create, edit, and inspect files using native Linux tools.

Importance of securing sensitive data using minimal-access principles.

5. Conclusion

This lab reinforced the foundations of Linux system navigation and file security, which are essential for cybersecurity workflows. The ability to manage file permissions correctly is a key skill for securing systems and preventing unauthorized access.
