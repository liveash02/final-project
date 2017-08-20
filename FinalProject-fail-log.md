# Final Project- Fail Log

### 1. Getting my .txt files
##### What I did:
- I started by downloading the Shawville Equity newspaper, focusing on the years 1906, 1916, and 2006
- Performed:
```sh
liveash02@0ee73abc98e4:~$ cd equity
liveash02@0ee73abc98e4:~/equity$ pwd
/home/liveash02/equity
liveash02@0ee73abc98e4:~/equity$ mkdir equity2
liveash02@0ee73abc98e4:~/equity$ cd equity2
liveash02@0ee73abc98e4:~/equity/equity2$ wget http://collections.banq.qc.ca:8008/jrn03/equity/src/1906/ -A .txt -r --no-parent -nd -w 2 --limit-rate=20k
FINISHED 
Total wall clock time: 9m 3s
Downloaded: 117 files, 6.0M in 5m 3s (20.2 KB/s)
```
- I attempted to zip the folder containing the year 1906 to make downloading easier

```sh
liveash02@0ee73abc98e4:~/equity/equity2$ zip -r equity1906.zip equity2
        zip warning: name not matched: equity2
zip error: Nothing to do! (try: zip -r equity1906.zip . -i equity2)
liveash02@0ee73abc98e4:~/equity/equity2$ zip -r equity1906.zip . -i equity2
        zip warning: zip file empty
liveash02@0ee73abc98e4:~/equity/equity2$ ls
83471_1906-01-04.txt  83471_1906-03-01.txt  83471_1906-04-26.txt  83471_1906-06-21.txt  83471_1906-08-16.txt  83471_1906-10-11.txt  83471_1906-12-06.txt
83471_1906-01-11.txt  83471_1906-03-08.txt  83471_1906-05-03.txt  83471_1906-06-28.txt  83471_1906-08-23.txt  83471_1906-10-18.txt  83471_1906-12-13.txt
83471_1906-01-18.txt  83471_1906-03-15.txt  83471_1906-05-10.txt  83471_1906-07-05.txt  83471_1906-08-30.txt  83471_1906-10-25.txt  83471_1906-12-20.txt
83471_1906-01-25.txt  83471_1906-03-22.txt  83471_1906-05-17.txt  83471_1906-07-12.txt  83471_1906-09-06.txt  83471_1906-11-01.txt  83471_1906-12-27.txt
83471_1906-02-01.txt  83471_1906-03-29.txt  83471_1906-05-24.txt  83471_1906-07-19.txt  83471_1906-09-13.txt  83471_1906-11-08.txt
83471_1906-02-08.txt  83471_1906-04-05.txt  83471_1906-05-31.txt  83471_1906-07-26.txt  83471_1906-09-20.txt  83471_1906-11-15.txt
83471_1906-02-15.txt  83471_1906-04-12.txt  83471_1906-06-07.txt  83471_1906-08-02.txt  83471_1906-09-27.txt  83471_1906-11-22.txt
83471_1906-02-22.txt  83471_1906-04-19.txt  83471_1906-06-14.txt  83471_1906-08-09.txt  83471_1906-10-04.txt  83471_1906-11-29.txt
liveash02@0ee73abc98e4:~/equity/equity2$ zip -r equity1906.zip . -i equity2
        zip warning: zip file empty
```
- FAIL: I couldn't get the folder "equity2" to zip, so I guess I'll have to download each .txt file individually
- CORRECTION: Did some more searching on the [workbook][workb] and found that *"you can't zip a folder from the command line if you are in that folder, so cd out of it if necessary"*
- Performed:
```sh
liveash02@0ee73abc98e4:~$ cd equity
liveash02@0ee73abc98e4:~/equity$ zip -r equityfiles.zip equity2
  adding: equity2/ (stored 0%)
  adding: equity2/83471_1906-02-15.txt (deflated 46%)
  adding: equity2/83471_1906-06-07.txt (deflated 50%)
  adding: equity2/83471_1906-05-10.txt (deflated 45%)
  adding: equity2/83471_1906-10-25.txt (deflated 7%)
  adding: equity2/83471_1906-07-05.txt (deflated 49%)
  adding: equity2/83471_1906-11-15.txt (deflated 49%)
  adding: equity2/83471_1906-06-21.txt (deflated 46%)
  adding: equity2/83471_1906-09-13.txt (deflated 50%)
  adding: equity2/83471_1906-11-29.txt (deflated 48%)
  adding: equity2/83471_1906-08-23.txt (deflated 48%)
  adding: equity2/83471_1906-01-25.txt (deflated 46%)
  adding: equity2/83471_1906-08-30.txt (deflated 49%)
  adding: equity2/83471_1906-08-02.txt (deflated 49%)
  adding: equity2/83471_1906-10-11.txt (deflated 48%)
  adding: equity2/83471_1906-08-16.txt (deflated 49%)
  adding: equity2/83471_1906-11-08.txt (deflated 48%)
  adding: equity2/83471_1906-07-12.txt (deflated 50%)
  adding: equity2/83471_1906-12-13.txt (deflated 49%)
  adding: equity2/83471_1906-12-06.txt (deflated 48%)
  adding: equity2/83471_1906-09-06.txt (deflated 50%)
  adding: equity2/83471_1906-11-01.txt (deflated 48%)
  adding: equity2/83471_1906-04-26.txt (deflated 48%)
  adding: equity2/83471_1906-12-20.txt (deflated 48%)
  adding: equity2/83471_1906-02-01.txt (deflated 47%)
  adding: equity2/83471_1906-06-14.txt (deflated 7%)
  adding: equity2/83471_1906-04-19.txt (deflated 50%)
  adding: equity2/83471_1906-03-15.txt (deflated 47%)
  adding: equity2/83471_1906-02-22.txt (deflated 48%)
  adding: equity2/83471_1906-03-29.txt (deflated 46%)
  adding: equity2/83471_1906-03-22.txt (deflated 47%)
  adding: equity2/83471_1906-05-24.txt (deflated 49%)
  adding: equity2/83471_1906-07-19.txt (deflated 48%)
  adding: equity2/83471_1906-12-27.txt (deflated 49%)
  adding: equity2/83471_1906-10-04.txt (deflated 48%)
  adding: equity2/83471_1906-03-08.txt (deflated 48%)
  adding: equity2/83471_1906-07-26.txt (deflated 48%)
  adding: equity2/83471_1906-05-17.txt (deflated 52%)
  adding: equity2/83471_1906-04-12.txt (deflated 47%)
  adding: equity2/83471_1906-01-18.txt (deflated 44%)
  adding: equity2/83471_1906-08-09.txt (deflated 50%)
  adding: equity2/83471_1906-05-31.txt (deflated 7%)
  adding: equity2/83471_1906-01-11.txt (deflated 47%)
  adding: equity2/83471_1906-06-28.txt (deflated 49%)
  adding: equity2/83471_1906-10-18.txt (deflated 48%)
  adding: equity2/83471_1906-01-04.txt (deflated 7%)
  adding: equity2/83471_1906-05-03.txt (deflated 50%)
  adding: equity2/83471_1906-11-22.txt (deflated 49%)
  adding: equity2/83471_1906-09-20.txt (deflated 49%)
  adding: equity2/83471_1906-02-08.txt (deflated 47%)
  adding: equity2/83471_1906-04-05.txt (deflated 48%)
  adding: equity2/83471_1906-09-27.txt (deflated 48%)
  adding: equity2/83471_1906-03-01.txt (deflated 48%)
```

- Repeated this whole process again (downloaded the collection of that year and then zipped the folder) for the years 1916 and 2006
- I have 3 zip folders:
1. equityfiles.zip  (1906)
2. equityfiles2.zip (1916)
3. equityfiles3.zip (2006)
- I saved my history as 'dhbox-final-work.md' and 'dhbox-final-work2.md' and placed them in my Github repository called [liveash02/final-project][githubfp]

[workb]: <http://workbook.craftingdigitalhistory.ca/module-4/Exercises/>
[githubfp]: <https://github.com/liveash02/final-project> 

### 2. Getting the pdfs of the scanned newspaper articles
##### What I did:
- I went to the [site][site] with the articles sorted by year
- I looked through the year 1906 focusing on September (The Great Shawville Fire), 1916 focusing on February (the Parliament Buildings burned in Ottawa), and 2006 focusing on September again (100 years after the Great Fire). I downloaded these articles to use/reference in my StoryMap. 
- I saved the pdfs to my computer and to my [Github][githubfp]


[site]: <http://collections.banq.qc.ca:8008/jrn03/equity/src/> 

### 3. Attempting to clean the data
##### What I did:

- I was having issues with my .txt files and OCR. The data was looking messy and contained strange characters and symbols, things I didn't want to show up in my word cloud. I also knew this would take ages to manually edit the data therefore I thought of using DHBox. I mentioned the issue I was had to Professor Graham on [slack][slack]. I attempted to use his suggestion. 
- Performed: 

