<img width="746" alt="image" src="https://github.com/user-attachments/assets/7a70881a-db76-4596-8b12-9d0f5ba1e6a4" /><img width="795" alt="image" src="https://github.com/user-attachments/assets/0c7d778b-7f0d-49ab-b59a-03eeb825b502" /># OS-Linux-commands-Shell-scripting
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
<img width="582" alt="image" src="https://github.com/user-attachments/assets/eb3ab5f7-bfcf-473c-8f21-27ad3fefd9bd" />




cat < file2
## OUTPUT
<img width="582" alt="image" src="https://github.com/user-attachments/assets/4b2584a9-79d1-4f2c-b9c6-3c58df2b88ac" />



# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT

 
diff file1 file2
## OUTPUT
<img width="642" alt="image" src="https://github.com/user-attachments/assets/c84cb6a8-b832-469f-8d4c-7a97d4ddae0d" />


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

<img width="642" alt="image" src="https://github.com/user-attachments/assets/dcc315eb-85f2-4807-8f6a-16c5cc796ee5" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="700" alt="image" src="https://github.com/user-attachments/assets/a2f85273-53d2-4081-8af6-a2996d1a3759" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="700" alt="image" src="https://github.com/user-attachments/assets/1cf92932-dad7-4fb9-a3f1-99574cf38037" />


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

<img width="700" alt="image" src="https://github.com/user-attachments/assets/3be339c5-0a4a-4f57-8875-f6d260efa777" />



grep hello newfile 
## OUTPUT
<img width="700" alt="image" src="https://github.com/user-attachments/assets/e08ad934-6309-4865-a845-1cfb3c646bc4" />




grep -v hello newfile 
## OUTPUT
<img width="700" alt="image" src="https://github.com/user-attachments/assets/7b16a3da-9737-49d3-9c5a-dddf7d098b03" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="759" alt="image" src="https://github.com/user-attachments/assets/ceaec56f-f6f9-4750-9f2e-63a8fb2e8d83" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/74ec03de-8ec9-44fe-91a2-1247a29a6d2d" />




grep -R ubuntu /etc
## OUTPUT

<img width="795" alt="image" src="https://github.com/user-attachments/assets/196a5a8d-025d-40d6-bf7f-98bc58d15501" />


grep -w -n world newfile   
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/eb2c8d3a-95f0-4ddc-a118-ac92bf2ff73c" />


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
<img width="795" alt="image" src="https://github.com/user-attachments/assets/9432d9d5-11f9-4c6d-bfae-ed2c31897dd5" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/98fe141b-f48a-40d7-9911-0c5e7baf909f" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/131b721e-4436-45e5-88d5-e2ef172dd77b" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/c28332e1-cc60-4463-854b-f3a42830f3b5" />



egrep '(world$)' newfile 
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/ba66cb6f-c9f3-4f0c-b690-6668675c1afe" />



egrep '(World$)' newfile 
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/b1eafcda-773e-461b-b774-1f0285d4531e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/209e3a50-7ffe-41dc-8689-5d4fc407200d" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/26cb2464-4c24-415d-adf4-17f314e7f24d" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/a1f2652f-de1c-4589-85c4-552c8e569a3c" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/a0e7fab2-0c23-4409-98c5-e09279abacec" />


egrep l{2} newfile
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/325a6928-e524-424b-aecb-8f8bd7198e3a" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="795" alt="image" src="https://github.com/user-attachments/assets/c56a1a86-6404-44c7-8794-281a16eaf2a2" />


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
<img width="795" alt="image" src="https://github.com/user-attachments/assets/213020db-ee4a-4871-9f42-5cdb2471d5d4" />



sed -n -e '$p' file23
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/c0341647-04a8-4d0d-9de9-97535d9a634a" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/58aaeb9e-41dc-4b43-bcd3-08646e74745e" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/574914cf-0008-4e54-9b0e-ae7d435de02b" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/f570759e-0ebe-4d59-8729-6a5efc07e9a0" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="795" alt="image" src="https://github.com/user-attachments/assets/0eb06587-b000-4c0b-b041-10b4d78efd0a" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="746" alt="image" src="https://github.com/user-attachments/assets/3c4a67cb-43bb-4bc6-af4e-cc82745f5537" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="786" alt="image" src="https://github.com/user-attachments/assets/4015fa99-8208-43ef-ad8b-4077f064c569" />



seq 10 
## OUTPUT
<img width="529" alt="image" src="https://github.com/user-attachments/assets/dbd59beb-d48b-49b6-8229-207817744acf" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="688" alt="image" src="https://github.com/user-attachments/assets/e826c09d-468b-4bb8-b143-408a2101ba39" />



seq 10 | sed -n '2, 4p'
## OUTPUT
<img width="688" alt="image" src="https://github.com/user-attachments/assets/59a45e69-bbd5-4843-a430-c628adc32408" />



seq 3 | sed '2a\hello'
## OUTPUT
<img width="688" alt="image" src="https://github.com/user-attachments/assets/c5cf5000-0f2a-4f27-a10e-ad4a99f1a028" />



seq 2 | sed '2i\
hello'
## OUTPUT
<img width="688" alt="image" src="https://github.com/user-attachments/assets/99197dd3-2afb-41e8-924a-d3a7f9ec5ea5" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="688" alt="image" src="https://github.com/user-attachments/assets/9c80cbba-c316-425d-b2a7-fa474569fdf3" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="688" alt="image" src="https://github.com/user-attachments/assets/d44ced9a-42c4-41c7-a68a-8f9ea903a8ed" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="688" alt="image" src="https://github.com/user-attachments/assets/5f3cd0d4-a665-4423-9c28-8c9858782169" />


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
<img width="688" alt="image" src="https://github.com/user-attachments/assets/4cdbb3f6-acea-4650-a458-3ac27a68078c" />


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
<img width="587" alt="image" src="https://github.com/user-attachments/assets/e0c790a2-4445-441e-97ae-b0416aad47bb" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="812" alt="image" src="https://github.com/user-attachments/assets/eb27c79a-1b18-4891-81ba-a6bc7f098f7e" />

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
<img width="812" alt="image" src="https://github.com/user-attachments/assets/2564859a-b017-4bac-ba3f-53ac5a088ff6" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="812" alt="image" src="https://github.com/user-attachments/assets/560afde4-6b49-4334-9717-c02c1bc0444f" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="812" alt="image" src="https://github.com/user-attachments/assets/e4b232a7-70cb-4067-a648-309b2241dfd9" />


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="812" alt="image" src="https://github.com/user-attachments/assets/0acea997-1b3a-4dae-9996-8bf87943559f" />


tar -xvf backup.tar
## OUTPUT
<img width="812" alt="image" src="https://github.com/user-attachments/assets/946d8839-e051-4115-b7a6-9ed69725a4a0" />

gzip backup.tar

ls .gz
## OUTPUT
 
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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
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
