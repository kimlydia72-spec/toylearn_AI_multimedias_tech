```
~ $ cd Commands/ && pwd
/home/node/Commands
~/Commands $ mkdir test && ls -l
total 4
drwxr-sr-x    2 node     node          4096 Nov  7 03:42 test
~/Commands $ mkdir notes && cd notes/ && pwd
/home/node/Commands/notes
~/Commands/notes $ cd ../
~/Commands $ mkdir -p images videos docs && ls -l
total 20
drwxr-sr-x    2 node     node          4096 Nov  7 03:46 docs
drwxr-sr-x    2 node     node          4096 Nov  7 03:46 images
drwxr-sr-x    2 node     node          4096 Nov  7 03:43 notes
drwxr-sr-x    2 node     node          4096 Nov  7 03:42 test
drwxr-sr-x    2 node     node          4096 Nov  7 03:46 videos
~/Commands $ cd docs && cd ../ && ls -l
total 20
drwxr-sr-x    2 node     node          4096 Nov  7 03:46 docs
drwxr-sr-x    2 node     node          4096 Nov  7 03:46 images
drwxr-sr-x    2 node     node          4096 Nov  7 03:43 notes
drwxr-sr-x    2 node     node          4096 Nov  7 03:42 test
drwxr-sr-x    2 node     node          4096 Nov  7 03:46 videos
~/Commands $ 
```