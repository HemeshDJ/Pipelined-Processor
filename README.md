# Pipelined Processor
This code simulates a Pipelined processor. Given data cache, instruction cache and register file, it can simulate the execution of instructions and give the final data cache, register file and stats.

There are 3 Versions of the processor:
1. Pipelined Processor
2. Pipelined Processor with Operand Forwarding
3. Super Scalar Pipelined Processor

## Pipelined Processor

### Usage
```
g++ pipeline.cpp -o pipeline
./pipeline
```

## Pipelined Processor with Operand Forwarding

### Usage
```
g++ pipeline_forwarding.cpp -o pipeline_forwarding
./pipeline_forwarding
```

## Super Scalar Pipelined Processor

### Properties    
- 6-stage pipeline (fetch-decode-dispatch-execute-finish-complete)
- Fetches Multiple Instructions at Once
- Register Renaming
- Reservation Station
- Reorder Buffer
- Out-of-Order Execution
- In-order Dispatch and Completion

### Assumptions
- No fetching until Branch is resolved
- Execution of any operation in any Funcitonal Unit takes 1 cycle
- Any number of instructions can be dispatched from the dispatch buffer in a cycle

    **NOTE**: Instruction can be dispatched only if functional units are not busy

### Dependencies
- g++

### Usage
```
g++ super-scalar.cpp -o super-scalar
./super-scalar
```

### Output
Files Output.txt, ODache.txt and ORF.txt will be generated in the output directory i.e. output/
- Output.txt will contain the stats of the execution.
- ODache.txt will contain the final Dache.
- ORF.txt will contain the final RF.