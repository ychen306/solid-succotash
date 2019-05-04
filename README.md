Prerequisite
* `nasm` should be in your path
* you should be able to run `perf stat ...` without issue (this tool only works on linux).

Usage:
1. put basic block you want to profile in `bb.nasm`. Right now we only support basic block written in intel syntax.
Alternatively, if you have binary of your basic block, you can edit `run_test.nasm` to include `bb.bin`, 
which should contains binary of your basic block (and that only -- `bb.bin` is not an object file
but a file containing the raw binary).
2. Do `./a64-out.sh <reps>`. Where `<reps>` is the number of iterations you want to run.
