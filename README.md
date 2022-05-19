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
In contrast to a scalar processor, which can execute at most one single instruction per clock cycle, a superscalar processor can execute more than one instruction during a clock cycle by simultaneously dispatching multiple instructions to different execution units on the processor

### Properties    
- 6-stage pipeline (fetch-decode-dispatch-execute-finish-complete)
- Fetches Multiple Instructions at Once
- Register Renaming
- Reservation Station
- Reorder Buffer
- Out-of-Order Execution
- In-order Dispatch and Completion

### Dependencies
- g++

### Usage
```
g++ super-scalar.cpp -o super-scalar
./super-scalar
```

## Output
Files Output.txt, ODache.txt and ORF.txt will be generated in the output directory i.e. output/
- Output.txt will contain the stats of the execution.
- ODache.txt will contain the final data cache.
- ORF.txt will contain the final register file.