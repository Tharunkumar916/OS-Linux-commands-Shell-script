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

<img width="814" height="84" alt="Screenshot 2025-10-25 051028" src="https://github.com/user-attachments/assets/e9170b68-4ef0-4a56-9b79-6ec0b25282d4" />


cat < file2
## OUTPUT

<img width="814" height="101" alt="Screenshot 2025-10-25 051115" src="https://github.com/user-attachments/assets/a7e5fed5-545d-4561-8a69-237f1a01e2a8" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="815" height="32" alt="Screenshot 2025-10-25 051143" src="https://github.com/user-attachments/assets/3035ed48-1302-4a40-8072-e1410da2eed7" />

 
comm file1 file2
 ## OUTPUT

<img width="812" height="155" alt="Screenshot 2025-10-25 051205" src="https://github.com/user-attachments/assets/45cb8370-8fd6-4ba5-85fa-6a1d43bde1cf" />

 
diff file1 file2
## OUTPUT

<img width="816" height="167" alt="Screenshot 2025-10-25 051231" src="https://github.com/user-attachments/assets/c8a88440-d33d-48a1-87fb-32a845962188" />


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

<img width="813" height="53" alt="Screenshot 2025-10-25 051300" src="https://github.com/user-attachments/assets/6da333fa-ab71-4d10-b689-445b311eb192" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="814" height="66" alt="Screenshot 2025-10-25 051315" src="https://github.com/user-attachments/assets/3d565d8c-07ef-4098-8883-d3eeb7fed006" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="813" height="67" alt="Screenshot 2025-10-25 051330" src="https://github.com/user-attachments/assets/1c3c0105-862c-45cd-8a53-074821032f0f" />


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

<img width="812" height="29" alt="Screenshot 2025-10-25 051512" src="https://github.com/user-attachments/assets/49b0a297-dda6-4019-b923-638e18b49ab1" />


grep hello newfile 
## OUTPUT

<img width="814" height="29" alt="Screenshot 2025-10-25 051522" src="https://github.com/user-attachments/assets/bbe86879-fe81-4d40-a898-6f71ff254a71" />



grep -v hello newfile 
## OUTPUT

<img width="813" height="30" alt="Screenshot 2025-10-25 051535" src="https://github.com/user-attachments/assets/76d15cbe-ffff-4b65-ae2c-7c4b256a00e4" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="814" height="47" alt="Screenshot 2025-10-25 051553" src="https://github.com/user-attachments/assets/40309873-210e-489c-a165-ec978c48893d" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="814" height="29" alt="Screenshot 2025-10-25 051606" src="https://github.com/user-attachments/assets/465b31fb-fbc3-4a11-9ece-4497babdf641" />



grep -R ubuntu /etc
## OUTPUT


<img width="815" height="196" alt="Screenshot 2025-10-25 051618" src="https://github.com/user-attachments/assets/8119d13d-4093-491a-acdc-4b9f7895654d" />


grep -w -n world newfile   
## OUTPUT


<img width="813" height="53" alt="Screenshot 2025-10-25 051629" src="https://github.com/user-attachments/assets/c58c06ee-5dce-486f-8427-5373c14a0c0b" />


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

<img width="813" height="43" alt="Screenshot 2025-10-25 051822" src="https://github.com/user-attachments/assets/7197db8c-80be-4b96-a42c-722da4503496" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="813" height="42" alt="Screenshot 2025-10-25 051833" src="https://github.com/user-attachments/assets/888a03be-ae3a-493c-9241-210566bf7003" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="816" height="44" alt="Screenshot 2025-10-25 051841" src="https://github.com/user-attachments/assets/b77b2863-bb90-43de-8ddb-ba2b29c5ddee" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="814" height="30" alt="Screenshot 2025-10-25 051853" src="https://github.com/user-attachments/assets/fa4924b6-fcb3-4209-adde-dc581179b198" />


egrep '(world$)' newfile 
## OUTPUT

<img width="822" height="44" alt="Screenshot 2025-10-25 051915" src="https://github.com/user-attachments/assets/92ca7dad-69e4-4ab5-908d-338f50950694" />


egrep '(World$)' newfile 
## OUTPUT

