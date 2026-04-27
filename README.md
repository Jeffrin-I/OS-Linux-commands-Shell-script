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
<img width="621" height="163" alt="image" src="https://github.com/user-attachments/assets/9be1e8eb-10e8-4e66-8008-5bd63073e092" />



cat < file2
## OUTPUT
<img width="631" height="179" alt="image" src="https://github.com/user-attachments/assets/be339f93-a7e9-448b-b031-e881b5753e64" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="626" height="76" alt="image" src="https://github.com/user-attachments/assets/9f13156c-c412-4927-b7fa-1129a4d37ba8" />

 
comm file1 file2
 ## OUTPUT
 <img width="638" height="231" alt="image" src="https://github.com/user-attachments/assets/06e6ba8a-1829-42fa-a67b-8ab429dd0f62" />


 
diff file1 file2
## OUTPUT
<img width="644" height="276" alt="image" src="https://github.com/user-attachments/assets/40d2ae23-2c5a-4335-89ed-92ffb489321c" />


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
<img width="623" height="100" alt="image" src="https://github.com/user-attachments/assets/1c6769ac-725c-49c2-82e8-45c631630de9" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="630" height="133" alt="image" src="https://github.com/user-attachments/assets/1978a49a-09fe-4eba-9a3b-bf3c0923347b" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="667" height="127" alt="image" src="https://github.com/user-attachments/assets/c6768e72-cf51-4501-928b-d59c9bd5a6f6" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="618" height="78" alt="image" src="https://github.com/user-attachments/assets/fc5d60e2-0f84-4e14-bdb7-ec84910f29c1" />



grep hello newfile 
## OUTPUT
<img width="635" height="78" alt="image" src="https://github.com/user-attachments/assets/714e2e39-b2d7-479b-8e3b-0f49fae9f4cb" />





grep -v hello newfile 
## OUTPUT
<img width="625" height="73" alt="image" src="https://github.com/user-attachments/assets/8024bd40-35d5-4392-b25f-0df856ab6d2f" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="658" height="99" alt="image" src="https://github.com/user-attachments/assets/dcfc31f0-49a0-481a-9749-efd862862541" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="626" height="75" alt="image" src="https://github.com/user-attachments/assets/f826b469-d12f-4436-99c2-4508f7b57318" />




grep -R ubuntu /etc
## OUTPUT
<img width="1433" height="697" alt="image" src="https://github.com/user-attachments/assets/dd70cbef-be94-4b66-b517-e74e035ed7c7" />
<img width="1053" height="571" alt="image" src="https://github.com/user-attachments/assets/aeec37b0-11ea-46f8-9674-19437f5a9948" />



grep -w -n world newfile   
## OUTPUT
<img width="668" height="100" alt="image" src="https://github.com/user-attachments/assets/92b1d084-14b6-4ec0-bbd9-80d3d66f8335" />



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
<img width="635" height="106" alt="image" src="https://github.com/user-attachments/assets/0678a83f-e7a3-4239-9c6a-ee40e38b9e57" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="627" height="103" alt="image" src="https://github.com/user-attachments/assets/a22f61f7-cbed-4162-ac5c-4e62ab7265d6" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="641" height="103" alt="image" src="https://github.com/user-attachments/assets/4a4d3f06-b6f6-44c2-baa3-f0583e23255a" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="642" height="82" alt="image" src="https://github.com/user-attachments/assets/07bd3c1f-36bf-491f-a680-528881252619" />



egrep '(world$)' newfile 
## OUTPUT
<img width="654" height="100" alt="image" src="https://github.com/user-attachments/assets/e2a9594f-873f-40d1-8725-f1fa7ac9e8eb" />



egrep '(World$)' newfile 
## OUTPUT
<img width="664" height="82" alt="image" src="https://github.com/user-attachments/assets/9732cf57-3d9e-4344-9106-9caba2d08c17" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="652" height="134" alt="image" src="https://github.com/user-attachments/assets/1ef26e21-23c2-4ca6-95e5-6a8fedcc4777" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="652" height="77" alt="image" src="https://github.com/user-attachments/assets/be563fd9-b113-434a-9238-c5c6ddb1e393" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="641" height="80" alt="image" src="https://github.com/user-attachments/assets/5aea0e64-7319-44a6-9dc4-1ae712af8d8a" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="679" height="81" alt="image" src="https://github.com/user-attachments/assets/f45be2c6-79b8-44d7-b9df-4fd932649408" />


egrep l{2} newfile
## OUTPUT
<img width="642" height="104" alt="image" src="https://github.com/user-attachments/assets/107a8297-f24a-4129-addf-aa0ee83a6b4b" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="661" height="129" alt="image" src="https://github.com/user-attachments/assets/19a9d58b-c823-495b-b101-53527a91d353" />


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
<img width="685" height="79" alt="image" src="https://github.com/user-attachments/assets/5f14b7bb-82c4-46de-95d3-65c3c39f19ad" />



