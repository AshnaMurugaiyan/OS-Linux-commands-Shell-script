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
<img width="341" height="102" alt="image" src="https://github.com/user-attachments/assets/0aaa57f3-0639-4688-b4a7-152fbe4d017d" />



cat < file2
## OUTPUT
<img width="328" height="162" alt="image" src="https://github.com/user-attachments/assets/301c20af-c62c-44c0-b686-382c7a3ce08c" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="362" height="44" alt="image" src="https://github.com/user-attachments/assets/23407498-db29-49ec-b4f8-08aa6030a432" />

comm file1 file2
 ## OUTPUT
<img width="375" height="198" alt="image" src="https://github.com/user-attachments/assets/0ccef1d7-9ce2-4b8e-acb5-0d62117cbcb0" />

 
diff file1 file2
## OUTPUT
<img width="428" height="305" alt="image" src="https://github.com/user-attachments/assets/48267267-6efe-437e-b24a-4075df86df7b" />


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

<img width="383" height="84" alt="image" src="https://github.com/user-attachments/assets/1597cf63-5a1c-42f7-8a05-cc6bbe6315e0" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="433" height="109" alt="image" src="https://github.com/user-attachments/assets/9c47caa8-ce34-4a0b-b186-353ad7a67169" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="442" height="110" alt="image" src="https://github.com/user-attachments/assets/b84b09ea-b797-44bf-ac14-743e62ece48f" />


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

<img width="409" height="56" alt="image" src="https://github.com/user-attachments/assets/fe8e0e72-f633-4b9e-a5a1-01759c8b95ca" />


grep hello newfile 
## OUTPUT

<img width="400" height="58" alt="image" src="https://github.com/user-attachments/assets/4f32ffe6-7405-420f-a3ad-ceb9338270e6" />



grep -v hello newfile 
## OUTPUT
<img width="430" height="59" alt="image" src="https://github.com/user-attachments/assets/1703e079-3c95-4589-8c40-04c2576b0b04" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="546" height="81" alt="image" src="https://github.com/user-attachments/assets/e956f454-839d-4dbb-b4dc-dd9a5741725b" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="578" height="52" alt="image" src="https://github.com/user-attachments/assets/6e2e5151-6f9f-4adf-a2a9-97081dacbd4b" />



grep -R ubuntu /etc
## OUTPUT

<img width="609" height="218" alt="image" src="https://github.com/user-attachments/assets/b994371d-fe49-42ad-bcbb-dcf04edd2e13" />



grep -w -n world newfile   
## OUTPUT
<img width="474" height="80" alt="image" src="https://github.com/user-attachments/assets/7eb52472-0775-42dc-ba71-ab66f5c23487" />


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

<img width="563" height="78" alt="image" src="https://github.com/user-attachments/assets/88e7227a-ab81-4ea1-b7b7-72d7db5b508a" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/63dd4200-a0e7-4e7d-9afb-e5917a715963" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/2b342072-5d1c-4f0c-9b14-eb8019f49c2a" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="489" height="58" alt="image" src="https://github.com/user-attachments/assets/2a119332-9573-4321-88bf-530b95969fe6" />


egrep '(world$)' newfile 
## OUTPUT

<img width="489" height="58" alt="image" src="https://github.com/user-attachments/assets/25c446db-beaf-4799-b479-158d2d48ba61" />


egrep '(World$)' newfile 
## OUTPUT
<img width="485" height="49" alt="image" src="https://github.com/user-attachments/assets/9532181e-845a-471c-bd2d-b310c8aea7f0" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="559" height="76" alt="image" src="https://github.com/user-attachments/assets/c14730ec-159a-4b46-a3d1-2334029b898f" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="475" height="62" alt="image" src="https://github.com/user-attachments/assets/fd8c8e94-8f37-4042-b547-cbe518886819" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="547" height="55" alt="image" src="https://github.com/user-attachments/assets/25f8adf2-3bf9-4519-b643-cf19183f6c65" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="540" height="57" alt="image" src="https://github.com/user-attachments/assets/a5a000ed-66a2-40a8-95ef-fc973c63615e" />

egrep l{2} newfile
## OUTPUT

