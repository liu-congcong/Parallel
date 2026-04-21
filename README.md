# Parallel

Run some commands in parallel.

## Usage

```text
parallel v1.1.2
Run some commands in parallel.
https://github.com/liu-congcong/parallel

Usage:
  parallel [options]

Options:
  -c    Commands to run
        Use #i to refer to the i-th parameter in a single run
        Lines starting with "# " will be ignored
  -p    List of parameters
        Use commas to separate multiple parameters in a single run
  -P    File contains a list of parameters
        Each line represents a single run, with multiple parameters separated by commas
        Lines starting with "#" will be ignored
  -q    Maximum number of commands in the queue (default: 1000000)
  -t    Number of threads (default: 1)
  -d    Print commands only
  -v    Set verbose output level (default: 0):
        0: Suppress both stdout and stderr
        1: Output stdout only
        2: Output stderr only
        3: Output both stdout and stderr
```

```text
parallel -t 3 -c "sleep #1" -p 2 2 2 2 2 2
parallel -t 1 -c "echo #1, #2" -p Hello,world -v
```
