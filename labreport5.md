__Lab Report 5__
---
One particular lab activity that I would like to revisit would be the exploration of the different ways in which you can use `find` and `grep`. In my 
own lab report 3, I explored 5 different way in which `grep` could be used, including commands such as `grep -v`, `grep "" file_name`, and `grep -c`.
For this report, I am going to explore 5 ways in which you can use the `find` command.

***Some of the terminal output is ommitted because of how long it is***

__First use:__  `find -iname` or searching by approximate name

Example #1:

![Image](Screen Shot 2023-03-12 at 11.41.44 PM.png)

Here is the command and its output in a code block:

```
dronregmi@Drons-MacBook-Air CSE12 % cd docsearch            
dronregmi@Drons-MacBook-Air docsearch % cd written_2            
dronregmi@Drons-MacBook-Air written_2 % cd travel_guides        
dronregmi@Drons-MacBook-Air travel_guides % find .  -iname "Amster*"
./berlitz2/Amsterdam-WhereToGo.txt
./berlitz2/Amsterdam-WhatToDo.txt
./berlitz2/Amsterdam-History.txt
./berlitz2/Amsterdam-Intro.txt
```

Example #2 :

![Image](Screen Shot 2023-03-12 at 11.45.26 PM.png)

Here is the command and its output in a code block:
```
dronregmi@Drons-MacBook-Air CSE12 % cd docsearch            
dronregmi@Drons-MacBook-Air docsearch % cd written_2 
dronregmi@Drons-MacBook-Air written_2 % find . -iname "Cas*"
./non-fiction/OUP/Castro
```

__Second Use:__ `find -type d` or listing directories

Example #1:

![Image](Screen Shot 2023-03-12 at 11.51.22 PM.png)

Here is the command and its output in a code block:
```
dronregmi@Drons-MacBook-Air written_2 % find . -type d          
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Berk
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Rybczynski
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Castro
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz2
```

Example #2:

![Image](Screen Shot 2023-03-12 at 11.54.34 PM.png)

Here is the command and its output in a code block:

```
dronregmi@Drons-MacBook-Air written_2 % cd ..               
dronregmi@Drons-MacBook-Air docsearch % find . -type d
.
./lib
./.git
./.git/objects
./.git/objects/pack
./.git/objects/info
./.git/info
./.git/logs
./.git/logs/refs
./.git/logs/refs/heads
./.git/logs/refs/remotes
./.git/logs/refs/remotes/origin
./.git/hooks
./.git/refs
./.git/refs/heads
./.git/refs/tags
./.git/refs/remotes
./.git/refs/remotes/origin
./written_2
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Berk
./written_2/non-fiction/OUP/Abernathy
./written_2/non-fiction/OUP/Rybczynski
./written_2/non-fiction/OUP/Kauffman
./written_2/non-fiction/OUP/Fletcher
./written_2/non-fiction/OUP/Castro
./written_2/travel_guides
./written_2/travel_guides/berlitz1
./written_2/travel_guides/berlitz2
```

__Third Use:__ `find . -type f -empty` or finding all empty files in the current directory and its subdirectories

Example #1 :

![Image](Screen Shot 2023-03-13 at 12.00.41 AM.png)

Here is the command and its output in a code block:

```
dronregmi@Drons-MacBook-Air docsearch % cd written_2 
dronregmi@Drons-MacBook-Air written_2 % find . -type f -empty   
./foundfile.txt
./founfile.txt
```

Example #2 :

![Image](Screen Shot 2023-03-13 at 12.04.28 AM.png)

Here is the command and its output in a code block:

```
dronregmi@Drons-MacBook-Air written_2 % cd travel_guides 
dronregmi@Drons-MacBook-Air travel_guides % find . -type f -empty
```

__Fourth Use:__ `find -size +_M` or finding files larger than _ amount of megabytes

Example #1:

![Image](Screen Shot 2023-03-13 at 12.56.21 AM.png)


```
dronregmi@Drons-MacBook-Air travel_guides % find . -size +2M 
dronregmi@Drons-MacBook-Air travel_guides % 
```

Example #2:

![Image](Screen Shot 2023-03-13 at 1.05.06 AM.png)

```
dronregmi@Drons-MacBook-Air travel_guides % cd ..
dronregmi@Drons-MacBook-Air written_2 % cd non-fiction 
dronregmi@Drons-MacBook-Air non-fiction % cd OUP 
dronregmi@Drons-MacBook-Air OUP % find . -size +1M
```

__Fifth Use:__ `find . -type f` or finding non-directory files

![Image](Screen Shot 2023-03-13 at 1.30.00 AM.png)

Example #1 : 

```
dronregmi@Drons-MacBook-Air written_2 % find . -type f
./non-fiction/OUP/Berk/ch2.txt
./non-fiction/OUP/Berk/ch1.txt
./non-fiction/OUP/Berk/CH4.txt
./non-fiction/OUP/Berk/ch7.txt
./non-fiction/OUP/Abernathy/ch2.txt
./non-fiction/OUP/Abernathy/ch3.txt
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Abernathy/ch7.txt
./non-fiction/OUP/Abernathy/ch6.txt
./non-fiction/OUP/Abernathy/ch8.txt
./non-fiction/OUP/Abernathy/ch9.txt
./non-fiction/OUP/Abernathy/ch15.txt
./non-fiction/OUP/Abernathy/ch14.txt
./non-fiction/OUP/Rybczynski/ch2.txt
./non-fiction/OUP/Rybczynski/ch3.txt
./non-fiction/OUP/Rybczynski/ch1.txt
./non-fiction/OUP/Kauffman/ch3.txt
./non-fiction/OUP/Kauffman/ch1.txt
./non-fiction/OUP/Kauffman/ch4.txt
./non-fiction/OUP/Kauffman/ch5.txt
./non-fiction/OUP/Kauffman/ch7.txt
./non-fiction/OUP/Kauffman/ch6.txt
./non-fiction/OUP/Kauffman/ch8.txt
./non-fiction/OUP/Kauffman/ch9.txt
./non-fiction/OUP/Kauffman/ch10.txt
./non-fiction/OUP/Fletcher/ch2.txt
./non-fiction/OUP/Fletcher/ch1.txt
./non-fiction/OUP/Fletcher/ch5.txt
./non-fiction/OUP/Fletcher/ch6.txt
./non-fiction/OUP/Fletcher/ch9.txt
./non-fiction/OUP/Fletcher/ch10.txt
./non-fiction/OUP/Castro/chR.txt
./non-fiction/OUP/Castro/chP.txt
./non-fiction/OUP/Castro/chQ.txt
./non-fiction/OUP/Castro/chB.txt
./non-fiction/OUP/Castro/chC.txt
./non-fiction/OUP/Castro/chA.txt
./non-fiction/OUP/Castro/chV.txt

```

Example #2:
