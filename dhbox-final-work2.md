    1  cd equity
    2  zip -r equityfiles.zip equity2
    3  mkdir equity3
    4  cd equity3
    5  history
    6  history > dhbox-final-work2.md
    7  clear
    8  cd equity
    9  cd -
   10  mkdir equity4
   11  cd equity4
   12  wget http://collections.banq.qc.ca:8008/jrn03/equity/src/2006/ -A .txt -r --no-parent -nd -w 2 --limit-rate=20k
   13  cd -
   14  zip -r equityfiles2.zip equity3
   15  zip -r equityfiles3.zip equity4
   16  history
   17  history > dhbox-final-work2.md
