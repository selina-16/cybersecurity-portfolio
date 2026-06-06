File permissions in Linux
Project description
In this project, I used Linux commands to examine and manage file permissions for a research team. I reviewed file and directory permissions, identified unauthorized access, and modified permissions using the chmod command. These actions helped ensure that only authorized users could access sensitive files and directories.

Check file and directory details
I used the following command to view all files, directories, and permissions, including hidden files:
ls -la
This command displays file permissions, ownership information, file sizes, and hidden files that begin with a period (.).

Describe the permissions string
-rw-rw-r--
Explanation:
The first character (-) indicates that the item is a file.
The next three characters (rw-) show the owner's permissions: read and write.
The next three characters (rw-) show the group's permissions: read and write.
The last three characters (r--) show others' permissions: read only.
This 10-character string helps identify who can access a file and what actions they can perform.

Change file permissions
I identified a file that allowed write access to others and removed that permission using:
chmod o-w project_k.txt
This command removes write permissions for others and helps prevent unauthorized modifications.

Change file permissions on a hidden file
The hidden file .project_x.txt required updated permissions. I used:
chmod u-w,g-w,o-r .project_x.txt
This command removes write permissions for the user and group while ensuring the group retains read access.

Change directory permissions
The drafts directory should only be accessible by researcher2. I modified its permissions using:
chmod g-x drafts
This command removes execute permissions from the group, restricting access to the directory.

Summary
In this project, I used Linux commands to inspect and modify file permissions. I used ls -la to review permissions and chmod to remove unauthorized access from files and directories. These changes improved security by ensuring that only authorized users could access sensitive project resources. 


