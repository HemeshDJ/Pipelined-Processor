# Super Scalar Pipelined Processor
This code simulates a [Super Scalar Pipelined processor](https://en.wikipedia.org/wiki/Superscalar_processor). Given data cache, instruction cache and register file, it can simulate the execution of instructions and give the final data cache, register file and stats.

## Properties    
- 6-stage pipeline (fetch-decode-dispatch-execute-finish-complete)
- Fetches Multiple Instructions at Once
- Register Renaming
- Reservation Station
- Reorder Buffer
- Out-of-Order Execution
- In-order Dispatch and Completion

## Assumptions
- No fetching until Branch is resolved
- Execution of any operation in any Funcitonal Unit takes 1 cycle
- Any number of instructions can be dispatched from the dispatch buffer in a cycle

    **NOTE**: Instruction can be dispatched only if functional units are not busy

## Dependencies
- g++

## Input
- DCache.txt and ICache.txt (input cache files)
- Input Files to be placed in the input directory i.e. input/

## Usage
```
g++ super-scalar.cpp -o super-scalar
./super-scalar
```

## Output
Files Output.txt, ODache.txt and ORF.txt will be generated in the output directory i.e. output/
- Output.txt will contain the stats of the execution.
- ODache.txt will contain the final Dache.
- ORF.txt will contain the final RF.