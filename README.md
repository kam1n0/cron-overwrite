# cron-overwrite

*Credit to Tib3rius* | https://tryhackme.com/room/linuxprivesc

Given a cron job that runs a script with root privileges and is world-writeable.
Overwrite the script with with a bash script that connects back to the attacking machine with a reverse shell with root permissions.

1. View the contents of the system-wide crontab:

![Image of crontab](https://github.com/kam1n0/cron-overwrite/blob/master/tmp_upload/etc_cron.png)

2. Locate the full path of the overwrite.sh file:

![Image of overwrite](https://github.com/kam1n0/cron-overwrite/blob/master/tmp_upload/overwrite_sh.png)

3. Check the file permissions of overwrite.sh:

* Note that the file is world-writeable

![Image of ls_l](https://github.com/kam1n0/cron-overwrite/blob/master/tmp_upload/ls_l.png)

4. Replace the contents of the overwrite.sh file with the following (IP of attacking machine):

![Image of bin_bash](https://github.com/kam1n0/cron-overwrite/blob/master/tmp_upload/bin_bash.png)

5. Get reverse shell with root privilegs

![Image of nc_nlvp](https://github.com/kam1n0/cron-overwrite/blob/master/tmp_upload/nc_nlvp.png)