<img width="809" height="31" alt="Screenshot 2025-10-25 051939" src="https://github.com/user-attachments/assets/869171ea-9818-4e82-b396-149c9a05d2a9" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="808" height="64" alt="Screenshot 2025-10-25 051952" src="https://github.com/user-attachments/assets/2bb9a2c9-cbdb-4f2b-9301-02992cf21bb1" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="816" height="35" alt="Screenshot 2025-10-25 052005" src="https://github.com/user-attachments/assets/04f23c31-77d3-405c-89f5-b17237ff5af0" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="815" height="35" alt="Screenshot 2025-10-25 052015" src="https://github.com/user-attachments/assets/494f9e44-e5d6-497a-96d9-65073682af6f" />


egrep 'Linux.*World' newfile 
## OUTPUT


<img width="815" height="26" alt="Screenshot 2025-10-25 052037" src="https://github.com/user-attachments/assets/c3ac25b1-72d7-4557-9c0d-bf9bb1ae6c38" />


egrep l{2} newfile
## OUTPUT

<img width="816" height="47" alt="Screenshot 2025-10-25 052046" src="https://github.com/user-attachments/assets/4c6e05f1-9fc0-466d-94e1-9aed35adc55a" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="815" height="60" alt="Screenshot 2025-10-25 052057" src="https://github.com/user-attachments/assets/6e18ff62-14da-4e7c-a4d5-ad2cf0a79108" />



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

<img width="812" height="27" alt="Screenshot 2025-10-25 052355" src="https://github.com/user-attachments/assets/8bdddc7c-6b7e-418a-8ccf-96c1553dc8bf" />


sed -n -e '$p' file23
## OUTPUT

<img width="811" height="29" alt="Screenshot 2025-10-25 052407" src="https://github.com/user-attachments/assets/a9bc0d58-7494-4b15-a603-7382c5a5686e" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="814" height="139" alt="Screenshot 2025-10-25 052416" src="https://github.com/user-attachments/assets/66a2ef58-9277-4d48-96c6-351a2916ebfd" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="812" height="136" alt="Screenshot 2025-10-25 052425" src="https://github.com/user-attachments/assets/737e73eb-2857-4c6f-ada1-aea519324270" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="817" height="141" alt="Screenshot 2025-10-25 052434" src="https://github.com/user-attachments/assets/ea5933e5-69a7-4907-8803-1661ab811180" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="815" height="93" alt="Screenshot 2025-10-25 052518" src="https://github.com/user-attachments/assets/d14ff0c0-cad8-41f3-82a5-61769711d2eb" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="811" height="64" alt="Screenshot 2025-10-25 052542" src="https://github.com/user-attachments/assets/4a9e6d6f-9b59-4433-aae1-40f98dcf8bec" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="814" height="50" alt="Screenshot 2025-10-25 052553" src="https://github.com/user-attachments/assets/3d60c5e5-15c7-4d42-b3a6-60bd52c7ca92" />


seq 10 
## OUTPUT

<img width="809" height="171" alt="Screenshot 2025-10-25 052605" src="https://github.com/user-attachments/assets/42130a69-e12e-4c77-ab90-1c0ab29dd5ab" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="817" height="61" alt="Screenshot 2025-10-25 052618" src="https://github.com/user-attachments/assets/22c56fdd-73ef-4925-ac85-7c6cb0b8805d" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="817" height="31" alt="Screenshot 2025-10-25 052628" src="https://github.com/user-attachments/assets/20f2c832-2a36-49aa-bb1d-9d0249bd628c" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="818" height="32" alt="Screenshot 2025-10-25 052638" src="https://github.com/user-attachments/assets/29953bdb-c800-4411-afbe-745e6ab76341" />


seq 2 | sed '2i hello'
## OUTPUT


<img width="814" height="30" alt="Screenshot 2025-10-25 052647" src="https://github.com/user-attachments/assets/847e4bde-1965-4f78-9e5d-e90795b11b35" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="814" height="31" alt="Screenshot 2025-10-25 052658" src="https://github.com/user-attachments/assets/27e6d6fb-edf5-47a4-8891-8aa8c3b5db29" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="815" height="30" alt="Screenshot 2025-10-25 052707" src="https://github.com/user-attachments/assets/2b0f7f22-b904-485b-adeb-653f4ce31c98" />


sed -n '2,4{s/$/*/;p}' file23

<img width="816" height="33" alt="Screenshot 2025-10-25 052719" src="https://github.com/user-attachments/assets/425b9d49-eefa-404f-9c75-cdff70150c00" />



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

<img width="812" height="94" alt="Screenshot 2025-10-25 053256" src="https://github.com/user-attachments/assets/40631dcc-cb48-44f2-ad58-ba3b67c413ae" />



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

