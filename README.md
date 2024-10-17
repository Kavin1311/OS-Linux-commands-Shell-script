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
guptabarun sengupta
c.k. shukla
lalit chowdury
s.n. das
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/user-attachments/assets/9ce08987-c533-4c37-9a80-75999b7e8588)



cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/d7616476-49f7-4ce6-9f6a-7958bb79d9ba)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/65db1b00-76bb-4a5d-90e1-ef88a4e06e78)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/fa220040-dc51-4257-91b0-a35957b5099e)

 
diff file1 file2
## OUTPUT
![image-4](https://github.com/user-attachments/assets/f9820900-9e3f-43e9-9892-ef20490d4317)


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
![image-83](https://github.com/user-attachments/assets/a8caf96b-7d4b-4dfd-a58a-0dfc7f874574)




cut -d "|" -f 1 file22
## OUTPUT

![image-5](https://github.com/user-attachments/assets/67198206-04ef-41d3-9ca2-5835929bae9d)


cut -d "|" -f 2 file22
## OUTPUT
![image-6](https://github.com/user-attachments/assets/a01551b8-8534-4bc7-bcd5-3ee471c15b13)


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
![image-7](https://github.com/user-attachments/assets/f1c450df-48c1-4a55-9502-3b328b81029b)


grep hello newfile 
## OUTPUT
![image-8](https://github.com/user-attachments/assets/29d902e4-eb77-4676-a72e-b04ad6b3516d)




grep -v hello newfile 
## OUTPUT
![image-9](https://github.com/user-attachments/assets/bc596746-4ce0-42ad-9f0b-49d7ea4d4f48)




cat newfile | grep -i "hello"
## OUTPUT
![image-10](https://github.com/user-attachments/assets/b255b2fb-1a40-4810-ac9b-da43a6c88709)




cat newfile | grep -i -c "hello"
## OUTPUT
![image-11](https://github.com/user-attachments/assets/9c9bd9f9-26dd-4ef8-8825-0631b9edd01e)



grep -R ubuntu /etc
## OUTPUT
![image-12](https://github.com/user-attachments/assets/35b87c84-2f5d-4fd3-83d0-74700f50d1f1)



grep -w -n world newfile   
## OUTPUT
![image-13](https://github.com/user-attachments/assets/8614a0a0-81c9-4a40-b991-21e433314468)


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
![image-14](https://github.com/user-attachments/assets/4aa70e59-ab9d-44cf-963f-c4d8726f5cb5)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image-15](https://github.com/user-attachments/assets/d00c88fa-056e-4421-a249-519f77bb9424)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image-16](https://github.com/user-attachments/assets/f565f3fd-3e5f-46a9-90cf-01a5fa6d3db5)



egrep '(^hello)' newfile 
## OUTPUT
![image-17](https://github.com/user-attachments/assets/60d7902a-8d38-4909-a2b8-54b0348e7e4a)



egrep '(world$)' newfile 
## OUTPUT
![image-18](https://github.com/user-attachments/assets/6fb52ddb-4572-4e2e-bdd6-4dc89fa3e406)



egrep '(World$)' newfile 
## OUTPUT
![image-19](https://github.com/user-attachments/assets/a921d19f-7624-47ad-8a03-9743dfccf39e)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image-20](https://github.com/user-attachments/assets/cd52ab67-3c92-4a16-90a6-3dfc9ed52a3d)



egrep '[1-9]' newfile 
## OUTPUT
![image-21](https://github.com/user-attachments/assets/09eae081-03b8-4927-8557-83f33544f791)



egrep 'Linux.*world' newfile 
## OUTPUT
![image-22](https://github.com/user-attachments/assets/2868e499-237b-424c-9111-7677f0664b2c)


egrep 'Linux.*World' newfile 
## OUTPUT
![image-23](https://github.com/user-attachments/assets/97d99fa8-d649-43d3-aa19-c28d4b3ee9c7)

egrep l{2} newfile
## OUTPUT

![image-24](https://github.com/user-attachments/assets/fce6ad90-7a42-4a29-9920-36f4147b975a)


egrep 's{1,2}' newfile
## OUTPUT 

![image-25](https://github.com/user-attachments/assets/8f27d416-2291-4074-ab8a-8ed5f3ea766d)

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
![image-26](https://github.com/user-attachments/assets/a3f39465-e24b-436c-af7d-d92ff3676d76)



sed -n -e '$p' file23
## OUTPUT
![image-27](https://github.com/user-attachments/assets/b66220ea-41a8-46ee-8444-96d825e28edf)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image-28](https://github.com/user-attachments/assets/dc093252-678c-4a01-b217-69db1ae6e4de)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image-29](https://github.com/user-attachments/assets/20635d0f-e144-46c3-a989-5c88674bb6db)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image-30](https://github.com/user-attachments/assets/509ed29f-f209-405c-b049-42a2aa4347bc)



sed -n -e '1,5p' file23
## OUTPUT

![image-31](https://github.com/user-attachments/assets/3a95d489-7146-47f5-ae18-abd12c43b4fb)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![image-32](https://github.com/user-attachments/assets/0266da49-a9cf-41bd-bf7b-9277dda50e31)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image-33](https://github.com/user-attachments/assets/68caf48c-094e-45e2-9036-35239bbe454a)



seq 10 
## OUTPUT
![image-34](https://github.com/user-attachments/assets/539c467c-e2aa-41a1-b9c0-5cefc7b3f5e7)

seq 10 | sed -n '4,6p'
## OUTPUT
![image-35](https://github.com/user-attachments/assets/df9a834f-9ad3-43a3-9bce-3d021da65f1b)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image-36](https://github.com/user-attachments/assets/963fd223-caa9-419a-b389-c40f98ce2834)



seq 3 | sed '2a hello'
## OUTPUT
![image-37](https://github.com/user-attachments/assets/4aece7d3-edf9-4655-a0ba-7b7fe995ef6c)



seq 2 | sed '2i hello'
## OUTPUT
![image-38](https://github.com/user-attachments/assets/a3057b90-4e69-490f-a716-7ea4dbe661f7)


seq 10 | sed '2,9c hello'
## OUTPUT
![image-39](https://github.com/user-attachments/assets/28b74c42-8f6e-4cc7-9117-801f935ef294)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image-40](https://github.com/user-attachments/assets/e7293bef-b147-4c6b-87ae-355df5782a1a)


## OUTPUT 
![image-41](https://github.com/user-attachments/assets/ba871a0c-0d65-4e26-9cb7-f0663694110b)

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
![image-42](https://github.com/user-attachments/assets/ffd16a75-01d2-4b4e-8bb8-b3d962b318cf)


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

![image-43](https://github.com/user-attachments/assets/1e47bddc-0f7d-4ba8-8722-fe4def87ed73)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image-44](https://github.com/user-attachments/assets/1c1b2c01-8c91-46db-ab1c-db82ebcff5ea)

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
![image-45](https://github.com/user-attachments/assets/51294b4c-4bc2-427e-84ac-f0c4b0740f0e)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image-46](https://github.com/user-attachments/assets/173e9504-239e-436e-b7ab-37216a337a6a)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image-47](https://github.com/user-attachments/assets/f20e7309-7d5b-4d4f-990e-95cb7bf5d4d4)



 tar -xvf backup.tar
## OUTPUT
![image-48](https://github.com/user-attachments/assets/43569914-ec37-4ffb-b111-a067600faa79)


gzip backup.tar

ls .gz
## OUTPUT
![image-49](https://github.com/user-attachments/assets/16a5967e-364d-45e3-be3a-2f65acf14251)

gunzip backup.tar.gz
## OUTPUT
![image-81](https://github.com/user-attachments/assets/1a02f253-30a3-45bc-9b82-831a81152f94)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image-82](https://github.com/user-attachments/assets/49f59c85-4923-4ea1-abcd-b26d6492652e)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image-50](https://github.com/user-attachments/assets/25b2dd9c-636b-4752-9892-4d82487c0e10)


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
![image-51](https://github.com/user-attachments/assets/e3ba5241-8a40-4963-bde8-1e3234877a07)

 
ls file1
## OUTPUT
![image-52](https://github.com/user-attachments/assets/46472a7f-3e49-4e01-9ab0-24f0790b9305)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

![image-53](https://github.com/user-attachments/assets/d8e021d3-369b-40e9-b23d-30a248a3d3fb)


 
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


##OUTPUT

![image-54](https://github.com/user-attachments/assets/884e7f62-b536-40f0-9027-36afcc1c77d1)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image-55](https://github.com/user-attachments/assets/51af6d23-5d70-4e89-bb24-53435d9533ac)

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
![image-56](https://github.com/user-attachments/assets/01857c61-e383-4d5c-bc17-13be005c4681)

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

![image-57](https://github.com/user-attachments/assets/3a09d229-c475-420e-a89c-a307dd92e9fe)


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

![image-58](https://github.com/user-attachments/assets/5bef9ee7-4dd1-489b-8b1d-73f054cff4ac)



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
![image-59](https://github.com/user-attachments/assets/6da8c56a-6ce8-4658-bf54-251d2f0d367b)


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
![image-60](https://github.com/user-attachments/assets/5c26ad3d-0b7f-4e88-81c1-4ec4d9155c70)


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
 
 ## OUTPUT
![image-61](https://github.com/user-attachments/assets/5c817909-8f13-4b8f-8b0b-3fbe9f6ac37f)


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
 
 ## OUTPUT
 ![image-62](https://github.com/user-attachments/assets/df778f9a-99ff-4d8d-b3a4-12888521bad9)

 
cat untiltest.sh 
```
bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
## OUTPUT
![image-63](https://github.com/user-attachments/assets/a7117814-0edb-4d0a-963c-7e2a2a0719d9)

 
cat >forin1.sh 
```
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 ## OUTPUT
 ![image-64](https://github.com/user-attachments/assets/7f2e9163-8e79-497d-8401-4cca7d6ae596)


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
 
 ## OUTPUT

![image-65](https://github.com/user-attachments/assets/0943eaf3-6a27-4da2-be5f-2b9d6534c282)


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
![image-66](https://github.com/user-attachments/assets/836207b1-f12a-484b-8a0b-ecfa6238bf5d)


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
![image-67](https://github.com/user-attachments/assets/4acb964b-1e56-4ed1-9312-9bfe61f2d379)


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
![image-68](https://github.com/user-attachments/assets/b3cb23a1-574e-4db2-97a9-32cdde9b028c)


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
 ![image-69](https://github.com/user-attachments/assets/1eb99caa-1fe0-49ee-9af7-575f2a6f8880)

 
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
![image-70](https://github.com/user-attachments/assets/12b13884-f3c9-44da-ac30-ad1d628d36c0)


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
## OUTPUT
![image-71](https://github.com/user-attachments/assets/f72ab9a2-c780-4048-9235-6e33668f90b2)

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![image-72](https://github.com/user-attachments/assets/b131950d-f521-4e0c-a72c-cbf655ec1be6)


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
![image-73](https://github.com/user-attachments/assets/add29e7d-7556-4e60-8c9d-c00e96fef61c)


 
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
![image-73](https://github.com/user-attachments/assets/681e3876-effd-42fa-bd08-2565e15e5840)


 ./funcex.sh 1 2
![image-74](https://github.com/user-attachments/assets/c9e85b43-8b89-495e-82c6-17d60d1b0882)

 
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
![image-76](https://github.com/user-attachments/assets/002c00ae-ef3d-4547-992b-e713a33a2253)

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
![image-77](https://github.com/user-attachments/assets/6d01efbc-7f5a-4681-970c-ff7289159f14)



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

 ![image-78](https://github.com/user-attachments/assets/cb24504a-8bd1-471a-b253-5cac39bc7929)

 
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
 ![image-79](https://github.com/user-attachments/assets/4963484c-7328-4891-89c0-ee9282c737b2)


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
![image-80](https://github.com/user-attachments/assets/03ee5efd-5958-43ed-8c93-4325a217960a)


# RESULT:
The Commands are executed successfully.
