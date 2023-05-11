# Lab Report 3

# Researching the `find` Command

##  `-type` Command-Line Option

The `-type` command allows the user to search for files/directories by type. 

In this first codeblock, I searched for all the file types (`-type f`) in the directory I gave.
This is useful because it allows the user to only search for the *files* of a particular directory, which can get more specific if desired. 

```
[cs15lsp23ln@ieng6-202]:~:444$ find stringsearch/stringsearch-data/technical/911report/ -type f
stringsearch/stringsearch-data/technical/911report/chapter-1.txt
stringsearch/stringsearch-data/technical/911report/chapter-10.txt
stringsearch/stringsearch-data/technical/911report/chapter-11.txt
stringsearch/stringsearch-data/technical/911report/chapter-12.txt
stringsearch/stringsearch-data/technical/911report/chapter-13.1.txt
stringsearch/stringsearch-data/technical/911report/chapter-13.2.txt
stringsearch/stringsearch-data/technical/911report/chapter-13.3.txt
stringsearch/stringsearch-data/technical/911report/chapter-13.4.txt
stringsearch/stringsearch-data/technical/911report/chapter-13.5.txt
stringsearch/stringsearch-data/technical/911report/chapter-2.txt
stringsearch/stringsearch-data/technical/911report/chapter-3.txt
stringsearch/stringsearch-data/technical/911report/chapter-5.txt
stringsearch/stringsearch-data/technical/911report/chapter-6.txt
stringsearch/stringsearch-data/technical/911report/chapter-7.txt
stringsearch/stringsearch-data/technical/911report/chapter-8.txt
stringsearch/stringsearch-data/technical/911report/chapter-9.txt
stringsearch/stringsearch-data/technical/911report/preface.txt
[cs15lsp23ln@ieng6-202]:~:445$ 
```

In this second codeblock, I searched for all the directory types (`-type d`) in the directory I gave.
This is useful because it allows the user to only search for the *directories* of a particular path, which can get more specific if desired.

```
[cs15lsp23ln@ieng6-202]:~:445$ find stringsearch/ -type d
stringsearch/
stringsearch/.git
stringsearch/.git/branches
stringsearch/.git/info
stringsearch/.git/hooks
stringsearch/.git/refs
stringsearch/.git/refs/heads
stringsearch/.git/refs/tags
stringsearch/.git/refs/remotes
stringsearch/.git/refs/remotes/origin
stringsearch/.git/objects
stringsearch/.git/objects/pack
stringsearch/.git/objects/info
stringsearch/.git/logs
stringsearch/.git/logs/refs
stringsearch/.git/logs/refs/remotes
stringsearch/.git/logs/refs/remotes/origin
stringsearch/.git/logs/refs/heads
stringsearch/stringsearch-data
stringsearch/stringsearch-data/.git
stringsearch/stringsearch-data/.git/branches
stringsearch/stringsearch-data/.git/info
stringsearch/stringsearch-data/.git/hooks
stringsearch/stringsearch-data/.git/refs
stringsearch/stringsearch-data/.git/refs/heads
stringsearch/stringsearch-data/.git/refs/tags
stringsearch/stringsearch-data/.git/refs/remotes
stringsearch/stringsearch-data/.git/refs/remotes/origin
stringsearch/stringsearch-data/.git/objects
stringsearch/stringsearch-data/.git/objects/pack
stringsearch/stringsearch-data/.git/objects/info
stringsearch/stringsearch-data/.git/logs
stringsearch/stringsearch-data/.git/logs/refs
stringsearch/stringsearch-data/.git/logs/refs/remotes
stringsearch/stringsearch-data/.git/logs/refs/remotes/origin
stringsearch/stringsearch-data/.git/logs/refs/heads
stringsearch/stringsearch-data/technical
stringsearch/stringsearch-data/technical/911report
stringsearch/stringsearch-data/technical/biomed
stringsearch/stringsearch-data/technical/government
stringsearch/stringsearch-data/technical/government/About_LSC
stringsearch/stringsearch-data/technical/government/Alcohol_Problems
stringsearch/stringsearch-data/technical/government/Env_Prot_Agen
stringsearch/stringsearch-data/technical/government/Gen_Account_Office
stringsearch/stringsearch-data/technical/government/Media
stringsearch/stringsearch-data/technical/government/Post_Rate_Comm
stringsearch/stringsearch-data/technical/plos
[cs15lsp23ln@ieng6-202]:~:446$
```

