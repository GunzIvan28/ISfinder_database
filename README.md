### lastest fasta maybe in https://github.com/thanhleviet/ISfinder-sequences <br><br>
#### download database from http://www-genome.biotoul.fr
```
python3 ISfiner.step1.py  step1
python3 ISfiner.step2.py step1.IS.ID.list outdir
rm IS.database.tmp.fa
find outdir/ -type f -name 'IS*.seq.fa'|xargs -L 1 -I {} cat {} >> IS.database.tmp.fa
python3 check.empty.py IS.database.tmp.fa IS.database.fa
```
#### IS.database.fa is the fasta database of isfinder


#### python version dependence
python3

#### python3 package dependence
Biopython
BeautifulSoup
requests

