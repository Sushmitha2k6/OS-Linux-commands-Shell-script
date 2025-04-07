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

![Screenshot 2025-03-26 210800](https://github.com/user-attachments/assets/2f9ee40d-12ec-4876-9285-3e866dacbdc2)


cat < file2
## OUTPUT


![Screenshot 2025-03-26 210812](https://github.com/user-attachments/assets/2c62b459-1da0-4f5e-b374-e9441c5fdcb1)


# Comparing Files
cmp file1 file2
## OUTPUT


![Screenshot 2025-03-26 210827](https://github.com/user-attachments/assets/78a8fa0a-3732-423e-8d92-4bb846a036a8)


 
comm file1 file2
 ## OUTPUT

![Screenshot 2025-03-26 210842](https://github.com/user-attachments/assets/b8f6be74-8a02-4b4d-9d5f-d76cb22d2677)


 
diff file1 file2
## OUTPUT


![Screenshot 2025-03-26 210858](https://github.com/user-attachments/assets/ea0c344e-ee8f-4e5b-aa9e-e9f667207332)



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


![Screenshot 2025-03-26 213417](https://github.com/user-attachments/assets/6fe46ad2-5b3c-447e-a403-0332f690056c)


cut -d "|" -f 1 file22
## OUTPUT

![Screenshot 2025-03-26 213449](https://github.com/user-attachments/assets/e456adbe-5205-41cf-9ec3-08f4ec0da11f)


cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-03-26 213508](https://github.com/user-attachments/assets/46d26780-966c-4007-86d8-950aaf4f196e)


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

![Screenshot 2025-03-26 213551](https://github.com/user-attachments/assets/602929cd-96c2-434b-a738-84bd1c96d2fc)


grep hello newfile 
## OUTPUT

![Screenshot 2025-03-26 213559](https://github.com/user-attachments/assets/67e1e95a-15be-4a6f-9cdf-c0ad110adfb2)



grep -v hello newfile 
## OUTPUT
![Screenshot 2025-03-26 213609](https://github.com/user-attachments/assets/b73050ee-5b50-4bea-91e5-5ff749caefbd)



cat newfile | grep -i "hello"
## OUTPUT


![Screenshot 2025-03-26 213619](https://github.com/user-attachments/assets/54948a12-8888-4017-a280-6503e7905518)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot 2025-03-26 213619](https://github.com/user-attachments/assets/32b89267-7f18-430f-a682-827d66a5dce1)
![Screenshot 2025-03-26 213635](https://github.com/user-attachments/assets/b0a771b5-a17e-4575-aea1-44e7e538dd63)



grep -R ubuntu /etc

![Screenshot 2025-03-26 213635](https://github.com/user-attachments/assets/b0a771b5-a17e-4575-aea1-44e7e538dd63)
## OUTPUT

![Screenshot 2025-03-26 213732](https://github.com/user-attachments/assets/cf1a5cc0-9dc4-4d8f-ab2b-fa9383c760c0)


grep -w -n world newfile   
## OUTPUT
![Screenshot 2025-03-26 222232](https://github.com/user-attachments/assets/c7a653bb-1863-418a-9d3c-a635666c82d4)


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


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2025-03-26 222340](https://github.com/user-attachments/assets/99ba4ac6-dd24-41f3-beb4-3669a2b1a236)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![Screenshot 2025-03-26 222352](https://github.com/user-attachments/assets/61670562-adfb-447e-985a-1a3d838b3333)


egrep '(^hello)' newfile 
## OUTPUT

![Screenshot 2025-03-26 222359](https://github.com/user-attachments/assets/5fb2a501-a145-4440-8ce1-04ae4f283c67)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot 2025-03-26 222433](https://github.com/user-attachments/assets/b865fac4-d7dc-4cd7-b3fc-15990f4c292e)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot 2025-03-26 222453](https://github.com/user-attachments/assets/c9dd7fcc-6d74-4c11-b633-fd30d5bd7012)


egrep '[1-9]' newfile 
## OUTPUT


![Screenshot 2025-03-26 222522](https://github.com/user-attachments/assets/cbc4e078-cba5-44b7-aa50-81ee49676750)



egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot 2025-03-26 222538](https://github.com/user-attachments/assets/229a6209-1397-446b-8156-c224688fb9f9)

egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot 2025-03-26 222602](https://github.com/user-attachments/assets/b8bda186-ee6b-4c5c-a65b-6bb5f6117c2e)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2025-03-26 222653](https://github.com/user-attachments/assets/ff7c8259-833b-43c2-a3a3-4446c233257f)


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

![Screenshot 2025-03-26 222702](https://github.com/user-attachments/assets/a3f4a1ff-80f2-446c-a241-8f62afb7db1f)


sed -n -e '$p' file23
## OUTPUT

![Screenshot 2025-03-26 222702](https://github.com/user-attachments/assets/6758f060-80c2-4a07-a047-608c23afe110)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot 2025-03-26 230531](https://github.com/user-attachments/assets/82f50059-8411-4083-aafd-a6e802348b01)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot 2025-03-26 230543](https://github.com/user-attachments/assets/c76d5979-1d6d-47af-aadd-c8e322bfbe18)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot 2025-03-26 230610](https://github.com/user-attachments/assets/bafde40c-0661-48df-8c54-9d182234f674)



sed -n -e '1,5p' file23
## OUTPUT

![Screenshot 2025-03-26 230618](https://github.com/user-attachments/assets/fd2b9afd-9749-4268-b284-86e4b12b2a46)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot 2025-03-26 230642](https://github.com/user-attachments/assets/668ef8f0-db09-4df6-91eb-5b2e3efffcd0)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot 2025-03-26 230642](https://github.com/user-attachments/assets/e22abdde-e522-49ed-99df-de03c4d54201)


seq 10 
## OUTPUT

![Screenshot 2025-03-26 230653](https://github.com/user-attachments/assets/cd0f405a-273c-4c86-89e8-c80cb0bc59ec)

seq 10 | sed -n '4,6p'
## OUTPUT


![Screenshot 2025-03-26 231316](https://github.com/user-attachments/assets/69b65dae-0785-485f-9f30-67cdd5e8c7e2)

seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot 2025-03-26 231328](https://github.com/user-attachments/assets/58e7ab82-f889-48ee-853b-4fbc165b8071)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2025-03-26 231359](https://github.com/user-attachments/assets/2042ea02-0395-403e-824e-0b10b32ae9aa)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot 2025-03-26 231408](https://github.com/user-attachments/assets/1fd0445e-d5ba-42f8-b772-1ffee761530d)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot 2025-03-26 232040](https://github.com/user-attachments/assets/65acb364-654f-452e-a1fe-91545dab5a7d)


sed -n '2,4{s/$/*/;p}' file23


![Screenshot 2025-03-26 232049](https://github.com/user-attachments/assets/e3dc63b1-1e81-4ef7-a2e1-a35d940d3de7)


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

![Screenshot 2025-03-28 170821](https://github.com/user-attachments/assets/2d14216c-ebfc-4764-897e-b80bb60ea7af)

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

![Screenshot 2025-03-28 170840](https://github.com/user-attachments/assets/ab43d735-3ab6-4dbb-8307-7ef902c59f96)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![Screenshot 2025-03-28 170851](https://github.com/user-attachments/assets/45b64a7b-dca4-403c-809c-9efccd565c2a)


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

![Screenshot 2025-03-28 170908](https://github.com/user-attachments/assets/f0ce5c82-4928-449f-95ad-9db29996ff24)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2025-03-28 170917](https://github.com/user-attachments/assets/22251b0c-439c-41e4-a96a-5b1cecf3e7fa)



tar -xvf backup.tar
## OUTPUT

![Screenshot 2025-03-28 175145](https://github.com/user-attachments/assets/6399a46b-b440-46a3-abff-3000610e3fe0)


gzip backup.tar

ls *.gz
## OUTPUT


![Screenshot 2025-03-28 175249](https://github.com/user-attachments/assets/f8bc62f8-9f54-4fd2-802e-0725600c9d55)



 
gunzip backup.tar.gz
## OUTPUT


![Screenshot 2025-03-28 175257](https://github.com/user-attachments/assets/d985a497-3228-42d6-bc0d-7a2972733fe7)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


![Screenshot 2025-03-28 175306](https://github.com/user-attachments/assets/60a57ad4-1002-44b5-ad75-14706ed6d584)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


![Screenshot 2025-03-28 175316](https://github.com/user-attachments/assets/2c38abbb-fbab-4c42-892d-cf0eaf07ef8d)


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



![Screenshot 2025-03-30 123324](https://github.com/user-attachments/assets/7d201ce6-3c13-4dd1-97e8-cef80f2c494e)

 
ls file1
## OUTPUT


![Screenshot 2025-03-30 123336](https://github.com/user-attachments/assets/85aedb2c-becd-4664-9202-af3ac6976aa2)



echo $?
## OUTPUT 


![Screenshot 2025-03-30 123342](https://github.com/user-attachments/assets/0036fe18-2d3d-4759-a578-658b573082a3)

 
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


![Screenshot 2025-03-30 123405](https://github.com/user-attachments/assets/56034afc-12c3-4715-9554-26ff2e284977)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![Screenshot 2025-03-30 123418](https://github.com/user-attachments/assets/d19af3dc-3cd1-4e46-88be-2a6a39dbdc67)



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


![Screenshot 2025-03-30 123426](https://github.com/user-attachments/assets/c576acc6-7fd6-4063-87c8-50b3eba4f2d4)



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
