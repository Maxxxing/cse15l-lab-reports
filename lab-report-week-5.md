# __Week 5 Lab Report__

## Command-line options for `find`

<br>

### Example 1:
Code: 
```
find technical/ -iname "CHAPTER.txt"`
```
Output: 

```
technical/911report/chapter-1.txt
```

Explaination:

The function of the command-line option `-iname` for `find` is very similar to `-name` that it can search for files by specific name and ignore case. Different file writers may have different naming conventions, which can be effectively avoided this situation by this command-line.

<br>

### Example 2:
Code: 
```
find technical/ -type d
```

Output:
```
technical/
technical/911report
technical/biomed
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm
technical/plos
```

Explaination:

The function of the command-line option `-type` for `find` is search different type of objects by different key value, such like `d` for folder, `f` for normal file and so on. This command line can help us quickly find special objects which we want. 

<br>

### Example 3:
Code: 
```
echnical/ -type f -size +110k -size -200k
```

Output:
```
technical/911report/chapter-1.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/biomed/1471-2105-3-2.txt
technical/government/About_LSC/State_Planning_Report.txt
technical/government/Env_Prot_Agen/ctm4-10.txt
technical/government/Env_Prot_Agen/multi102902.txt
technical/government/Env_Prot_Agen/tech_adden.txt
technical/government/Gen_Account_Office/May1998_ai98068.txt
technical/government/Gen_Account_Office/Sept27-2002_d02966.txt
technical/government/Gen_Account_Office/ai9868.txt
technical/government/Gen_Account_Office/d01376g.txt
technical/government/Gen_Account_Office/d0269g.txt
technical/government/Gen_Account_Office/d02701.txt
technical/government/Gen_Account_Office/im814.txt
technical/government/Gen_Account_Office/pe1019.txt
```

Explaination:

The function of the command-line option `-size` for `find` is search different files by size. In this example, the command-line is try to search all the normal files which have the size between 110kb to 200kb.




<br>
<br>
<br>

## Command-line options for `less`

<br>

### Example 1:
Code: 
```
less -N findName.txt
```
Output:
```
      1 technical/911report/chapter-1.txt
      2 technical/911report/chapter-10.txt
      3 technical/911report/chapter-11.txt
      4 technical/911report/chapter-12.txt
      ...
      ...
```
Explaination:

The function of the command-line option `-N` for `less` shows the number of lines in the `findName.txt`. This option can help users to have a better reading experience and will not be lost in `less` pages.   


<br>

### Example 2:
Code: 

```
less -E findName.txt
```

Output:
```
NONE
```

Explaination:

The function of the command-line option `-E` for `less` is close the `less` page automatically when the page jump to the end of the file, and go back to the original terminal page. It could be helpful for beginners who don't know how to use `Ctrl+z` or type `q` to get back to the initial terminal.

<br>

### Example 3:
Code: 
```
less -m findName.txt
```

Output:

```
...
...
technical/biomed/1471-2105-4-25.txt
technical/biomed/1471-2105-4-26.txt
technical/biomed/1471-2105-4-27.txt
technical/biomed/1471-2105-4-28.txt
technical/biomed/1471-2105-4-31.txt
technical/biomed/1471-2121-1-2.txt
technical/biomed/1471-2121-2-1.txt
5%
```

Explaination:

The command-line option `-m` for `less` will display a percentage number which present the current position in the file. This option can help users to have a better reading experience.


<br>
<br>
<br>

## Command-line options for `grep`

<br>

### Example 1:
Code: 
```
grep -b "chapter" findName.txt
```

Output:
```
0:technical/911report/chapter-1.txt
34:technical/911report/chapter-10.txt
69:technical/911report/chapter-11.txt
104:technical/911report/chapter-12.txt
139:technical/911report/chapter-13.1.txt
176:technical/911report/chapter-13.2.txt
213:technical/911report/chapter-13.3.txt
250:technical/911report/chapter-13.4.txt
287:technical/911report/chapter-13.5.txt
324:technical/911report/chapter-2.txt
358:technical/911report/chapter-3.txt
392:technical/911report/chapter-5.txt
426:technical/911report/chapter-6.txt
460:technical/911report/chapter-7.txt
494:technical/911report/chapter-8.txt
528:technical/911report/chapter-9.txt
```

Explaination:

The command-line option `-b` for `grep` outputs the search results and provides the number of rows per line of results. It is helpful because it support to search special word and point its position out.

<br>

### Example 2:
Code: 
```
grep -i "CHAPTER" findName.txt
```

Output:
```
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
```

Explaination:

The function of the command-line option `-i` for `grep` is very similar to `-iname` for `find` that it can search for context by specific input and ignore case. It is helpful beacause we always capitalize the first word of a sentence, the normal search will make some data be lost.


### Example 3:
Code: 
```
grep -c "chapter" findName.txt
```

Output:
```
16
```

Explaination:

The command-line option `-c` for `grep` counts the number of the searched word appear and print it out. It is really helpful when we do not want to know the exactly content of the searched word, and we can get the number of it appear in an easy way.








