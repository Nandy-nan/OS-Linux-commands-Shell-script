
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
![image](https://github.com/user-attachments/assets/5792619c-2fa4-4fe9-a6d6-ceb930de64bc)



cat < file2
## OUTPUT


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/82a6f5c9-b972-4bc6-b256-4caaef603c8b)

 
comm file1 file2
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/e6360349-1090-447c-9afd-9f1a3ccbfb20)


 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/8cd9b8d1-ddd9-47f0-924a-e57c9f24aa31)



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

![image](https://github.com/user-attachments/assets/453d537e-62cc-434c-bc3a-32efacac2a64)



cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/677883b9-7176-42af-9455-c61e5e230669)




cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/45f66da9-d2a5-47ac-b443-b69a39c1e60d)



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
![image](https://github.com/user-attachments/assets/6c05e926-a4b6-4b14-ac80-37ad6114b74d)




grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/38482696-e007-4339-9b39-6caf15347576)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/74227bee-cc54-4936-af46-0495da1f62a8)




cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/86a294d6-b2df-46b0-a402-c09c25ba892f)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/3bf3e982-bfee-4a89-871b-0710534792fe)




grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/405007e9-ba0b-4399-9b07-dbbd9e590ab3)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/bc88731a-b4ba-411c-aaf9-c41cc136a1e4)



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
![image](https://github.com/user-attachments/assets/f12e7f5c-3a3a-4c4b-921e-4fff2a118bf5)




egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b11c075e-3b21-4dc6-a993-648ee21b29d3)





egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a7a98a08-55cd-4231-9fd1-54ddfe13dc61)




egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d5010aaf-3f88-44ae-8d78-8ca55b39c00b)




egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/7025acaf-7428-4568-bae6-9e7e9f57ef91)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/40af4d9b-6cc1-49ee-ae52-2bdd1bae1055)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/eb079467-9493-4163-a2ea-b7e5133f38f4)




egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/745663c6-66b2-4fad-9655-52642e5f7a42)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/709880a5-e6d5-4406-a34b-6b67432e1fd3)



egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/349d8e4b-1d9a-4593-93f1-8f74126b677a)




egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/a6061b41-67de-4660-a47e-22c32241c1d1)



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
![image](https://github.com/user-attachments/assets/ac0d4ceb-9f6b-4155-9ddb-ce13bd7a4837)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/2e4eaf53-2493-438a-a71e-9b67d3440461)




sed  -e 's/Ram/Sita/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/b56f2cb9-4dcb-4eed-96e6-4f932285f64f)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/52e64821-597d-45fc-8968-ff9d7e20541e)



sed  '/tom/s/5000/6000/' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/0f29aaac-c7ae-46d1-8b65-0dc8719f79b2)



sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/e61a681c-9203-46dc-a5e6-8acd65c79a07)



sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/172c8db9-8230-4dda-b43f-29e809e6ea23)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/5d8daa20-4a58-4a8d-8a4b-ba51a212c5f5)



seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/809c123f-8451-4807-83da-8b366edca396)




seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/ae71fa6e-959e-4f08-b1b8-d15b90f0714c)




seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/fa775c42-5ed4-41c6-87c7-92f9255633c2)




seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/d4e94d18-6c35-4958-8902-f79aeac0261b)




seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/44230cbc-e458-4e4e-afaa-2b9dcd9e3a2c)



seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/708d371e-9d61-4b84-8a35-9f509e1432cf)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/2952f287-ae8c-4bed-91af-fa24ecf13e5d)




sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/user-attachments/assets/cde1b0dd-73c3-4115-8292-38a1a83a11ee)


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

![image](https://github.com/user-attachments/assets/ef1003d5-0a8f-4522-a3ae-4a435a40a83f)




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

![image](https://github.com/user-attachments/assets/01782dc2-24af-4320-937d-8785166ca247)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/a22255b3-8af2-4a97-a8a3-35b2b3431ee5)


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

 ![image](https://github.com/user-attachments/assets/90525973-da89-4e1f-8387-a9688578fc7f)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


![image](https://github.com/user-attachments/assets/2caa046c-0df8-408d-94b4-d6fbb2a70c0f)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/ba12366a-c4f4-4fd5-b8f9-920cf23457bb)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/348ce348-c069-414a-b68e-4faff9d89e9c)


tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/dbdcfa0a-de3f-41e9-86c5-c2d1e4a2dc8a)


gzip backup.tar

ls .gz
## OUTPUT


 ![image](https://github.com/user-attachments/assets/78002de3-1331-4823-ac61-cbc0b4912d8a)

gunzip backup.tar.gz
## OUTPUT


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/009dcc35-2dc7-409e-b374-5485e2ae828d)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/319e2f78-8239-4acd-b7c2-bfe327be14ee)



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

![image](https://github.com/user-attachments/assets/db6a6dec-2a0c-450d-b75e-ed51d9a6513c)


 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/4e741e53-2ade-4748-919a-2ff54052a815)


echo $?
## OUTPUT 

![image](https://github.com/user-attachments/assets/137de412-2683-405c-a495-d213eb9bf175)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

![image](https://github.com/user-attachments/assets/f8d0c419-c909-4449-86b9-1e9cc2f49329)


 
abcd
 
echo $?
 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/2e715f79-d269-4e42-98f4-286cfcaf9364)



 
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

![image](https://github.com/user-attachments/assets/d2699ca5-a29b-4ad6-bf71-d5c6117bc90b)




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

![image](https://github.com/user-attachments/assets/b3b6d76f-f3e4-47f9-a47f-adc4cd67daf8)


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

![image](https://github.com/user-attachments/assets/cf20b93d-ff6a-4f83-b768-ee576b95410d)



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

![image](https://github.com/user-attachments/assets/e946e780-2ac0-449c-b0ea-2cf51844d02b)



# RESULT:
The Commands are executed successfully.