<img width="549" height="76" alt="image" src="https://github.com/user-attachments/assets/43cd6102-3a1f-4b7a-b405-a702bf419f5e" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="492" height="116" alt="image" src="https://github.com/user-attachments/assets/ee4445cb-40a1-4800-9ca4-6fbaaa6430b8" />


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

<img width="446" height="52" alt="image" src="https://github.com/user-attachments/assets/d2753d44-db34-4951-8e4a-332943b95449" />


sed -n -e '$p' file23
## OUTPUT

<img width="463" height="58" alt="image" src="https://github.com/user-attachments/assets/8813d316-c1bc-4003-9f67-8e3d428415c4" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="520" height="243" alt="image" src="https://github.com/user-attachments/assets/32fec562-3a97-4ab7-9aa8-5a9ab9158646" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="521" height="237" alt="image" src="https://github.com/user-attachments/assets/8bbb912a-d9f1-4f01-b121-1c512b37b82e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="555" height="245" alt="image" src="https://github.com/user-attachments/assets/77ee3b3b-7726-4eef-8e05-e272c32033b4" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="481" height="169" alt="image" src="https://github.com/user-attachments/assets/cb0b125c-6cf3-467e-9a6e-37e6cd2f9465" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="520" height="108" alt="image" src="https://github.com/user-attachments/assets/f750c789-b7da-48ec-a455-f765bd29d562" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="560" height="83" alt="image" src="https://github.com/user-attachments/assets/3ce812e7-2e8e-4a48-919d-65977df0a8c4" />


seq 10 
## OUTPUT

<img width="470" height="241" alt="image" src="https://github.com/user-attachments/assets/a12c920d-8135-4bd8-aa9c-a0419534eca7" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/b3bdef63-2096-469b-a6a7-f2fe5c1b45c1" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/7b20ffa0-bfd3-415e-b12e-b6e13b47fcfb" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="476" height="116" alt="image" src="https://github.com/user-attachments/assets/ab41c5c1-16a5-4ad6-9f3a-6d04a17522fc" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/ab9487c9-988f-4724-995f-034d0851c5bb" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/d3d8141e-2848-4275-ba87-93e3f1e084a7" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="542" height="102" alt="image" src="https://github.com/user-attachments/assets/171f978e-7bbf-44d1-bdd0-34fd9428ed19" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="565" height="112" alt="image" src="https://github.com/user-attachments/assets/d55abc94-cfdc-48ec-82b9-01b6a5e1773c" />

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
<img width="343" height="156" alt="image" src="https://github.com/user-attachments/assets/0e52632b-3600-4d62-93d6-93fd523fdd00" />


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

<img width="363" height="160" alt="image" src="https://github.com/user-attachments/assets/026ad56a-360b-47eb-876b-a2d8ee6aad1c" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="652" height="243" alt="image" src="https://github.com/user-attachments/assets/f77d5913-1d0f-41c3-adca-6d95950a470d" />

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

<img width="536" height="113" alt="image" src="https://github.com/user-attachments/assets/1998c940-b0de-4164-a274-bbf9cda278fa" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="304" height="149" alt="image" src="https://github.com/user-attachments/assets/d21c60a8-732d-4dbf-8798-f5b67414e1ec" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="393" height="140" alt="image" src="https://github.com/user-attachments/assets/54f47cc0-5d6e-4bf2-b14f-b563834e84dc" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="474" height="163" alt="image" src="https://github.com/user-attachments/assets/0842b524-4e10-45c8-aa9f-f91f4c3742c7" />


tar -xvf backup.tar
## OUTPUT
<img width="393" height="140" alt="image" src="https://github.com/user-attachments/assets/30f7fb56-11bf-43e3-ad3a-92d95c546b4d" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="644" height="140" alt="image" src="https://github.com/user-attachments/assets/03110fd6-7914-4e50-930c-d4db3dca0e6a" />

gunzip backup.tar.gz
## OUTPUT
<img width="648" height="196" alt="image" src="https://github.com/user-attachments/assets/43efed6b-9095-4848-835a-1bb6074fda25" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="785" height="335" alt="image" src="https://github.com/user-attachments/assets/f46dc4d9-d011-4645-bb4b-f12ae383c776" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="337" height="97" alt="image" src="https://github.com/user-attachments/assets/b31f415b-6f57-4093-87d3-88f9cec6c5d3" />


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
<img width="430" height="331" alt="image" src="https://github.com/user-attachments/assets/860ec88a-b047-4eca-9499-f9e9e6ede391" />

 
ls file1
## OUTPUT
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/a8914ac7-19d2-4d23-9c26-8c0c0dd9a36b" />

