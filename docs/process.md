## Process

![](http://s3.10pm.com/wp-content/uploads/2015/1110/92521/how-linux-deals-with-frozen-applications-1.jpg)

### 1. Process Manager

List Process [^1]

```bash
# display Linux processes
top

# list process
ps -aux

# sort by CPU usage
top -o %CPU

# sort by memory usage
top -o %MEM
ps aux --sort -rss
top # then press M

# count process
ps -eaf | awk '{print $8}' | sort | uniq -c | sort -nr
```

Kill Process

```
# kill process by name
pkill firefox
```

### 2. Screen

```bash
# create new screen
screen -S [screen_name]

# list screen
screen -ls

# exit from screen
Ctrl-a d

# reattach a session
screen -r [screen_pid]

# delete a screen
screen -X -S [screen_pid] quit
```

[^1]: [Sorting down processes by memory usage](http://unix.stackexchange.com/questions/92493/sorting-down-processes-by-memory-usage)