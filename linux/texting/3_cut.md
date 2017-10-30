grep
============
**echo**

```shell
echo -e "this is a word\nnext line"
echo -E "this is a word\nnext line"
```

**grep**

```shell
grep -E "[a-z]+" filename
egrep "[a-z]+" filename
```
```shell
grep -v match_pattern file
```
```shell
# only the number of matching lines
grep -c "text" filename

# To count the number of matching items
echo -e "1 2 3 4\nhello\n5 6" | egrep -o "[0-9]" | wc -l
```

```shell
grep -bon qlik . -r --include *.java
grep "main()" . -r --exclude "README"
```

```shell
grep -l linux sample1.txt sample2.txt
```

```shell
echo hello world | grep -i "HELLO"
```

```shell
grep -e "pattern1" -e "pattern"
```

```shell
grep -f pattern_filesource_filename
```

```shell
grep "test" file* -lZ | xargs -0 rm
```

```shell
#!/bin/bash
# Filename: silent_grep.sh
# Desc: Testing whether a file contain a text or not

# $0 = silent_grep.sh
if [ $# -ne 2 ]; then
echo "Usage: $0 match_text filename"
exit 1
fi

match_text=$1
filename=$2
grep -q "$match_text" $filename

# $? is used to find the return value of the last executed command.
if [ $? -eq 0 ]; then
echo "The text exists in the file"
else
echo "Text does not exist in the file"
fi
```

```
seq 10 | grep 5 -A 3
seq 10 | grep 5 -B 3
seq 10 | grep 5 -C 3

```
