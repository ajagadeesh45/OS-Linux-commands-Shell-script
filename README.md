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
![image](https://github.com/user-attachments/assets/943b5568-714e-4efc-b536-36fe225978f1)

cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/8d77d46e-1043-4401-bfa6-2c4fa82e2eda)

# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/c3f59e29-e094-40df-9ed9-e723b4cb1682)

comm file1 file2
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/a7d2d607-5345-4d25-b7b7-436a7ec1edf6)

diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/fe542402-7acf-4cf9-b0ef-e64e02fdb046)



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
![image](https://github.com/user-attachments/assets/28092a27-fc62-475a-acd8-252d4618251b)





cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/e4e87fc7-6404-4225-9033-1bf1d0b6561b)




cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/36a0a3ef-1319-46d6-af6d-a8f92206d3e2)



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
![image](https://github.com/user-attachments/assets/aacfff64-f8b3-4e9c-b927-5383c8810c92)




grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4a56f013-49af-4c9d-b34e-e32a1020e5ad)





grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/68d50ad0-4a5c-4b01-a77f-57d0d7a5b896)




cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/5ba6e85e-ca91-499c-adb0-53fe93e6ba97)





cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/8144c6db-b64c-4ba2-b9a8-8112c25b2b37)





grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/d6dad3ae-5e42-44c4-84c9-ce218a765106)
![image](https://github.com/user-attachments/assets/191c1166-de3c-443a-8aeb-a66c6a908312)
![image](https://github.com/user-attachments/assets/f6b14f53-a67f-4427-80b1-5c0bda205db1)
![image](https://github.com/user-attachments/assets/7af4af58-2f70-40f8-a03e-ae35784158b4)






grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/d44bef1d-fed9-4e6c-b624-51bfd0463409)



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
![image](https://github.com/user-attachments/assets/438240b2-6a1c-4f2f-b1b6-cbf704bf8195)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/c704e6b6-3c27-416d-9190-67349403a2e8)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d759d8ac-2867-4e2c-83ca-3aa6d7cea215)





egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/046128cf-2e99-4c2d-99ee-6a8274ba5fc1)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/31f2b02f-5f90-4c21-a895-9083882a5dfd)




egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/31f2b02f-5f90-4c21-a895-9083882a5dfd)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/7c0e9384-e0de-446c-a536-84f4eb1aff29)




egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/197070f4-407e-4754-8441-b45d418bfad7)




egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/9627ac4b-0fbe-4aff-a1b6-5b043d3af2e2)



egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/86403292-396a-41c5-a97a-9c454411a3a0)



egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/7af87896-8b13-4098-83f6-008955f2f24f)




egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/01476292-8c1e-4695-979c-ce3b261aa47e)



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
![image](https://github.com/user-attachments/assets/69e1c1f6-07a5-4323-9b6f-0ff3e5e2b2bf)




sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/858f3048-497a-40d8-a453-cf6d1c0503bb)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/37ee8e99-0d4a-4272-ab09-60b2a7cdea1d)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/eb6e184f-8e72-42f3-b54f-09abb5edfc0f)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1260ebc6-a161-4603-8777-d99dd9b05a54)




sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/c2e4bc11-550e-4dac-aabd-c2577957358c)




sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8666196b-03d7-4e65-829e-a53f70a73450)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f6828383-f6ab-4dee-8904-208739450f47)




seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/e47169b9-2bf2-47dd-8783-d4624e171fab)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/28e9946f-c079-4cb6-a11d-551abda06050)



seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/d6042f69-440f-4177-99aa-dc2b140763c4)


seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/d48caaba-6546-4d7f-877d-2b02502d21eb)




seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/04be6ff8-7247-4554-99be-3fdd955d576d)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/e3ffc841-b69f-4e7d-83e1-ec4281f229e3)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/49832dd8-e387-470f-9641-72143bfdfabc)



