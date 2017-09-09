The script takes a list of hosts on the command line and generates a dot format
network topology of all the IPs encounted on the way. The dot renderer is then
run by ```make``` to create the SVG. For convenience I've listed the hosts in a
separate text file [hosts.txt](hosts.txt) which ```make``` expands. And rather
than running it manually I include it in a Jenkins nightly (just link to the
generated SVG in your workspace).
```bash
$ ./hosts2dot.sh github.com silobrighton.com
```
Render SVG with ```make```
```bash
$ make clean
$ make
```
View the SVG in a web browser
```bash

$ firefox example.svg
```
![](example.svg)
