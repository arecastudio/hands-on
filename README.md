# Description
A repo to put anything I got from this book https://www.pdfdrive.com/penetration-testing-a-hands-on-introduction-to-hacking-d36645450.html
## Practical
Some command to keep in mind
### Grep Command
```
tux@x250:~/Documents/projects/hands-on/mydir$ cat myfile
1 Derbycon September
2 Shmoocon January
3 Brucon September
4 Blackhat July
5 Bsides *
6 HackerHalted October
7 Hackcon April
tux@x250:~/Documents/projects/hands-on/mydir$ grep September myfile
1 Derbycon September
3 Brucon September
```
### Cut Command
```
tux@x250:~/Documents/projects/hands-on/mydir$ grep September myfile|cut -d " " -f 2
Derbycon
Brucon

```
### Sed Command
```
tux@x250:~/Documents/projects/hands-on/mydir$ sed 's/Blackhat/Defcon/g' myfile 
1 Derbycon September
2 Shmoocon January
3 Brucon September
4 Defcon July
5 Bsides *
6 HackerHalted October
7 Hackcon April
tux@x250:~/Documents/projects/hands-on/mydir$ cat myfile |grep -i blackhat
4 Blackhat July
tux@x250:~/Documents/projects/hands-on/mydir$ sed -i 's/Blackhat/Defcon/g' myfile 
tux@x250:~/Documents/projects/hands-on/mydir$ cat myfile |grep -i july
4 Defcon July

```