sed -n '2,4{s/$/*/;p}' file23
## output 
![image](https://github.com/user-attachments/assets/2ac1f262-e6d0-483f-950a-91331a690960)



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
![image](https://github.com/user-attachments/assets/33af0a4a-cf80-4a4c-9750-b17c164a4940)



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
![image](https://github.com/user-attachments/assets/abee4baf-5074-4fb1-ba13-6da078172622)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/aed03c3a-e780-41ca-89d2-d18a7c2510c9)


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

![image](https://github.com/user-attachments/assets/f7ccdd23-a9c7-465f-8b33-34b4583ad0fb)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/87a4245c-3087-496a-99d9-59b08aea63d8)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/6bc61cd8-d566-45dc-ada6-01f9791ea117)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/9a85801a-610a-4def-ae60-bcfd3dcab088)



tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/1b7dea59-c551-4684-a163-a17897a3a875)


gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/user-attachments/assets/e89d26a1-1987-4307-bd59-c05ebf8adef1)

 
gunzip backup.tar.gz
## OUTPUT

 ![image](https://github.com/user-attachments/assets/827270ce-7b13-4068-b785-2b7a0f33d3f9)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/1095df2b-9340-49ca-92be-cec7e8463ac3)



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
![image](https://github.com/user-attachments/assets/7ab29808-1efd-4a93-b35a-37835b8dcc03)


 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/677cbcb1-ca8d-4380-a3ab-ad564fd88184)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/eeba0dd6-6008-4965-a9e1-68e18ab08571)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/eeba0dd6-6008-4965-a9e1-68e18ab08571)

 
abcd
 
echo $?
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/d87ea27b-273f-4776-81c5-4186b8f6b022)



 
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
![image](https://github.com/user-attachments/assets/744f74ad-5e16-409d-b5cf-58dbc23dc1a0)




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/ccd6aa9b-7e21-47fa-b796-7dacb7ec7765)



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
![image](https://github.com/user-attachments/assets/dbd457e4-624f-4eb4-8279-0007c31b6557)


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
![image](https://github.com/user-attachments/assets/eddba616-0492-4c52-88ba-7865e031dc0d)




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
![image](https://github.com/user-attachments/assets/82b1053f-ce06-4ab4-ac54-9b38394c47da)


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
![image](https://github.com/user-attachments/assets/0d7e1005-19f9-449e-9a97-0ceb68604612)


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
![image](https://github.com/user-attachments/assets/13696c28-e12a-48e8-ba4f-6035cd7e8c07)



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
![image](https://github.com/user-attachments/assets/065e3430-70c9-424c-9b3d-cfb815753a6d)


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
 # output
 ![image](https://github.com/user-attachments/assets/d30cd934-45bf-4f95-98de-58eee7d7393e)

 
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
# output
![image](https://github.com/user-attachments/assets/ee59e4fe-d813-4913-aebc-744236d36033)

 
 
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
$ ./untiltest.sh 
# output
![image](https://github.com/user-attachments/assets/7719e41c-cb58-4165-9550-c0491f57f909)

 
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
 
 
cat>forin2.sh 
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
# output
![image](https://github.com/user-attachments/assets/8f0ad277-36a6-431e-be6d-00b0a4b50a45)

 
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
# output
![image](https://github.com/user-attachments/assets/e54d2ab7-c65c-4520-8813-3ccab5b0f23a)

 
cat>forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh
$ ./forin3.sh 
# output
![image](https://github.com/user-attachments/assets/5951e24e-dfc9-4b1c-886c-37c54c95d30e)

 
cat>forin1.sh 
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
![image](https://github.com/user-attachments/assets/abaa3a58-0413-45f4-a915-9492a16e8320)

cat>forinfile.sh 
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
![image](https://github.com/user-attachments/assets/b557e2dd-3a9f-4637-a80d-0d6a6c0b8c53)



cat>forctype.sh 
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
![image](https://github.com/user-attachments/assets/6f67e8b6-ca80-45eb-996d-b4bea34f321d)


cat>forctype1.sh 
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
![image](https://github.com/user-attachments/assets/09bb157b-de41-49c6-8499-c161856d2cf0)

cat>fornested1.sh 
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
 ![image](https://github.com/user-attachments/assets/cbdd84e3-b5d7-4ebc-978e-17aeed7ff133)


 
cat>forbreak.sh 
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
![image](https://github.com/user-attachments/assets/90fd5fc3-104f-4f18-beb8-ef637a1f24e6)

 
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
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
```


## OUTPUT
![image](https://github.com/user-attachments/assets/90fd5fc3-104f-4f18-beb8-ef637a1f24e6)

 
cat>exread.sh 
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
![image](https://github.com/user-attachments/assets/3a13d055-ffe2-4868-a260-f89881fdfc10)



 cat>exread1.sh
```bash
#!/bin/bash
# testing the read command
read -n "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 

## OUTPUT
![image](https://github.com/user-attachments/assets/94654506-220b-4550-ba8e-9e21051a5b9a)





 
cat>funcex.sh
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
![image](https://github.com/user-attachments/assets/6ce04ee8-d06a-4026-bc95-7aba9d278b8e)
./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/aec42264-8ab5-4ef8-b97a-c666ba4bac14)



 


 
cat>argshift.sh
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
![image](https://github.com/user-attachments/assets/4ee78e77-e877-4cb0-831a-bde60453ed0d)

 
 cat>argshift1.sh
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
![image](https://github.com/user-attachments/assets/42172da7-8aa1-4052-ad3a-788eb44b01c3)

 
cat>argshift.sh
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
 ![image](https://github.com/user-attachments/assets/21d9bf55-5975-4a65-8dcf-f2c8a649c980)

 
 
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
![image](https://github.com/user-attachments/assets/65c20d63-ac76-466c-a398-2299d5d1d0d0)

 
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
![image](https://github.com/user-attachments/assets/e5b5dbd5-a355-4b1f-a21a-8f883ab98b9b)



# RESULT:
The Commands are executed successfully.
