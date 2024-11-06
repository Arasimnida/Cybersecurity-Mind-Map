The goal of the Fingerprint - pattern search Method is to search for relevant patterns in [[Memory]].

**Scan for sufficiently unique structure signatures**:
- [[PoolFinder]] parses [[Kernel]] pool memory (pre-allocated 4,000 memory pool pages)
- [[PTFinder]] works with [[EPROCESS]] and [[ETHREAD]] structs (_ DISPATCHER_HEADER)

**Perform basic [[Sanity checks]]** on data to weed out corrupt records, duplicates etc.

#methodology #forensics #memory #data-storage