<img width="810" height="92" alt="Screenshot 2025-10-25 053322" src="https://github.com/user-attachments/assets/fae2232d-2fa9-4f68-aeca-6290bc1ec97a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="818" height="131" alt="Screenshot 2025-10-25 053332" src="https://github.com/user-attachments/assets/f5fccbfe-e1c8-4fb3-b13a-74603c079983" />


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

<img width="820" height="61" alt="Screenshot 2025-10-25 053740" src="https://github.com/user-attachments/assets/3751e96f-c258-4111-a798-703ee7b3ba6b" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="817" height="61" alt="image" src="https://github.com/user-attachments/assets/d6d0b75a-deb8-46e1-9892-1ebd183732f5" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="817" height="867" alt="image" src="https://github.com/user-attachments/assets/cfd268d8-d652-4193-8f83-ae3dee306e35" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="807" height="852" alt="image" src="https://github.com/user-attachments/assets/413f72d3-cff2-4853-a324-9adb816684fb" />


tar -xvf backup.tar
## OUTPUT

<img width="811" height="865" alt="image" src="https://github.com/user-attachments/assets/5be4a858-6d6f-4605-ad2c-0c3ad5174b0c" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="816" height="29" alt="Screenshot 2025-10-25 054231" src="https://github.com/user-attachments/assets/3c95b771-639e-4cd0-b2f4-465600c7da78" />

 
gunzip backup.tar.gz
## OUTPUT


<img width="815" height="55" alt="Screenshot 2025-10-25 054254" src="https://github.com/user-attachments/assets/60471d81-0163-4f72-85b9-c00d39bb5d22" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


<img width="815" height="97" alt="Screenshot 2025-10-25 054419" src="https://github.com/user-attachments/assets/5a09c22a-9026-42dd-bee2-64190aa81a22" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="812" height="62" alt="Screenshot 2025-10-25 054440" src="https://github.com/user-attachments/assets/0a3ba8a7-755d-4de9-b2d9-f499c9939366" />



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


<img width="816" height="230" alt="Screenshot 2025-10-25 054514" src="https://github.com/user-attachments/assets/a365472a-7632-478e-839d-672fa91ca8ff" />

 
ls file1
## OUTPUT


<img width="814" height="30" alt="Screenshot 2025-10-25 054547" src="https://github.com/user-attachments/assets/6817dab5-a442-4a29-8e16-25a956b303d3" />

echo $?
## OUTPUT 

<img width="815" height="31" alt="Screenshot 2025-10-25 054557" src="https://github.com/user-attachments/assets/336ce249-8b39-49d1-983f-366959d819b8" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 


 <img width="810" height="31" alt="Screenshot 2025-10-25 054658" src="https://github.com/user-attachments/assets/1c8ab200-5aa1-43f8-ab54-458b87437552" />

abcd
 
echo $?
 ## OUTPUT

<img width="813" height="31" alt="Screenshot 2025-10-25 054710" src="https://github.com/user-attachments/assets/c0c820f7-cca4-499b-935b-07670155a8be" />

 
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

<img width="816" height="177" alt="Screenshot 2025-10-25 054804" src="https://github.com/user-attachments/assets/de6dc28d-bdd8-464f-9d22-3194efe33b6c" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="807" height="22" alt="image" src="https://github.com/user-attachments/assets/b15c40a7-d03d-4067-ae3c-27b7fca0b63f" />



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

<img width="815" height="24" alt="Screenshot 2025-10-25 054915" src="https://github.com/user-attachments/assets/a6b816e0-427b-458b-8a77-a00851b1d99b" />


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

<img width="815" height="56" alt="Screenshot 2025-10-25 054949" src="https://github.com/user-attachments/assets/e21163d4-93ae-4dbd-a908-c5052bd1e5ec" />


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

<img width="812" height="52" alt="image" src="https://github.com/user-attachments/assets/b5e099d2-75e2-4dde-9e37-e3c8e5ba968a" />


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

<img width="816" height="40" alt="Screenshot 2025-10-25 055206" src="https://github.com/user-attachments/assets/a09b0362-6656-4f7a-ba72-e8affccf1752" />


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

<img width="815" height="37" alt="Screenshot 2025-10-25 055237" src="https://github.com/user-attachments/assets/1f32593e-d334-46be-980a-017595cbd518" />


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