echo $?
## OUTPUT 
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/b32e4a48-a367-432a-80a9-5507e58002b8" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/4a49bed9-785c-4a35-a0e1-612838e2fe55" />

abcd
 
echo $?
 ## OUTPUT

<img width="469" height="221" alt="image" src="https://github.com/user-attachments/assets/38369fa4-fc27-4dec-9d1c-ffde56c45da1" />

 
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

<img width="476" height="243" alt="image" src="https://github.com/user-attachments/assets/09ff6032-04e2-40e7-a06e-4f0b61805409" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="725" height="222" alt="image" src="https://github.com/user-attachments/assets/d356dabf-e435-4a15-8527-46501763d3eb" />

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
<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/4a778fb3-bc71-4e24-8cf4-7b95d79e8ae5" />

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

<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/ff26a5e5-563a-4d1e-b2fa-60ab691c3a7a" />


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
<img width="524" height="391" alt="image" src="https://github.com/user-attachments/assets/6748d0ab-5eff-44ff-9e19-c2d7dc5bc9dd" />

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
<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/e2028714-47e8-4c34-83d0-a4b06dec613f" />

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
<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/22bd3ef8-391a-4f8b-8a9c-0784925d4f4b" />


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
<img width="541" height="248" alt="image" src="https://github.com/user-attachments/assets/ae401d3e-f545-464b-beff-9c2bb9571bd3" />

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
<img width="504" height="160" alt="image" src="https://github.com/user-attachments/assets/00337bb7-c3ad-4a25-8606-d425adc3a31a" />

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
<img width="446" height="201" alt="image" src="https://github.com/user-attachments/assets/2b92e49b-a31a-45d6-9c00-594fef5607f5" />


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
<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/96bab4fa-f6f1-432c-920d-83fa46626a22" />


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
<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/805ecdc0-c1f3-4466-b069-c4dbddf297de" />

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
<img width="412" height="201" alt="image" src="https://github.com/user-attachments/assets/ed722529-00c3-461a-aa3e-24de52bc23ba" />

 
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
<img width="753" height="287" alt="image" src="https://github.com/user-attachments/assets/c7469bb0-5465-48c9-b7fc-96f1e147e3aa" />

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
 <img width="756" height="275" alt="image" src="https://github.com/user-attachments/assets/f45a6715-e65c-4197-b871-b5d7deccb14f" />

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
<img width="481" height="144" alt="image" src="https://github.com/user-attachments/assets/2687fbca-efbb-46bb-83b0-1d296bbf7cfd" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="774" height="137" alt="image" src="https://github.com/user-attachments/assets/a09dac48-b27c-4a2a-a34a-f6258bda4616" />


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
<img width="755" height="44" alt="image" src="https://github.com/user-attachments/assets/70c4ff41-dabd-4e10-9b4c-9d74a96cf1c3" />


 ./funcex.sh 
<img width="762" height="38" alt="image" src="https://github.com/user-attachments/assets/f339d3a5-ab95-47e7-b027-563575b5b68d" />

 
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
<img width="758" height="63" alt="image" src="https://github.com/user-attachments/assets/856a7d21-70d3-4d72-a620-bc66cbb819d9" />

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
<img width="762" height="87" alt="image" src="https://github.com/user-attachments/assets/2e6845cf-a2d2-4b9d-8435-55c516c7e22a" />

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
 <img width="765" height="327" alt="image" src="https://github.com/user-attachments/assets/8fc57a59-23d6-4241-a3cb-d952e20b51ad" />

 
 
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
 <img width="783" height="218" alt="image" src="https://github.com/user-attachments/assets/cad2067c-6efb-4b8c-945b-826a67d5729c" />

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
<img width="772" height="70" alt="image" src="https://github.com/user-attachments/assets/b2beeb47-5730-4881-9865-48cdffda8b9f" />


# RESULT:
The Commands are executed successfully.