sed -n -e '$p' file23
## OUTPUT
<img width="662" height="75" alt="image" src="https://github.com/user-attachments/assets/765dcd7d-f581-45aa-919b-4b14bc8f461a" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="670" height="252" alt="image" src="https://github.com/user-attachments/assets/c9235f46-3058-48f6-918a-d7ad46dd0fc9" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="680" height="248" alt="image" src="https://github.com/user-attachments/assets/c76b47c2-8858-42f1-9ea6-bcc9ef6319a0" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="652" height="258" alt="image" src="https://github.com/user-attachments/assets/db31921b-3399-4272-b893-80e8eecb9354" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="649" height="178" alt="image" src="https://github.com/user-attachments/assets/be20ba7a-bd34-4a45-82b2-107669ceb89e" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="656" height="133" alt="image" src="https://github.com/user-attachments/assets/b7517604-355c-4b29-8b01-33482ab02f00" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="682" height="102" alt="image" src="https://github.com/user-attachments/assets/4df04df8-7da6-4094-94e6-6b8bfe3a5fc5" />



seq 10 
## OUTPUT
<img width="674" height="302" alt="image" src="https://github.com/user-attachments/assets/7f72b8ea-80ea-461e-b3dc-e786ad5fd0d1" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="640" height="128" alt="image" src="https://github.com/user-attachments/assets/5c6f0c6b-24c4-4099-b6ec-b1fe19fc3eae" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="765" height="131" alt="image" src="https://github.com/user-attachments/assets/5cdb75a6-b876-4c78-95ca-76ec0702f3d8" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="701" height="148" alt="image" src="https://github.com/user-attachments/assets/639544ff-4785-4018-88ad-f40ab7940596" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="687" height="125" alt="image" src="https://github.com/user-attachments/assets/ff66a32c-bd4f-41a0-8bb5-c6db1fdd0d25" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="704" height="122" alt="image" src="https://github.com/user-attachments/assets/f4823305-7d24-4ec5-8b2b-c8562528d20d" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="704" height="127" alt="image" src="https://github.com/user-attachments/assets/1a83376f-e9ac-469a-ba1d-54dc7fc4d14e" />



sed -n '2,4{s/$/*/;p}' file23
<img width="664" height="122" alt="image" src="https://github.com/user-attachments/assets/f5e28741-d082-4e66-89fc-62cdcc5b3870" />


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
<img width="773" height="181" alt="image" src="https://github.com/user-attachments/assets/60458b0d-fd70-4450-bf91-a3299022d335" />


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
<img width="663" height="176" alt="image" src="https://github.com/user-attachments/assets/ab05db97-6e60-4c68-9981-6cce67bfa72b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="692" height="249" alt="image" src="https://github.com/user-attachments/assets/38c0df7b-ca3a-422d-9576-d0f26c5fc3ca" />

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

<img width="651" height="123" alt="image" src="https://github.com/user-attachments/assets/44b13524-f94d-4ee3-b2f2-6a8b35373883" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="643" height="123" alt="image" src="https://github.com/user-attachments/assets/91d1b2af-ae5b-4759-b841-106d4cbc2522" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="639" height="309" alt="image" src="https://github.com/user-attachments/assets/39971694-0653-481c-a827-2bf2e145995a" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="788" height="305" alt="image" src="https://github.com/user-attachments/assets/0d8c48d3-817b-416c-ab32-e41c6dbe7dab" />



tar -xvf backup.tar
## OUTPUT
<img width="793" height="333" alt="image" src="https://github.com/user-attachments/assets/339e7bb9-9327-4b25-9bae-85e413b5976c" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="763" height="125" alt="image" src="https://github.com/user-attachments/assets/35a3cd1d-dd6a-4045-b697-418205ed3773" />

 
gunzip backup.tar.gz
## OUTPUT
<img width="732" height="55" alt="image" src="https://github.com/user-attachments/assets/cd738051-4f4d-423d-9e3d-40d381d6b402" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="643" height="146" alt="image" src="https://github.com/user-attachments/assets/0d1e31de-bc94-451c-a44c-a99877825343" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="617" height="124" alt="image" src="https://github.com/user-attachments/assets/62a7c29a-6192-460b-a89b-42e4b1835efd" />


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
<img width="684" height="456" alt="image" src="https://github.com/user-attachments/assets/8131ced9-9480-44cf-a096-6b8114cbc6c9" />

 
ls file1
## OUTPUT
<img width="655" height="73" alt="image" src="https://github.com/user-attachments/assets/06af8273-7079-4c49-a6dc-684ce10e86f9" />