```sh
liveash02@0ee73abc98e4:~/equity$ cd equity2
liveash02@0ee73abc98e4:~/equity/equity2$ sed 's/[^\w\s]/ /g' 83471_1906-09-06.txt
```

- I got something that looked like this:
```sh
                         
                            
     �
                        
            s                
                                         s          w                 s                                    
    w  
      s   
                  
              �  
          
                                              
  �  �                   
 s        
         �
          
          
          
          
   s                              
          
        s                           s                                 
                
                   s    ss        s    s      w  
```

- I am not exactly sure if I was supposed to get this. I re-downloaded the "cleaned" 83471_1906-09-06.txt file and plugged it into [Lexos][lexos] to see if this improved my filtering. 
- FAIL: It did not. 
- I researched online and searched through [Module 3: Fixing Data][mod3] in our workbook to find other ways to filter the data and remove the special characters.
- Performed:
```sh
liveash02@0ee73abc98e4:~/equity/equity2$ tr -d '[[^:print:]\t]' < 83471_1906-09-06.txt
###PAGE###1###

Ne. 13. 24 Yea
8HAWVILLE, PONTIAC COUNTY,
QUE., THURSDAY, SEPTEMBER 6,
1 UX�
81.00 A YEAR IN ADVANCE.
The Mechas Bak of Caada.
If you could ake a look Io he hudeds of buel whch he gaduaes of ha eledld School of Commece
Oawa.
offces I
THE HARDWARE STORE
ESTABLISHED 1h�;4
$6,000,000
Coal (Auhozed) .. Caal (ad u) .. ..
H� � al Tded ofe
s.ooo.ooa
13,014.68�
8.05V, 274
THE WILLIS
$3,674,596
ca*L*A
Pesde, m  H. moauu a lea
l'KovDKx
Vce-Pesde, Joaha oo o, Esq E. E. 11KHDKN, Geeal Maage.
BUSINESS COLLEGE
ae makg a gad success of hemselves, you would le ohg hde you fom begg a
BOARD OK DIRECTORS
Geouk Hay, Pesde
Dav Ma L uKN,
Vce Pesde.
B* N. llae, Hob. Geo. H y so. H. K. Ega J. H.  ase, Joh Mahe. Des Muhy Geog.* II. Peley. M. 1\
Th, Bak ha� 114 Bache, aqd Ag�c<e. Abued houghou Oao, �uewe, Maoba
aqd ohe Noh-Wes Povces.
SAVINGS HANK DEPARTMENT.
Ieval a 3 e ce. j*  Aua allowed o Savg* Bak Deos�
Half* yealy.
Busess, Skobaod o Telegahy
Mllme�s Sules
Couse whou delay oe he yea oud, ad you may ee a ay me. Why o ow ?
We ae
B�lS, x. Geeal Maage
D. M. Fk, A a. Geeal Maage
Ime 4�del u P < �1
Ou caalogue gves full aculas
Sem fo *
A Geeal Hakg Busess Tasaced Fames� Busess Solced
INSPECTORS
C. G. Pe ock
______ W. Dhe.
Ffy-seve Offces I he Domo of Caada.
Coesodes  evey Bakg ow  < mada. ad houghou he wold.
Ths Bak gves om aeo o l hakg husles eused o I.
```

