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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/6074b166-eeef-4273-ab98-8aebbeecca54)



cat < file2
## OUTPUT
![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/fe4dc55f-132d-4233-8a40-5fd686e9e7a8)


# Comparing Files
cmp file1 file2
## OUTPUT

 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/54cfd349-b50b-43a6-820f-3a5ae29b62b3)

comm file1 file2
 ## OUTPUT

 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/3c077ecb-862e-4e8a-8006-b4cb8edbb7ea)

diff file1 file2
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/d7775f74-8bca-474a-a301-9ec64c64b43e)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/275426e7-d787-46b5-a7fb-091e7667c4a4)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/31c4d517-de6a-493a-ad5c-0bc154f6afa6)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/6f45acb2-ca37-4d0e-ad14-643ade7733ae)

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
![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/e608ea32-9e7b-49ff-a97a-573ff840fd20)



grep hello newfile 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/8809b36a-e8d3-420c-bd4f-5daf467b7b42)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/6f7958ed-8d28-4114-ae9b-739b814ec1ea)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/5ffb5f16-52c7-40ff-aaac-e0a4e3a86c8d)



cat newfile | grep -i -c "hello"
## OUTPUT


![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/1f44eb93-095d-43a1-801b-73cbe48ae3a3)


grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/4a7457c9-884e-4760-83fc-bc733da87cb2)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/6c81a8bd-a850-4d96-a7b9-f1ebb066a13b)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/c8685716-7d69-4fe7-bfca-d173428a0eda)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/159ed1a4-9f78-40e4-a934-3e34449fd73d)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/c88e8c13-89b3-4f37-9f4f-18e346f54290)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/e436592f-2f92-4350-a923-d1f57338587f)


egrep '(world$)' newfile 
## OUTPUT


![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/d5a10bab-c71f-4b8d-a46c-bfb932c144de)

egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/1021fbab-ebd8-40c4-bc0e-83e58e95c50b)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/2eba6c4e-7b9b-4e4b-85d4-7b5707310001)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/01031890-406a-4a15-a161-227d3150886b)


egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/3d54d88f-9c3b-4922-ae13-668a6e87ad4d)

egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/b05b3c25-a633-4062-b2b9-e027537206c1)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/c5d99b88-e64b-4800-8c8e-9e886e842e7d)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/d55cf3c6-e11e-4b78-b380-5ee284695043)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/946a0dbd-6ccf-40ab-acfb-6ac5d3d05bb1)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/1363c4eb-9875-43ff-9a09-0a0dc0a941cc)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/d7424351-7556-44bb-a520-5afb932467bd)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/529f505b-eb93-4ba8-930d-825016809a14)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/96ae16c2-2788-43d4-850f-0d5653b971ac)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/a6937362-9a2f-4139-9a73-60ad96b9705d)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/c2aae15b-31ab-4d26-9c2b-7abccaea3f91)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/96f74877-b640-4825-a455-e370efb90802)


seq 10 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/9b7fd0f5-f824-42dc-9608-0ebb7b78c437)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/e7a80d8a-dfe5-4cb1-83b3-1aa1d5e07f2b)


seq 10 | sed -n '2,~4p'
## OUTPUT


![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/cca424eb-a80f-4fd7-a70c-b68d8873ac21)

seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/4cd67c5c-86d8-4cc0-b628-05f1053753a1)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/70010b38-157b-4c8e-97b3-7f9e03f45928)

seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/927da45c-5863-4b7a-bf06-7182f221de3e)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/870f5add-0142-44a2-a3d0-f398a4406f82)


sed -n '2,4{s/$/*/;p}' file23


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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/67f1bece-b68b-4236-a015-9a73d8b09464)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/a3a61428-c6bd-49a0-9431-96e7d359346f)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/17d53caf-3d94-4862-96c7-4836c3054539)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/0a5abb2f-e114-4d8f-a923-b39f54a3b36a)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/2e6aa826-963a-44ca-9cb0-4eeea7c265dd)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/3618354c-269c-46c7-bba1-f26d3b496ba2)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/a14fa8ac-85f2-4b5b-83bb-5f60c2aa0d63)

tar -xvf backup.tar
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/49e8da45-912d-4846-b7f3-b61e3c11632b)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/6bef5552-c1b0-4839-93ff-6dfd89b8552f)

gunzip backup.tar.gz
## OUTPUT

 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/b49b3a2e-0758-4d8d-8659-6624c12a9828)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/d3c29a1b-088c-40ef-a991-046da48594bc)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/77f0f240-70c0-4308-a46c-70820d3c0edd)

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

 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/419ed64c-0498-43ec-9b40-887a5b446bfc)

ls file1
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/420e43d9-0fd3-40da-84e1-5290fd9ed07c)

echo $?
## OUTPUT 

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/aa3eb251-e14b-427f-950b-e4fe8313cce9)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/5ee3038a-4d21-4af6-8999-b65616a1cb0c)

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
![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/6a9f653e-2382-4978-986e-684bdc3d0633)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/462ecd18-e5d3-4546-b1be-475d02a2ebc8)


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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/a74db4fe-189c-4bdb-835f-aab81e35a0a7)

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
![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/b8a69c38-c8ac-4771-98ce-ec15907d1f4b)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/784bbdae-d6a4-4f4a-a2a0-cc4b21332f97)

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
![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/04806cd0-9f8c-4049-a195-00b39d314a3a)

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
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/22e14e60-59c3-432f-a198-edf6d382e766)

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
 
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/0668505b-df7a-4a59-8ea7-d57e9ea5cd56)

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
 
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/b999e72e-8e9c-4bc5-ab91-8be04e7ac763)

 
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
 
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/1d1766ef-3b28-4a3d-b1e2-0e0545ff170c)

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
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/b93f4d38-53f7-4e04-b6dc-29fb6a4f1559)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/a9991697-41f3-4732-8704-ad72713c369e)


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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/e09bb656-cb25-420d-8817-96c478ad0f61)

$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/9b1f1984-4b4f-49dd-ab0a-f9284180bd07)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/57b93f86-7486-4112-9d4a-3cdd9c5d3a65)

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
![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/0d7eb6f5-2846-4397-8a1d-8d6a29482ec0)

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

 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/c3de0511-52d5-4acf-a236-7df06747ffb0)

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
![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/fb91d8b5-bfc3-47f9-8d1b-3e54ee540f57)

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
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/a7bb60d7-7f62-49d3-b76d-5a77eeedf106)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/d146a238-549b-49e4-8f48-50540fc7b0c7)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/e598f62e-34ca-48f5-92ad-fb77ed8f2a14)


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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/c44b0fff-f156-4c01-9701-989ac0185a4e)

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

## OUTPUT
$ ./argshift.sh 1 2 3
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/08bf3f5c-d6aa-4a90-85c9-6aa3966a97eb)

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
$ ./argshift.sh 1 2 3
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/92ae1fc1-cb6d-48f6-b545-a5a496a7a791)

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
 ./argshift.sh 1 2 3
 
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/e6cb073f-22c2-4187-b290-70beaa71122c)

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
 ![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/a54140db-68e6-4bed-a693-a5e1cb9abf0b)

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

![image](https://github.com/Sandeepzxi/OS-Linux-commands-Shell-script/assets/168530813/75d2e9f2-e240-45db-90db-6695aca35931)

# RESULT:
The Commands are executed successfully.
