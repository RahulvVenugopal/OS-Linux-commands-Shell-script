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
![Screenshot 2025-03-05 225811](https://github.com/user-attachments/assets/b2b6a7b8-d1e4-4d17-85b3-c470154a77eb)



cat < file2
## OUTPUT
![Screenshot 2025-03-08 164108](https://github.com/user-attachments/assets/8ac0cb66-8c5e-487a-a49f-cac231111aec)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2025-03-08 164401](https://github.com/user-attachments/assets/f55fbaa3-040a-4972-94f6-e0c76c5e655e)

 
comm file1 file2
 ## OUTPUT
![Screenshot 2025-03-08 164448](https://github.com/user-attachments/assets/8ce782c1-2e13-43d2-974d-0c61b04d75bb)

 
diff file1 file2
## OUTPUT
![Screenshot 2025-03-05 230010](https://github.com/user-attachments/assets/19969688-b33d-4b2b-937c-d882aa66cff6)


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
![image](https://github.com/user-attachments/assets/5f41ea43-d03a-4791-8b91-99ac6c9a2d60)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/071429e9-233a-4e78-ad25-cb53f91c6f81)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/752f05a8-47b4-4bbe-83ff-747b3b1ea1cc)


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
![image](https://github.com/user-attachments/assets/689cd9b4-e367-4631-a05e-4397719cf886)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/abfc9f2e-3bd2-449f-9e4f-7b5d5e937ee5)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/96faf734-a89e-4409-ae38-42fbf69fe05e)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/3b76d4ed-9e6c-4a18-9d32-fac55d1478bc)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/df2e1705-5604-436e-98f0-29184ee007a4)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/accef376-1df1-440f-85d7-250a5558a883)
![image](https://github.com/user-attachments/assets/a4e32da0-e26c-4c70-b2ce-6ff0caa33de8)
![image](https://github.com/user-attachments/assets/8b92ebfd-c121-4933-8cee-21245471651c)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/4bb95176-20d0-4e39-a198-e6a3d769ead5)


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
Hello rahul
hello rahul
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/79e11b3c-8415-4996-8e1d-be871ccb07a7)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/87b07066-20e0-438b-ac5f-ae3d90a77715)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/445458f6-9c8d-43cf-b4ac-43e3de24eab2)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/34ed0aea-5801-40bf-882e-eff68ad5ec10)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/0d8c66f5-76f4-4038-b874-54fd1dcc312a)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4be0f295-cac9-4f5f-a83c-f5609e59c519)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4a0de6cd-ab67-420f-9b1b-b3107ab9dfcf)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/0d799f45-5740-412e-aded-843c8b24ecf4)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ed1aa8ec-6363-4edb-a7d5-b7570e9e38d6)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/bdb48c63-d4d5-477a-8348-befc45e9a714)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/395d5944-7b1e-40a9-a81e-e7d7bbeecd8e)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/9a5b4cc0-8a17-40a5-955e-644b6b472aba)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Rahul |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1db39811-c64e-40a6-a9d2-c1fd2c045d69)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/20742652-cbd9-4285-bd7c-fbf1afb50391)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/207fc00d-0733-49d6-a371-2665ced9e91d)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/4b6da0d5-45f1-4350-babe-85fbef82839a)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/e7c26246-a441-4fdc-8147-7dc0d9ffd738)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ac16d1a3-3f38-4a3f-8cd1-5c8126df94a7)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/228ec64b-5159-4753-8fc7-922e3b25c763)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/161c0d25-f0a6-47b6-acc1-e24ec0fcdc13)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/9fe68d4d-ecad-43d9-abfe-bfaefc9c020b)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/e735dcaf-1be3-48ad-9c16-75e5ebc8e90c)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/d8a8cf05-e332-41db-b9ac-bde6cb9e2807)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/2c4d768f-80c0-431d-ba54-16e28c4e0d79)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/55d71a6c-9930-43ad-bfd6-9242827ee4e1)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/5cd996da-2126-4d2f-9def-6e9cf33c8063)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/351c4e26-4bf8-425e-9cc9-59490e5d6396)



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
![image](https://github.com/user-attachments/assets/1367e605-a6bb-44e3-a6e1-482b8f226e89)


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
![Screenshot 2025-03-08 175609](https://github.com/user-attachments/assets/b214c75c-8530-4a58-a505-2f0581e82f0e)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2025-03-08 180412](https://github.com/user-attachments/assets/cf4d5b2e-cc1d-48ba-836d-930fb4fe7c43)


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
 ![image](https://github.com/user-attachments/assets/b357c86b-f059-428b-a99f-a4f635101751)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/7615aa5b-5021-41a5-b299-4ce6769ff1d7)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot 2025-03-06 091311](https://github.com/user-attachments/assets/826eb00d-3b0a-476b-97c6-d18c8b006c52)
![Screenshot 2025-03-06 091336](https://github.com/user-attachments/assets/eea69801-6458-48e7-bc3f-dbac4d173b33)
![Screenshot 2025-03-06 091357](https://github.com/user-attachments/assets/de5de35d-e9f4-40cb-9fbf-c3b3c594abd8)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2025-03-06 091948](https://github.com/user-attachments/assets/263e0e3d-9e7f-466f-8635-093e3914a3ea)
![Screenshot 2025-03-06 092006](https://github.com/user-attachments/assets/16f8b73b-2647-4fe4-9931-98205433ff94)


tar -xvf backup.tar
## OUTPUT
![Screenshot 2025-03-06 092206](https://github.com/user-attachments/assets/70dfefeb-0159-4752-aca2-e1f83e3c8158)
![Screenshot 2025-03-06 092227](https://github.com/user-attachments/assets/76a5ed7b-9bb1-4af7-9b1d-d5fb80727f7e)
![Screenshot 2025-03-06 092249](https://github.com/user-attachments/assets/bf5cdd66-0be1-41e2-95a4-b7dd19f3e867)

gzip backup.tar

ls .gz
 
gunzip backup.tar.gz
## OUTPUT
![Screenshot 2025-03-06 092436](https://github.com/user-attachments/assets/4a195078-75c6-4917-a79f-9c1c5fd69ee4)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/00bf2040-a7c3-4137-90a6-357e4c1a25ef)


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2025-03-08 185601](https://github.com/user-attachments/assets/262066bc-87d9-427b-91d0-077ee31022e6)


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
![image](https://github.com/user-attachments/assets/85b06876-dbe3-4502-b2ce-0778dda757f7)

 
ls file1
## OUTPUT
![Screenshot 2025-03-08 190939](https://github.com/user-attachments/assets/069fa46f-5ec3-4730-964e-430856ffec0b)


echo $?
## OUTPUT 
![Screenshot 2025-03-08 191155](https://github.com/user-attachments/assets/d43cc091-8595-4e5e-b00d-4e884a6b2960)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![Screenshot 2025-03-07 202502](https://github.com/user-attachments/assets/217d02dc-3fd6-4577-a7bc-b13ed55e35b8)
 
abcd
 
echo $?
 ## OUTPUT
![Screenshot 2025-03-08 191155](https://github.com/user-attachments/assets/451bf75f-860d-4b38-9f1a-915e27760444)


 
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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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


# RESULT:
The Commands are executed successfully.
