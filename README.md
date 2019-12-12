# asciinema_statistics

**No longer maintained.**

A statistics page of [asciinema.org](https://asciinema.org/explore/public), visit [here](https://goreliu.github.io/asciinema_statistics/).

A screenshot:

![](https://raw.githubusercontent.com/wiki/goreliu/asciinema_statistics/images/screenshot.png)

## Tools

```
bin/update: pull new data from asciinema.org/explore/public and update index.html

bin/generate: generate index.html

bin/autoupdate: run bin/update every 600s

bin/playrandom: play a random asciinema cast from asciinema.org/explore/public in terminal

bin/savetosqlite: save data to a sqlite3 format database file(data/asciinema.db)

$ ./bin/savetosqlite
saved data to /home/goreliu/asciinema_statistics/data/asciinema.db
$ sqlite3 data/asciinema.db
SQLite version 3.28.0 2019-04-16 19:49:53
Enter ".help" for usage hints.
sqlite> .schema data
CREATE TABLE data (id int, os varchar(20), shell varchar(20), term varchar(50), user varchar(50));
sqlite> select count(*) from data where os = "Linux" and shell = "zsh";
3449
sqlite> select count(*) from data where os = "macOS" and shell = "zsh";
3265
```
