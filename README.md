# Pipelined Processor
This code simulates a Pipelined processor. Given data cache, instruction cache and register file, it can simulate the execution of instructions and give the final data cache, register file and stats.

There are 3 Versions of the processor:
1. Scalar Pipelined Processor
    - This is the simplest version of the processor. It has only one pipeline. It has no operand forwarding.
2. Scalar Pipelined Processor with Operand Forwarding
    - This is the simplest version of the processor. It has only one pipeline. It has operand forwarding.
3. Super Scalar Pipelined Processor
    - A superscalar processor can execute more than one instruction during a clock cycle by simultaneously dispatching multiple instructions to different execution units on the processor

### Additional Properties of the Super Scalar Processor
- 6-stage pipeline (fetch-decode-dispatch-execute-finish-complete)
- Fetches Multiple Instructions at Once
- Register Renaming
- Reservation Station
- Reorder Buffer
- Out-of-Order Execution
- In-order Dispatch and Completion

## Usage

### Scalar Pipelined Processor
```
g++ pipeline.cpp -o pipeline
./pipeline
```

### Scalar Pipelined Processor with Operand Forwarding
```
g++ pipeline_forwarding.cpp -o pipeline_forwarding
./pipeline_forwarding
```

### Super Scalar Pipelined Processor
```
g++ super-scalar.cpp -o super-scalar
./super-scalar
```

## Output
Files Output.txt, ODache.txt and ORF.txt will be generated in the output directory i.e. output/
- Output.txt will contain the stats of the execution.
- ODache.txt will contain the final data cache.
- ORF.txt will contain the final register file.