(Source: ChatGPT. I asked "can you tell me some command-line options using the command -find in bash")


## `-maxdepth` Command-Line Option

The `-maxdepth` command allows the user to limit the depth of the search.

In this first codeblock, I only searched for the directories that had a max depth of 2 relative to `stringsearch`.
This is useful because it allows the user to only search for paths that weren't any deeper than desired, which can help searching for files/directories easier.

```
[cs15lsp23ln@ieng6-202]:~:446$ find stringsearch/ -maxdepth 2
stringsearch/
stringsearch/.git
stringsearch/.git/description
stringsearch/.git/branches
stringsearch/.git/info
stringsearch/.git/hooks
stringsearch/.git/refs
stringsearch/.git/objects
stringsearch/.git/HEAD
stringsearch/.git/config
stringsearch/.git/logs
stringsearch/.git/packed-refs
stringsearch/.git/index
stringsearch/Server.java
stringsearch/StringServer.java
stringsearch/words.txt
stringsearch/stringsearch-data
stringsearch/stringsearch-data/.git
stringsearch/stringsearch-data/technical
[cs15lsp23ln@ieng6-202]:~:447$
```

In this second codeblock, I only searched for the *text* files that had a max depth of 3 relative to `stringsearch`.
This is useful because it allows the user to only search for paths that weren't any deeper than desired and that had a specific name, making it easier to search for.

```
[cs15lsp23ln@ieng6-202]:~:447$ find stringsearch/ -maxdepth 3 -name "*.txt"
stringsearch/words.txt
[cs15lsp23ln@ieng6-202]:~:448$
```

(Source: ChatGPT. I asked "can you tell me some command-line options using the command -find in bash") 


## `-size` Command-Line Option

The `-size` command allows the user to search for files by size.

In this first codeblock, I searched for all files with a size of exactly 2 bytes. 
This is useful because it allows the user to quickly search for files of an exact size and determine if they want to keep them or not.

```
[cs15lsp23ln@ieng6-202]:~:448$ find stringsearch/stringsearch-data/technical/ -size 2b 
stringsearch/stringsearch-data/technical/plos/pmed.0020191.txt
stringsearch/stringsearch-data/technical/plos/pmed.0020226.txt
[cs15lsp23ln@ieng6-202]:~:449$
```

In this second codeblock, I searched for all files with a size of less than 3 kilobytes.
This is useful because it allows the user to quickly search for files of a maximum size and determine if they want to keep them or not.

```
[cs15lsp23ln@ieng6-202]:~:449$ find stringsearch/stringsearch-data/technical/ -size -3k
stringsearch/stringsearch-data/technical/government/Media/Campaign_Pays.txt
stringsearch/stringsearch-data/technical/government/Media/Court_Keeps_Judge_From.txt
stringsearch/stringsearch-data/technical/government/Media/Fire_Victims_Sue.txt
stringsearch/stringsearch-data/technical/government/Media/Helping_Hands.txt
stringsearch/stringsearch-data/technical/government/Media/It_Pays_to_Know.txt
stringsearch/stringsearch-data/technical/government/Media/Justice_requests.txt
stringsearch/stringsearch-data/technical/government/Media/Lawyer_Web_Survey.txt
stringsearch/stringsearch-data/technical/government/Media/Self-Help_Website.txt
stringsearch/stringsearch-data/technical/government/Media/Wilmington_lawyer.txt
stringsearch/stringsearch-data/technical/plos/pmed.0020028.txt
stringsearch/stringsearch-data/technical/plos/pmed.0020048.txt
stringsearch/stringsearch-data/technical/plos/pmed.0020082.txt
stringsearch/stringsearch-data/technical/plos/pmed.0020120.txt
stringsearch/stringsearch-data/technical/plos/pmed.0020157.txt
stringsearch/stringsearch-data/technical/plos/pmed.0020191.txt
stringsearch/stringsearch-data/technical/plos/pmed.0020192.txt
stringsearch/stringsearch-data/technical/plos/pmed.0020226.txt
[cs15lsp23ln@ieng6-202]:~:450$
```

(Source: ChatGPT. I asked "can you tell me some command-line options using the command -find in bash") 


## `-delete` Command-Line Option

The `-delete` command allows the user to delete all files or directories that match the search criteria.

In this first codeblock, I searched for all the *text* files within the `911report` directory and deleted them.
This is useful because it allows the user to remove an entire directory that they don't need, which also frees up disk space. 

*Before:*