- I experimented with expressions in [RegExr][regx] while using some of the Equity text to test them.
- The expression *'([\w\d\s])\w+'* seemed to highlight everything I wanted to keep which was *'word, digit, whitespace'* and didn't highlight punctuation or characters. THIS IS GOOD.
- FAIL: I cannot figure out how to delete everything EXCEPT what is highlighted. I have googled everything from "regular expression cheat sheet" to "deleting characters in text files using command line" etc etc etc ETCCCCC, read other classmates faillogs, and combed over the workbook. HOURS LATER!
- The expression *'\bfire(s)?\b'* finds all instances of the word "fire". I also know that *'\W'*  (Not word) matches any character that is not a word character (alphanumeric & underscore). How am I to delete ONLY the characters and not the good words when the characters are filtered in with lines that have words. I could use the code from the REGEX exercises and put '~' before the lines with the characters (which seems like it would be EVERY line) but then how would I get dhbox command line to delete this. 
- Performed:
```sh
    3  sed -r -i.bak 's/[A-Za-z\w\d\s]/g' 83471_1906-08-16.txt
    4  sed 's/[\w\d\s]/ /g' 83471_1906-08-16.txt
    5  clear
    6  sed -r -i.bak 's/(\W) \n~ $&:\n\t/g' 83471_1906-02-08.txt
    7  sed -r -i.bak 's/(\W)/g' 83471_1906-02-08.txt
    8  sed 's/[\W]/ /g' 83471_1906-02-08.txt
```
- FAIL FAIL FAIL. ugh :(
- If I could do this class again, this is one area I would definitely spend more time in. It is such a crucial step in DH and I feel like the class didn't get to spend enough time experimently with the kinks of cleaning data. 
- Because I am having such difficulty cleaning the data and sorting through it, I am going to stick with looking at the scanned PDF articles of the newspaper for the years that I need.

[slack]: <https://hist3814o.slack.com/archives/C0GDSE1B8/p1502762595000170>
[lexos]: <http://lexos.wheatoncollege.edu/wordcloud>
[mod3]: <http://workbook.craftingdigitalhistory.ca/module-3/Exercises/#your-final-project>
[regx]: <http://regexr.com/>

### 4. Lexos
##### What I did:
- I went to [Lexos][lexos]
- Uploaded the following files: 83471_1906-09-13.txt and 83471_1906-09-20.txt
- I scrubbed the files using my stopWords.txt and keepWords.txt (located in my Github repository). I also removed all punctuation, made the text lowercase and removed digits. 
- I saved the word cloud as WordCloud-1906.png and put it into my Github repository
- I also recorded the word count for my keep words
- I repeated this process for 83471_1916-02-10.txt (after the Parliament fire)
- Then for 83471_2006-09-13.txt and 83471_2006-09-20.txt

### 5. Graphs
##### What I did:
- I went to [Online Chart Tool][oct] and created pie charts of the word counts
- Saved the charts to my Github repository

[oct]: <https://www.onlinecharttool.com/>

### 6. StoryMap
##### What I did:
- Added content to my Story Map titled "The Great Shawville Fire of 1906"
- Going to post this to my final project analysis
