## Lab 02

- Name:
- Email

Instructions for this lab: https://pattonsgirl.github.io/CEG2350/Labs/Lab02/Instructions.html

## Part 1 Answers

Full / absolute path to your private key file:C:\Users\yoelt> .\ceg2350-vm.pem 

Command to SSH to AWS instance:
```
[ssh -i .\ceg2350-vm.pem ubuntu@54.86.10.26]
```

## Part 2 Answers

1. `chmod u+r bubbles.txt`
    - Means: Allow the user to read bubles.txt.
    - Assessment:-rw-rw-r-- 1 ubuntu ubuntu 0 Sep  9 01:17 bubbles.txt
2. `chmod u=rw,g-w,o-x banana.cabana`
    - Means: User is only allowed to read and write, remove group writing permission and remove other execution permission from banana.cabana.
    - Assessment:-rw-r--r-- 1 ubuntu ubuntu 0 Sep  9 01:26 banana.cabana
3. `chmod a=w snow.md`
    - Means: All users permission is set to only write in snow.md.
    - Assessment:--w--w--w- 1 ubuntu ubuntu 0 Sep  9 01:38 snow.md
4. `chmod 751 program`
    - Means: Allow the owner to read,write and excute. while group can only write and excute, but others can only excute.
    - Assessment:-rwxr-x--x 1 ubuntu ubuntu 0 Sep  9 01:45 program
5. `chmod -R ug+w share`
    - Means: All file in share should have user and group writing permission.
    - Assessment:ubuntu@ceg2350-sandbox:~/share$ ls -l
total 4
drwxrwxr-x 2 ubuntu ubuntu 4096 Sep  9 02:02 share
---x--x--x 1 ubuntu ubuntu    0 Sep  9 02:03 snow
ubuntu@ceg2350-sandbox:~/share$ cd ..
ubuntu@ceg2350-sandbox:~$ chmod -R ug+w share
ubuntu@ceg2350-sandbox:~$ ls -l share
total 4
drwxrwxr-x 2 ubuntu ubuntu 4096 Sep  9 02:02 share
--wx-wx--x 1 ubuntu ubuntu    0 Sep  9 02:03 snow

## Part 3 Answers

1. Command to create new user: sudo adduser
2. Path to new user's home directory: /home/bob
3. Evaluate if `ubuntu` can add files to new user's home directory:No, permission denied
4. Command to switch to new user:su bob
5. Command(s) to go to new user's home directory:cd ~
6. Evaluate if new user can add files to user's home directory:
7. Command to return to `ubuntu` user:su ubuntu
8. Command to return to `ubuntu` home directory: exit

## Part 4 Answers

1. Command(s) to create group named `squad` and add members: sudo addgroup squad 
2. Command(s) to add `ubuntu` & user to group `squad`: sudo usermod -aG squad ubuntu
3. Command(s) to allow `squad` to view the `ubuntu` user's home directory contents: 
4. Command(s) to modify `share` to have group ownership of `squad`:sudo chgrp squad /home/ubuntu/share
5. Describe your tests and commands with the user account:The user account seems like almost everything is like 'ubuntu'. I ran touch test.txt and vim test.txt
6. Describe the full set of permissions / settings that enable the user to make edits:being in a groupship with ubuntu allows bob to edit

## Part 5 Answers

For each, write the command used or answer the question posed.

1. Command(s) to make file using `sudo`: sudo touch /path/to/filename
2. Command(s) to make file with `root`: su -c 'echo "your content here" > /path/to/file'
3. Describe / compare ownership and permissions of files: You have no restriction To create file using sudo, but root is like a different user so you need to have password to access.
4. Which account can do what actions? (Type Y or N in columns)

Contents inside of `share`
| Account   | Can View  | Can Edit  | Can Change Permissions    |
| ---       | ---       | ---       | ---                       |
| `root`    | Y          |  N         | Y                          |
| `ubuntu`  | Y          |   Y        |  N                         |
| `BOB`     | Y          |  Y         |  N                         |

`madewithsudo.txt`
| Account   | Can View  | Can Edit  | Can Change Permissions    |
| ---       | ---       | ---       | ---                       |
| `root`    |  Y         | Y          | Y                          |
| `ubuntu`  |  Y         | N          | N                          |
| `BOB`     |  Y         | N          | N                          |

5. Command(s) to modify permissions:chmod 777 dark.txt or chmod u=rwx,g=-w,o=-r darx.txt
6. How to give user account `sudo`:sudo usermod -aG sudo bob

## Citations

To add citations, provide the site and a summary of what it assisted you with.  If generative AI was used, include which generative AI system was used and what prompt(s) you fed it.