<img width="815" height="42" alt="Screenshot 2025-10-25 055300" src="https://github.com/user-attachments/assets/58ef5ed9-35b7-4904-aff2-b356350bdfd6" />

 
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

 <img width="817" height="151" alt="image" src="https://github.com/user-attachments/assets/44ea1573-4c7a-49f8-a690-49f747d1731b" />

 
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
 
 <img width="813" height="70" alt="image" src="https://github.com/user-attachments/assets/124aef48-9f8b-4568-b889-683ae56aa120" />

 
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

 <img width="816" height="109" alt="Screenshot 2025-10-25 055456" src="https://github.com/user-attachments/assets/2df6a8c1-17da-4edd-a658-2c6afd6aaaae" />

 
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

<img width="815" height="67" alt="Screenshot 2025-10-25 055525" src="https://github.com/user-attachments/assets/489c5523-8cea-4fcd-8e18-b2292a792d42" />

 
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

<img width="819" height="67" alt="Screenshot 2025-10-25 055552" src="https://github.com/user-attachments/assets/5e839ae4-7e72-4996-90c8-9f2bf937c7bb" />

 
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

<img width="812" height="111" alt="image" src="https://github.com/user-attachments/assets/be48e05c-34d0-4175-add4-35eed90c209b" />

 
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

<img width="812" height="107" alt="image" src="https://github.com/user-attachments/assets/d7603860-ded4-467e-bc80-595cea383cda" />


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

<img width="814" height="207" alt="Screenshot 2025-10-25 060231" src="https://github.com/user-attachments/assets/47d9d41f-61c5-42b0-a6c5-0ffda4e89b8b" />


cat forctype.sh 

<img width="817" height="96" alt="Screenshot 2025-10-25 060314" src="https://github.com/user-attachments/assets/e5417f9b-5d03-42f0-a67a-35ff2ba2a260" />



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

<img width="813" height="97" alt="image" src="https://github.com/user-attachments/assets/fffedf1a-efea-48d8-869a-02b1622c72c8" />


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

<img width="815" height="193" alt="Screenshot 2025-10-25 060436" src="https://github.com/user-attachments/assets/c8dbb118-428d-493e-b64a-7bf5b068d7b2" />


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

<img width="817" height="54" alt="Screenshot 2025-10-25 060501" src="https://github.com/user-attachments/assets/a0cc5203-89c8-47eb-a8b6-f7dcf564f713" />

 
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

<img width="811" height="96" alt="image" src="https://github.com/user-attachments/assets/64e6c990-2e94-4cc5-8008-2e4c9efb383a" />


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

<img width="811" height="97" alt="image" src="https://github.com/user-attachments/assets/63f76d02-8200-4e3f-831a-0fc857f1b6ce" />

 
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

<img width="815" height="57" alt="image" src="https://github.com/user-attachments/assets/40616ea6-1f45-4575-9ba8-c57f19833552" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="808" height="57" alt="Screenshot 2025-10-25 060808" src="https://github.com/user-attachments/assets/2f60c449-eb5a-433f-89a4-be877391e029" />



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

<img width="816" height="42" alt="Screenshot 2025-10-25 060852" src="https://github.com/user-attachments/assets/0f44646f-5a44-4bec-b515-960fb4bccd18" />

 
 ./funcex.sh
 
<img width="811" height="26" alt="Screenshot 2025-10-25 060903" src="https://github.com/user-attachments/assets/070d5f08-2d56-44dd-93a9-a978f57051dc" />

 
 
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

<img width="816" height="66" alt="Screenshot 2025-10-25 060952" src="https://github.com/user-attachments/assets/dc57e5f6-e323-4c69-bd06-6bb2a6581809" />


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
## OUTPUT

<img width="816" height="72" alt="image" src="https://github.com/user-attachments/assets/f5262963-0249-4776-98a9-fd68d57ddf90" />



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


<img width="815" height="216" alt="Screenshot 2025-10-25 061103" src="https://github.com/user-attachments/assets/3bacba84-cb93-471d-a49d-e27f7d976204" />



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

<img width="813" height="194" alt="Screenshot 2025-10-25 061130" src="https://github.com/user-attachments/assets/e0bfe5c2-6c09-4bb4-8693-1b410068e202" />


 
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

<img width="813" height="70" alt="Screenshot 2025-10-25 061157" src="https://github.com/user-attachments/assets/dd07d7c6-7db1-47fe-b3fe-ad9b3d922f5f" />


# RESULT:
The Commands are executed successfully.