```
[cs15lsp23ln@ieng6-202]:technical:456$ cd 911report/
[cs15lsp23ln@ieng6-202]:911report:457$ ls
chapter-1.txt   chapter-11.txt  chapter-13.1.txt  chapter-13.3.txt  chapter-13.5.txt  chapter-3.txt  chapter-6.txt  chapter-8.txt  preface.txt
chapter-10.txt  chapter-12.txt  chapter-13.2.txt  chapter-13.4.txt  chapter-2.txt     chapter-5.txt  chapter-7.txt  chapter-9.txt
[cs15lsp23ln@ieng6-202]:911report:458$
```

*After:*

```
[cs15lsp23ln@ieng6-202]:technical:459$ find 911report/ -name "*.txt" -delete
[cs15lsp23ln@ieng6-202]:technical:461$ cd 911report/
[cs15lsp23ln@ieng6-202]:911report:462$ ls
[cs15lsp23ln@ieng6-202]:911report:463$
```

In this second codeblock, I searched for all the files that started with `pmed` within the `plos` directory and deleted them.
This is useful because it allows the user to remove files that they don't need, which also frees up disk space. 
It also allows them to delete a group of files quickly by giving a specific criteria.

*Before:*

```
[cs15lsp23ln@ieng6-202]:technical:464$ cd plos/
[cs15lsp23ln@ieng6-202]:plos:465$ ls
journal.pbio.0020001.txt  journal.pbio.0020105.txt  journal.pbio.0020213.txt  journal.pbio.0020348.txt  journal.pbio.0030076.txt  pmed.0010036.txt  pmed.0010071.txt  pmed.0020045.txt  pmed.0020098.txt  pmed.0020160.txt  pmed.0020216.txt
journal.pbio.0020010.txt  journal.pbio.0020112.txt  journal.pbio.0020214.txt  journal.pbio.0020350.txt  journal.pbio.0030094.txt  pmed.0010039.txt  pmed.0020002.txt  pmed.0020047.txt  pmed.0020099.txt  pmed.0020161.txt  pmed.0020226.txt 
journal.pbio.0020012.txt  journal.pbio.0020113.txt  journal.pbio.0020215.txt  journal.pbio.0020353.txt  journal.pbio.0030097.txt  pmed.0010041.txt  pmed.0020005.txt  pmed.0020048.txt  pmed.0020102.txt  pmed.0020162.txt  pmed.0020231.txt 
journal.pbio.0020013.txt  journal.pbio.0020116.txt  journal.pbio.0020216.txt  journal.pbio.0020354.txt  journal.pbio.0030102.txt  pmed.0010042.txt  pmed.0020007.txt  pmed.0020050.txt  pmed.0020103.txt  pmed.0020180.txt  pmed.0020232.txt 
journal.pbio.0020019.txt  journal.pbio.0020121.txt  journal.pbio.0020223.txt  journal.pbio.0020394.txt  journal.pbio.0030105.txt  pmed.0010045.txt  pmed.0020009.txt  pmed.0020055.txt  pmed.0020104.txt  pmed.0020181.txt  pmed.0020235.txt 
journal.pbio.0020028.txt  journal.pbio.0020125.txt  journal.pbio.0020224.txt  journal.pbio.0020400.txt  journal.pbio.0030127.txt  pmed.0010046.txt  pmed.0020015.txt  pmed.0020059.txt  pmed.0020113.txt  pmed.0020182.txt  pmed.0020236.txt 
journal.pbio.0020035.txt  journal.pbio.0020127.txt  journal.pbio.0020228.txt  journal.pbio.0020401.txt  journal.pbio.0030129.txt  pmed.0010047.txt  pmed.0020016.txt  pmed.0020060.txt  pmed.0020114.txt  pmed.0020187.txt  pmed.0020237.txt 
journal.pbio.0020040.txt  journal.pbio.0020133.txt  journal.pbio.0020232.txt  journal.pbio.0020404.txt  journal.pbio.0030131.txt  pmed.0010048.txt  pmed.0020017.txt  pmed.0020061.txt  pmed.0020115.txt  pmed.0020189.txt  pmed.0020238.txt 
journal.pbio.0020042.txt  journal.pbio.0020140.txt  journal.pbio.0020241.txt  journal.pbio.0020406.txt  journal.pbio.0030136.txt  pmed.0010049.txt  pmed.0020018.txt  pmed.0020062.txt  pmed.0020116.txt  pmed.0020191.txt  pmed.0020239.txt 
journal.pbio.0020043.txt  journal.pbio.0020145.txt  journal.pbio.0020262.txt  journal.pbio.0020419.txt  journal.pbio.0030137.txt  pmed.0010050.txt  pmed.0020019.txt  pmed.0020065.txt  pmed.0020117.txt  pmed.0020192.txt  pmed.0020242.txt 
journal.pbio.0020046.txt  journal.pbio.0020146.txt  journal.pbio.0020263.txt  journal.pbio.0020420.txt  pmed.0010008.txt          pmed.0010051.txt  pmed.0020020.txt  pmed.0020067.txt  pmed.0020118.txt  pmed.0020194.txt  pmed.0020246.txt 
journal.pbio.0020047.txt  journal.pbio.0020147.txt  journal.pbio.0020267.txt  journal.pbio.0020430.txt  pmed.0010010.txt          pmed.0010052.txt  pmed.0020021.txt  pmed.0020068.txt  pmed.0020120.txt  pmed.0020195.txt  pmed.0020247.txt 
journal.pbio.0020052.txt  journal.pbio.0020148.txt  journal.pbio.0020272.txt  journal.pbio.0020431.txt  pmed.0010013.txt          pmed.0010056.txt  pmed.0020022.txt  pmed.0020071.txt  pmed.0020123.txt  pmed.0020196.txt  pmed.0020249.txt 
journal.pbio.0020053.txt  journal.pbio.0020150.txt  journal.pbio.0020276.txt  journal.pbio.0020439.txt  pmed.0010021.txt          pmed.0010058.txt  pmed.0020023.txt  pmed.0020073.txt  pmed.0020140.txt  pmed.0020197.txt  pmed.0020257.txt 
journal.pbio.0020054.txt  journal.pbio.0020156.txt  journal.pbio.0020297.txt  journal.pbio.0020440.txt  pmed.0010022.txt          pmed.0010060.txt  pmed.0020024.txt  pmed.0020074.txt  pmed.0020144.txt  pmed.0020198.txt  pmed.0020258.txt 
journal.pbio.0020063.txt  journal.pbio.0020161.txt  journal.pbio.0020302.txt  journal.pbio.0030021.txt  pmed.0010023.txt          pmed.0010061.txt  pmed.0020027.txt  pmed.0020075.txt  pmed.0020145.txt  pmed.0020200.txt  pmed.0020268.txt
journal.pbio.0020064.txt  journal.pbio.0020164.txt  journal.pbio.0020306.txt  journal.pbio.0030024.txt  pmed.0010024.txt          pmed.0010062.txt  pmed.0020028.txt  pmed.0020082.txt  pmed.0020146.txt  pmed.0020201.txt  pmed.0020272.txt 
journal.pbio.0020067.txt  journal.pbio.0020169.txt  journal.pbio.0020307.txt  journal.pbio.0030032.txt  pmed.0010025.txt          pmed.0010064.txt  pmed.0020033.txt  pmed.0020085.txt  pmed.0020148.txt  pmed.0020203.txt  pmed.0020273.txt 
journal.pbio.0020068.txt  journal.pbio.0020172.txt  journal.pbio.0020310.txt  journal.pbio.0030050.txt  pmed.0010026.txt          pmed.0010066.txt  pmed.0020034.txt  pmed.0020086.txt  pmed.0020149.txt  pmed.0020206.txt  pmed.0020274.txt 
journal.pbio.0020071.txt  journal.pbio.0020183.txt  journal.pbio.0020311.txt  journal.pbio.0030051.txt  pmed.0010028.txt          pmed.0010067.txt  pmed.0020035.txt  pmed.0020088.txt  pmed.0020150.txt  pmed.0020208.txt  pmed.0020275.txt 
journal.pbio.0020073.txt  journal.pbio.0020187.txt  journal.pbio.0020337.txt  journal.pbio.0030056.txt  pmed.0010029.txt          pmed.0010068.txt  pmed.0020036.txt  pmed.0020090.txt  pmed.0020155.txt  pmed.0020209.txt  pmed.0020278.txt 
journal.pbio.0020100.txt  journal.pbio.0020190.txt  journal.pbio.0020346.txt  journal.pbio.0030062.txt  pmed.0010030.txt          pmed.0010069.txt  pmed.0020039.txt  pmed.0020091.txt  pmed.0020157.txt  pmed.0020210.txt  pmed.0020281.txt 
journal.pbio.0020101.txt  journal.pbio.0020206.txt  journal.pbio.0020347.txt  journal.pbio.0030065.txt  pmed.0010034.txt          pmed.0010070.txt  pmed.0020040.txt  pmed.0020094.txt  pmed.0020158.txt  pmed.0020212.txt
[cs15lsp23ln@ieng6-202]:plos:466$
```

