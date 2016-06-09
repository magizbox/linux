# Shell

## Expression

```bash
a = 1;
b = "string";
c = [1, 2, "str", true, false];
a = 1 + 2;
b = a * 7;
c = "Con" ++ "cat";
d = c ++ b;
```


## Command

```bash
println("Hello world");
print("Hello");
println(" world");

java = "/usr/bin/java";
call(java, "-jar", "closure.jar");
```

## Conditional

```bash
a = 3;
if (a > 2) {
  println("Yes");
} else {
  println("No");
}
```

## Loop

```bash
// Fibonacci
n = 0;
i = 0;
j = 1;
while (n < 60) {
  k = i + j;
  i = j;
  j = k;
  n = n + 1;
  echo(k);
}
```

## Function

```bash
// Function call
function func1(p1, p2) {
  println(p1, p2);
}
func1("Hello", "World");

// Global and local variables
v1 = "Global V1";
v2 = "Global V2";
v3 = "Global V3";
function func2(p) {
  v1 = "Local " ++ p;
  println(v1);
  println(v2);
  global v3;
  v3 = "V3 Modified.";
}
func2("Var");
println(v1);
println(v3);

// Return value
function func3(num) {
  return num + 41;
}
func3(4);
println();
ret = func3(1);
println("Returned:", ret);
```

## Recursive

```bash
function fibonacci(num) {
  if (num == 0) {
    return 0;
  } else if (num == 1) {
    return 1;
  } else {
    return fibonacci(num - 2) + fibonacci(num - 1);
  }
}
fibonacci(5);
```

## File System

```bash
// List files
files = readdir();

// Test existence
if (exists("file1.txt")) {
  println("file1.txt exists.");
}

existence = exists("file2.txt");
if (existence) {
  println("file2.txt exists.");
}

if (!exists("file3.txt")) {
  println("file3.txt does not exist.");
}
```





[Batsh – A language that compiles to Bash and Windows Batch](http://batsh.org/)