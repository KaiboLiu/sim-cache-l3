# sim-cache-l3
implementation of L3 cache with SimpleScalar



## Bonus Points  
You need to modify the C/C++ source code in **sim-cache.c** file to add a third-level data cache
and a third-level instruction cache. After you modify the code, recompile it using command:  
  `make`  
you will get new simulation tool: "sim-cache" with extended functionality. You need to use the
two provided configuration files (cache_3a.cfg and cache_3b.cfg: also in the previous github
repository) on test-math to test if your implementation is correct. Use the command that is
similar to the following command.  
`./sim-cache -config cache_3a.cfg -redir:sim cache_3a.out ./test-math`



#### Hints:
**some related functions in sim-cache.c:**  
> sim_reg_options(struct opt_odb_t \*odb): /\* register simulator-specific options\*/  
> sim_check_options(...): /\* check simulator-specific option values \*/  
> sim_reg_stats(struct stat_sdb_t \*sdb): /\* register simulator-specific statistics \*/  
> dl1_access_fn(...): /\* l1 data cache l1 block miss handler function \*/  
> dl2_access_fn(...): /\* l2 data cache l2 block miss handler function \*/  
> il1_access_fn(...): /\*l1 inst cache l1 block miss handler function \*/  
> il2_access_fn(...): /\*l2 inst cache l2 block miss handler function \*/  
> sim_main(void):/\*start simulation, program loaded, processor precise state initialized \*/  


You should describe how to implement a level-3 instruction cache and a level-3 data cache in
SimpleScalar. You should also attach the modified source code : sim-cache.c, and mark the
place where you make modification. Run simulations using provided simulation configuration
file(cache_3a.cfg and cache_3b.cfg ), for each run you should submit one output file.
