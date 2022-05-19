# Super Scalar Pipelined Processor
This code simulates a [Super Scalar Pipelined processor](https://en.wikipedia.org/wiki/Superscalar_processor). A superscalar processor is a CPU that implements a form of parallelism called instruction-level parallelism within a single processor. In contrast to a scalar processor, which can execute at most one single instruction per clock cycle, a superscalar processor can execute more than one instruction during a clock cycle by simultaneously dispatching multiple instructions to different execution units on the processor.

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