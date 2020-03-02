# afl-dyninst-mode
afl dyninst mode

## Install
1. Change DYN_ROOT to your installed Dynisnt folder
2. Copy the whole afl-dyninst-mode folder to the AFL folder
3. make && make install

## Usage
First, instrument target binary;

Second, set LD_LIBRARY_PATH and PATH:
```
$ export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/path/to/afl-dyninst
$ export PATH=$PATH:/path/to/afl-dyninst
```

Then, set env AFL_SKIP_BIN_CHECK: e.g.,
```
AFL_SKIP_BIN_CHECK=1  ./afl-fuzz -i /seed -o /output -t 500 -m 1G  -- /instrumented/target [params]
```