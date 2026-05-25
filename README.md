# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="473" height="160" alt="image" src="https://github.com/user-attachments/assets/9b577234-2b8d-4ead-adee-aa9d25c91871" />




cat < file2
## OUTPUT
<img width="473" height="179" alt="image" src="https://github.com/user-attachments/assets/fe4c5e56-f43e-4b16-83d1-b85cb0c9bb52" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="497" height="72" alt="image" src="https://github.com/user-attachments/assets/5147dace-bab9-418b-b0ee-b71a2f1f351b" />


comm file1 file2
 ## OUTPUT
<img width="539" height="277" alt="image" src="https://github.com/user-attachments/assets/7eb0d048-b214-4726-ba7f-ed189ad37c5e" />


 
diff file1 file2
## OUTPUT
<img width="539" height="246" alt="image" src="https://github.com/user-attachments/assets/1a6d487b-bea7-4468-858c-7fc01547b9e6" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
<img width="556" height="74" alt="image" src="https://github.com/user-attachments/assets/947dcb50-605e-4afb-b42f-bf9606d0466d" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="551" height="119" alt="image" src="https://github.com/user-attachments/assets/6196c55c-6cf7-42db-b79c-2088c09c5c19" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="551" height="119" alt="image" src="https://github.com/user-attachments/assets/f1344814-34d6-459b-909a-955221e6a538" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep hello newfile 
## OUTPUT
<img width="557" height="65" alt="image" src="https://github.com/user-attachments/assets/8e9a89a0-4891-423b-b548-e235924479c5" />


grep -v hello newfile 
## OUTPUT
<img width="557" height="65" alt="image" src="https://github.com/user-attachments/assets/3dfd49d5-c04a-41ea-8dfe-d461c3b933cc" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="698" height="88" alt="image" src="https://github.com/user-attachments/assets/10c97ab5-3518-41aa-848e-c41678abf65c" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="685" height="66" alt="image" src="https://github.com/user-attachments/assets/8504f310-f4a7-427e-b88a-783fb9b857a0" />




grep -R ubuntu /etc
## OUTPUT
<img width="698" height="243" alt="image" src="https://github.com/user-attachments/assets/9d7db37a-afb3-4418-bcd8-e50529c5f5ad" />



grep -w -n world newfile   
## OUTPUT
<img width="717" height="83" alt="image" src="https://github.com/user-attachments/assets/92b5b7d9-2d1f-4d9b-8d14-fb6c5e99dc95" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="710" height="79" alt="image" src="https://github.com/user-attachments/assets/59b61014-4f68-4fab-b635-e4cda5eaa41d" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="704" height="68" alt="image" src="https://github.com/user-attachments/assets/dafff366-77d6-45d2-9da6-a8529d518a70" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="710" height="79" alt="image" src="https://github.com/user-attachments/assets/e134e4aa-7c66-45f5-87c8-164b0368843b" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="710" height="61" alt="image" src="https://github.com/user-attachments/assets/d579fda6-d22e-44e0-b540-aacb71c2be2a" />



egrep '(world$)' newfile 
## OUTPUT
<img width="709" height="77" alt="image" src="https://github.com/user-attachments/assets/991e57af-1919-417a-8978-25ccc9caf250" />



egrep '(World$)' newfile 
## OUTPUT
<img width="695" height="64" alt="image" src="https://github.com/user-attachments/assets/6fe73aec-e785-46b4-8790-0425cca4aaf2" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="701" height="104" alt="image" src="https://github.com/user-attachments/assets/b52e2186-2ef6-4ab7-97f7-25d6b36b0660" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="697" height="60" alt="image" src="https://github.com/user-attachments/assets/26618ea8-ec55-4fd4-8503-00793c329ea5" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="697" height="60" alt="image" src="https://github.com/user-attachments/assets/eb162b0c-9242-4b06-9b42-475e8df6edb9" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="697" height="60" alt="image" src="https://github.com/user-attachments/assets/e6c945f0-23ec-4347-a599-68cd63fad7e1" />


egrep l{2} newfile
## OUTPUT
<img width="706" height="82" alt="image" src="https://github.com/user-attachments/assets/8adacccc-c8ed-4555-b647-aa3c83fed274" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="704" height="98" alt="image" src="https://github.com/user-attachments/assets/f6dfbe7f-f2b7-481f-bf30-ff203342f972" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="889" height="44" alt="image" src="https://github.com/user-attachments/assets/c26a12e1-cf34-44c9-aea9-e85bd02ed0bb" />



