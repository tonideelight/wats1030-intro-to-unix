# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges
// SEE BELOW FOR RESPONSES
### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:*
* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*
* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*
* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*
* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*
* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
* Press the up arrow on your keyboard. *What just happened?*
* Press the up arrow a few more times. *What do you see?*
* Run the `history` command. *What do you see?*

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
* How long has your system been running? Use `uptime` to see, and *paste the result here:*
* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*
* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*


Navigating the Filesystem
Get an idea of where you are in the operating system. Use the pwd command to find your "path to working directory"--your current location in the filesystem of your devbox. Paste the output of the pwd command here: /mnt/c/Users/tonid/development
Discover more about this filesystem. Use ls (the "list" command)to see what is in this directory. What directories and files do you see when you run ls?
Desktop - Shortcut.lnk  wats1010-basic-markup    wats1010-product-page        wats3020-mad-libs
tonideelight.github.io  wats1010-css             wats1030-intro-to-unix       wats3020-sandwich-machine
wats1010-adv-markup     wats1010-embedded-media  wats3010-intro-to-bootstrap
You can use options to modify how a command runs. Try using ls -alh to see the contents of your current directory. How are the results different when you use the -alh options? Items are listed vertically as opposed to horizontally – “drwxrwxrwx 2 root root” is also listed with –alh
The man ("manual") command tells you more about how any given command works. (WARNING: CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/). Run manto see instructions about how to use man. Then use man to learn what the a, l, and h options mean when used with the ls command. Write down what those options do?   
-a, --all
do not ignore entries starting with .
-h, --human-readable
with -l, print sizes in human readable format (e.g., 1K 234M 2G)
 -l     use a long listing format

Commands can also take arguments, which are usually the names of files or locations that you want the command to work with. Try running ls / to see what files are in the root directory of the filesystem. What files and directories do you see listed?
acct  boot   data  etc   init  lib64       media  opt   root  sbin  sys  usr
bin   cache  dev   home  lib   lost+found  mnt    proc  run   srv   tmp  var
A Unix filesystem has a few special shortcuts to refer to specific locations. / indicates the root of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the cd ("change directory") command to move to the root directory. (Hint: Use man to look up the cd command if you have any issues) Then run pwd and paste the output here: /home/toni
Another special shortcut in Unix is the ~ location. This indicates the user root directory, meaning the top-most directory in the hierarchy that comes below your user account. Use cd to move to ~. Run pwd and paste the response here: /home/toni
Change directory into the challenge_files directory. Use ls to find only the files with a .demo pattern. How many files do you find? 2015_special_stuff.demo  cloaked-wookie.demo  scooter-double-mamba.demo
Use the cd command to move "up" one directory. Where are you in the filesystem now? toni@TONI-LAPTOP:~/development/wats1030-intro-to-unix$
Press the up arrow on your keyboard. What just happened? Cd .. populated 
Press the up arrow a few more times. What do you see? Previous steps are populating
Run the history command. What do you see? A list of the commands I’ve used since starting the assignment
Observing the System
Discover what account you are logged into using the whoami command. What username are you currently using? toni
Discover who else is on your system with the who command. Are any other users using your system? If so, list them here: no other users
How long has your system been running? Use uptime to see, and paste the result here: 17:37:40 up  2:21,  0 users,  load average: 0.52, 0.58, 0.59
Run ps aux and review the results. (Hint: Use man to learn more about the ps command and options.) How do you interpret what you see here? This displays what programs are being run on my command line
Run top and review the results. (Hint: You may need to use ctrl-c to get out of this app.) How do you interpret what you see here?  This displays what programs are being run on my command line but with more details (sleeping, stopped, memory used/free)
Finding and Viewing Files
Make sure you are in the challenge_files directory. Use the * wildcard to find all the files that have the word "credit" in the filename. How many files did you find? credit_cards2.txt  credit_cards.txt
Use the more command to view one of the credit_cards files you just discovered. (Hint: Type q to quit viewing the file. Press the spacebar to page down. Use your keyboard arrows to move up/down.) What is the date in the file you have viewed? Jul 2
Use the find command to search for files more effectively. Search the sub-directories under challenge_files to find the location of the file named modi_laboriosam.txt. Where is that file located? ./tmp/modi_laboriosam.txt
Use the grep command to search for text within a file. Use grep on all the .user files in challenge_files to find which files contain "WA" (the abbreviation for Washington state). How many files did you find?
Britt-Erdman.user:O'Harachester, WA 37261
Lissie-Strosin.user:Jewessfurt, WA 00816-7241
Use the -r option of grep to recursively find the text "Waldo" hidden in a file somewhere under the challenge_filesdirectory. Paste the result showing the file and line where the word "Waldo" shows up.
serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia.
Pipes and Connecting Commands
Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running ls > filestxt. Notice that the file files.txt was created. View that file using more. What do you see in the files.txt file? The list of file names from challenge files folder
Notice that if you run ls -alh in the challenge_files directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running ls -alh | more. Describe what you see when you run ls -alh | more.  The list of challenge files are listed from top to bottom, as opposed to just seeing the bottom without the | more command
Earlier, when you viewed the list of active processes on your devbox using ps aux, the list was probably really long. You can make this list more manageable by using the pipe (|) to filter the results of ps using grep. Run ps aux | grep <your_username> to see what processes are running for your specific user. Paste the list of processes that reference your username here:
toni         2  0.0  0.0      0     0 ?        Ss    2434   0:02 /bin/bash
toni       142  0.0  0.0      0     0 ?        R     2434   0:00 ps aux
toni       143  0.0  0.0      0     0 ?        S     2434   0:00 grep --color=auto

