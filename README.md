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
![image](https://github.com/user-attachments/assets/08f54037-c222-47ae-b596-e0135d9f547a)


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



# RESULT:
The Commands are executed successfully.
