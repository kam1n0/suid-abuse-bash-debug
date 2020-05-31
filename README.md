# suid-abuse-bash-debug
*Credit to Tib3rius* | https://tryhackme.com/room/linuxprivesc

Note: This will work on Bash versions <= 4.4

* This exploit leverages how Bash, when in debugging mode, uses the environment variagble PS4 to display an extra prompt for debugging statements.

1) Find all the SUID/SGID executables on the Linux machine

link suid

2) 	Run the /usr/local/bin/suid-env2 executable with bash debugging enabled and the PS4 variable set to an embedded command which creates a SUID verion of /bin/bash:

link debug

3) 	Run the /tmp/rootbash executable with -p to gain a shell running root privileges:

link root
