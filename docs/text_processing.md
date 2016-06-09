# Text Processing & Pipeline

## tail, head, cat

```bash
# output last part
tail test.txt
tail -f test.txt

# output first part
head test.txt
head -n 100 test.txt

# concatenate files and print
cat test1.txt
cat test1.txt test2.text
```

## sort

```bash
# unique
sort -u test.txt
```

## wc

```bash
# newline, word and byte counts
wc -l test.txt
ps aux | grep apach2 | wc -l
```
