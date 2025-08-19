### Use a for loop when...
You need to perform a side effect.
You need to print output, modify a variable outside the loop, or append to a pre-existing list.
The logic is complex and requires if/elif/else, or multiple lines of code.
You need to debug the process step-by-step.
You want to iterate over something and don't need to return a new sequence.

### Use a generator expression when...				
You need to transform data into a new sequence.				
You want to create a new list or tuple without using a for loop and .append().				
The logic is simple and can be written in a single line.				
You are performing a calculation with a very large dataset and need to be memory-efficient.				
The result will be used by another function, like sum(), min(), or max().				
