    1  cd equity
    2  pwd
    3  mkdir equity2
    4  cd equity2
    5  wget http://collections.banq.qc.ca:8008/jrn03/equity/src/1906/ -A .txt -r --no-parent -nd -w 2 --limit-rate=20k
    6  zip -r equity1906.zip equity2
    7  zip -r equity1906.zip . -i equity2
    8  ls
    9  zip -r equity1906.zip . -i equity2
   10  cd equity
   11  cd liveash02
   12  history
   13  history > dhbox-final-work.md