sed -n -e '$p' file23
## OUTPUT
<img width="889" height="44" alt="image" src="https://github.com/user-attachments/assets/43341a1e-c93b-4fbd-b356-26b84d5602ba" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="940" height="169" alt="image" src="https://github.com/user-attachments/assets/084cc369-da35-47e4-a83c-9aecee210f55" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="950" height="169" alt="image" src="https://github.com/user-attachments/assets/50438a75-2ad9-4b2e-9ea7-eb97ac131b82" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="950" height="169" alt="image" src="https://github.com/user-attachments/assets/8e25b5f2-c3be-475b-a9dc-21df57de1511" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="952" height="117" alt="image" src="https://github.com/user-attachments/assets/99d8e484-2c54-4a68-8050-c3953edea811" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="951" height="78" alt="image" src="https://github.com/user-attachments/assets/39487f5b-36ca-4822-9254-aa1879996914" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="969" height="62" alt="image" src="https://github.com/user-attachments/assets/88cc8e93-7ca5-44fd-8954-73d80a4d7395" />




seq 10 
## OUTPUT
<img width="754" height="198" alt="image" src="https://github.com/user-attachments/assets/9ca910e4-eb52-4b55-8f40-1525a0c32566" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="888" height="79" alt="image" src="https://github.com/user-attachments/assets/15d27871-a559-4543-908f-358e2e63cb25" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="892" height="76" alt="image" src="https://github.com/user-attachments/assets/a41a2f24-04fa-4707-bb08-9699d30a322b" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="891" height="94" alt="image" src="https://github.com/user-attachments/assets/0b02f753-abb7-4a0b-a205-625562ee5b86" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="890" height="82" alt="image" src="https://github.com/user-attachments/assets/26bd70ba-58db-4c94-8973-c087fecf11e1" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="910" height="80" alt="image" src="https://github.com/user-attachments/assets/a321f999-c257-40d9-8ee4-3ff4a565904e" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="954" height="76" alt="image" src="https://github.com/user-attachments/assets/0840a451-f6a5-4f35-ba64-b2d4704f232f" />



sed -n '2,4{s/$/*/;p}' file23
<img width="954" height="76" alt="image" src="https://github.com/user-attachments/assets/4194c92f-bcbb-4a29-b458-7fbaababf222" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="796" height="112" alt="image" src="https://github.com/user-attachments/assets/a2882915-2710-4f0d-9d63-2859d4ce3b76" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
<img width="796" height="112" alt="image" src="https://github.com/user-attachments/assets/47721fbe-34b4-4cc4-8c67-14162257b725" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1006" height="169" alt="image" src="https://github.com/user-attachments/assets/3ef657dd-7627-46d7-8faa-656bc1721d6b" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="858" height="74" alt="image" src="https://github.com/user-attachments/assets/5e25572c-354b-4d8e-a3c7-fa84829e241b" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1055" height="76" alt="image" src="https://github.com/user-attachments/assets/bc419e57-d153-416f-a296-fe1a52ad1f7e" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="892" height="363" alt="image" src="https://github.com/user-attachments/assets/ba467ae0-37ff-4349-9b08-dd65e52b922a" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="967" height="1001" alt="image" src="https://github.com/user-attachments/assets/d03fcfd6-fa74-493a-b5db-ebeaec7e34ca" />


tar -xvf backup.tar
## OUTPUT
<img width="967" height="1001" alt="image" src="https://github.com/user-attachments/assets/986f97c8-6c10-4ae1-9a1b-f24547ee0486" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="861" height="44" alt="image" src="https://github.com/user-attachments/assets/fd430dd0-03b9-442b-b7c1-48197a4fcc80" />

gunzip backup.tar.gz
## OUTPUT
<img width="1662" height="279" alt="image" src="https://github.com/user-attachments/assets/7bdc2d64-7841-418c-ae23-1093f607f28c" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1110" height="134" alt="image" src="https://github.com/user-attachments/assets/5e86a85b-2350-407b-9da4-9e8676c4a0f2" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="942" height="161" alt="image" src="https://github.com/user-attachments/assets/495843a7-ec05-4294-b412-41711c939ce1" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="901" height="507" alt="image" src="https://github.com/user-attachments/assets/c5a06cd5-27b7-4561-bc00-e1c9410dc3dc" />

 
ls file1
## OUTPUT
<img width="773" height="35" alt="image" src="https://github.com/user-attachments/assets/8f8b6c85-3572-4ed0-962c-bc05b07a414d" />