echo $?
## OUTPUT 
<img width="636" height="75" alt="image" src="https://github.com/user-attachments/assets/9b6cdf91-7d4a-4002-98f2-8a5fe4b41511" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="676" height="150" alt="image" src="https://github.com/user-attachments/assets/1924817f-013b-41f8-832e-9ab1328ec9b4" />

abcd
 
echo $?
 ## OUTPUT
 <img width="659" height="149" alt="image" src="https://github.com/user-attachments/assets/2ebdfdd9-7163-4f72-89d6-3264e2180d2f" />



 
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
##OUTPUT
<img width="618" height="275" alt="image" src="https://github.com/user-attachments/assets/b1098eb4-7a3b-4160-aabf-d43e8d0f8dc6" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="608" height="150" alt="image" src="https://github.com/user-attachments/assets/80cdac27-16af-47fa-a0b7-748ab38927b6" />


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
<img width="629" height="226" alt="image" src="https://github.com/user-attachments/assets/d0f71973-9141-4a71-aed3-9176ac0eb220" />
<img width="629" height="99" alt="image" src="https://github.com/user-attachments/assets/29058751-8446-483c-8e16-12a83f3eee21" />



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
<img width="636" height="146" alt="image" src="https://github.com/user-attachments/assets/b5d1cbba-ed3a-46dc-93dd-d480a5a17317" />



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
##OUTPUT
<img width="664" height="169" alt="image" src="https://github.com/user-attachments/assets/3f9e224c-e3e5-404b-bd29-d48e15f847f0" />

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
##OUTPUT
<img width="657" height="209" alt="image" src="https://github.com/user-attachments/assets/bf2c18e1-f52c-4013-887b-c6627c88a43b" />


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
<img width="649" height="150" alt="image" src="https://github.com/user-attachments/assets/131e2778-047d-4f0a-80bc-e18cd6f03add" />


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
<img width="665" height="151" alt="image" src="https://github.com/user-attachments/assets/f3a3fb84-2c10-4def-8a8f-1e6e4e27021d" />

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

## OUTPUT
<img width="622" height="300" alt="image" src="https://github.com/user-attachments/assets/6f718277-35d4-4af6-8e43-350c566a7c10" />

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

## OUTPUT
<img width="616" height="230" alt="image" src="https://github.com/user-attachments/assets/4b1ade39-f2ff-4ad1-80cc-286b71d5252f" />


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
<img width="627" height="228" alt="image" src="https://github.com/user-attachments/assets/33c270dc-1be6-4981-a0ec-18d894dab473" />

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
<img width="589" height="175" alt="image" src="https://github.com/user-attachments/assets/c584d83e-376f-4c7e-929c-8c3fb8aa09cb" />


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
<img width="615" height="399" alt="image" src="https://github.com/user-attachments/assets/67ce1347-cfbf-4fb8-a331-57a98df1b817" />

 
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
## OUTPUT
<img width="668" height="319" alt="image" src="https://github.com/user-attachments/assets/08a96fdb-ca67-4796-8725-92af000d08fc" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
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
 <img width="721" height="124" alt="image" src="https://github.com/user-attachments/assets/ca20e842-ac69-4650-86a5-0ece62fa03c2" />

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
<img width="632" height="148" alt="image" src="https://github.com/user-attachments/assets/87c6bb34-f003-4209-b496-918c63d86c2d" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="664" height="59" alt="image" src="https://github.com/user-attachments/assets/3f4fa30f-14dd-41e8-9fb2-db9cb963292a" />




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
 ./funcex.sh 

 
 ./funcex.sh 1 2

 <img width="678" height="555" alt="image" src="https://github.com/user-attachments/assets/918c67cb-f4c5-43d3-9cb6-15ac9857a76e" />

cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 <img width="647" height="180" alt="image" src="https://github.com/user-attachments/assets/405db7e2-4c12-4264-845f-7b1be6670663" />

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
## OUTPUT
<img width="628" height="46" alt="image" src="https://github.com/user-attachments/assets/9e6a5e9a-c3b7-4ccf-904a-a782d8a0d8f4" />

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
<img width="622" height="398" alt="image" src="https://github.com/user-attachments/assets/de911c74-149a-46e9-aaad-92c9a86ce157" />

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
 <img width="644" height="378" alt="image" src="https://github.com/user-attachments/assets/7ec725bc-fa67-4422-a7ac-0ba200f60fe1" />

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
<img width="704" height="605" alt="image" src="https://github.com/user-attachments/assets/427c63c9-d26f-4ef7-8043-b6079791ab8c" />



# RESULT:
The Commands are executed successfully.