*After:*

```
[cs15lsp23ln@ieng6-202]:technical:467$ find plos/ -name "pmed.*" -delete
[cs15lsp23ln@ieng6-202]:technical:468$ cd plos/
[cs15lsp23ln@ieng6-202]:plos:469$ ls
journal.pbio.0020001.txt  journal.pbio.0020052.txt  journal.pbio.0020112.txt  journal.pbio.0020150.txt  journal.pbio.0020215.txt  journal.pbio.0020297.txt  journal.pbio.0020354.txt  journal.pbio.0030021.txt  journal.pbio.0030105.txt     
journal.pbio.0020010.txt  journal.pbio.0020053.txt  journal.pbio.0020113.txt  journal.pbio.0020156.txt  journal.pbio.0020216.txt  journal.pbio.0020302.txt  journal.pbio.0020394.txt  journal.pbio.0030024.txt  journal.pbio.0030127.txt     
journal.pbio.0020012.txt  journal.pbio.0020054.txt  journal.pbio.0020116.txt  journal.pbio.0020161.txt  journal.pbio.0020223.txt  journal.pbio.0020306.txt  journal.pbio.0020400.txt  journal.pbio.0030032.txt  journal.pbio.0030129.txt     
journal.pbio.0020013.txt  journal.pbio.0020063.txt  journal.pbio.0020121.txt  journal.pbio.0020164.txt  journal.pbio.0020224.txt  journal.pbio.0020307.txt  journal.pbio.0020401.txt  journal.pbio.0030050.txt  journal.pbio.0030131.txt     
journal.pbio.0020019.txt  journal.pbio.0020064.txt  journal.pbio.0020125.txt  journal.pbio.0020169.txt  journal.pbio.0020228.txt  journal.pbio.0020310.txt  journal.pbio.0020404.txt  journal.pbio.0030051.txt  journal.pbio.0030136.txt     
journal.pbio.0020028.txt  journal.pbio.0020067.txt  journal.pbio.0020127.txt  journal.pbio.0020172.txt  journal.pbio.0020232.txt  journal.pbio.0020311.txt  journal.pbio.0020406.txt  journal.pbio.0030056.txt  journal.pbio.0030137.txt     
journal.pbio.0020035.txt  journal.pbio.0020068.txt  journal.pbio.0020133.txt  journal.pbio.0020183.txt  journal.pbio.0020241.txt  journal.pbio.0020337.txt  journal.pbio.0020419.txt  journal.pbio.0030062.txt
journal.pbio.0020040.txt  journal.pbio.0020071.txt  journal.pbio.0020140.txt  journal.pbio.0020187.txt  journal.pbio.0020262.txt  journal.pbio.0020346.txt  journal.pbio.0020420.txt  journal.pbio.0030065.txt
journal.pbio.0020042.txt  journal.pbio.0020073.txt  journal.pbio.0020145.txt  journal.pbio.0020190.txt  journal.pbio.0020263.txt  journal.pbio.0020347.txt  journal.pbio.0020430.txt  journal.pbio.0030076.txt
journal.pbio.0020043.txt  journal.pbio.0020100.txt  journal.pbio.0020146.txt  journal.pbio.0020206.txt  journal.pbio.0020267.txt  journal.pbio.0020348.txt  journal.pbio.0020431.txt  journal.pbio.0030094.txt
journal.pbio.0020046.txt  journal.pbio.0020101.txt  journal.pbio.0020147.txt  journal.pbio.0020213.txt  journal.pbio.0020272.txt  journal.pbio.0020350.txt  journal.pbio.0020439.txt  journal.pbio.0030097.txt
journal.pbio.0020047.txt  journal.pbio.0020105.txt  journal.pbio.0020148.txt  journal.pbio.0020214.txt  journal.pbio.0020276.txt  journal.pbio.0020353.txt  journal.pbio.0020440.txt  journal.pbio.0030102.txt
[cs15lsp23ln@ieng6-202]:plos:470$
```

(Source: ChatGPT. I asked "can you tell me some command-line options using the command -find in bash") 

Website: https://keeanalbao.github.io/cse15l-lab-reports/lab3.html