echo $?
## OUTPUT
<img width="773" height="35" alt="image" src="https://github.com/user-attachments/assets/a0e03702-46f5-42fc-9883-07800cc0d565" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="769" height="185" alt="image" src="https://github.com/user-attachments/assets/d57a182f-8a68-46bc-8a12-4e881c437ee8" />

abcd
 
echo $?
 ## OUTPUT
<img width="769" height="185" alt="image" src="https://github.com/user-attachments/assets/0ac4890a-47d1-4ec1-a468-436dbae1b4de" />


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
## OUTPUT
<img width="840" height="186" alt="image" src="https://github.com/user-attachments/assets/e09b9b43-558a-4277-a867-c9ccca4ca8c7" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="804" height="45" alt="image" src="https://github.com/user-attachments/assets/3952e412-d8ed-4832-9274-3453b44dbfed" />


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
<img width="824" height="47" alt="image" src="https://github.com/user-attachments/assets/2e230057-2b01-4f40-8b13-1a89333dbad2" />

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
<img width="820" height="82" alt="image" src="https://github.com/user-attachments/assets/23a90a82-bd78-478a-a6f2-256a17eea82a" />



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
<img width="792" height="62" alt="image" src="https://github.com/user-attachments/assets/bcea3244-3bad-48b1-88f4-cb1e137b123c" />

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT
<img width="820" height="82" alt="image" src="https://github.com/user-attachments/assets/f40c47ba-18cb-4c3a-a6c4-b12ce2ee8a8d" />

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
<img width="823" height="44" alt="image" src="https://github.com/user-attachments/assets/30edcb48-38ff-458e-a304-9a594307a1c5" />


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="823" height="44" alt="image" src="https://github.com/user-attachments/assets/2281b94b-da8e-4bd1-af59-9040be42c5b9" />

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 ## OUTPUT
 <img width="823" height="44" alt="image" src="https://github.com/user-attachments/assets/d02ed11b-b0bf-4cf5-b001-c254314108a4" />

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 ## OUTPUT
 <img width="829" height="203" alt="image" src="https://github.com/user-attachments/assets/15103d5f-dd03-4323-a405-1aaf5ffabf61" />

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
## OUTPUT
 <img width="829" height="100" alt="image" src="https://github.com/user-attachments/assets/8d10445a-46a2-42a5-970a-b60c882d27fc" />

 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 ## OUTPUT
 <img width="789" height="128" alt="image" src="https://github.com/user-attachments/assets/1218fa4a-242f-414c-93f4-de884c0453b6" />

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 ## OUTPUT
 <img width="784" height="80" alt="image" src="https://github.com/user-attachments/assets/2280b392-0bae-4c66-8a36-562c1667deb7" />

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 ## OUT[UT
 <img width="787" height="152" alt="image" src="https://github.com/user-attachments/assets/80b44d9e-be37-4df5-8fc6-967e619d4420" />

cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh


cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam




cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
<img width="816" height="113" alt="image" src="https://github.com/user-attachments/assets/1ef1e03d-df41-4ae2-ba2d-8c91628fd29c" />

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
<img width="823" height="115" alt="image" src="https://github.com/user-attachments/assets/998fb45d-8346-46bb-9f8f-c0cc73e43250" />

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<img width="833" height="236" alt="image" src="https://github.com/user-attachments/assets/2bc56252-f1fb-4c55-af62-d40511c74574" />

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 ## OUTPUT
 <img width="825" height="79" alt="image" src="https://github.com/user-attachments/assets/c9f23574-1aa9-4c50-9a63-13027846225a" />


cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="837" height="113" alt="image" src="https://github.com/user-attachments/assets/abe0cdd6-fd97-40f6-8123-715d858f714c" />

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
<img width="799" height="57" alt="image" src="https://github.com/user-attachments/assets/7647bdf2-2397-4d3d-8f73-d4a29697aa53" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="808" height="57" alt="image" src="https://github.com/user-attachments/assets/c333ce9f-ec33-40f2-ae36-b7c9053855a7" />



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
<img width="807" height="37" alt="image" src="https://github.com/user-attachments/assets/92bde299-818f-4469-a813-42ecd7c00359" />

 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh


$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
<img width="869" height="72" alt="image" src="https://github.com/user-attachments/assets/fbfe72d0-10cd-463d-b49b-5eea515c0303" />

 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 <img width="895" height="255" alt="image" src="https://github.com/user-attachments/assets/8dba1eca-bbec-42be-a123-57080549c6e9" />

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
<img width="839" height="72" alt="image" src="https://github.com/user-attachments/assets/c567c3ae-f84e-4c5e-bee9-8a249ef097b3" />


# RESULT:
The Commands are executed successfully.
