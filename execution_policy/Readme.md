# Parallel STL std::execution policy

The execution_policy example shows a simple benchmark.

* GCC requires TBB library (`dnf install tbb-devel` or `apt install libtbb-dev`)
* oneAPI uses oneTBB library

Performance seen with:

GCC 11.5 (Linux, TBB)

```
Method        Speed Ratio (vs. sequential)
Sequential     1.00
Parallel       23.50
Par_Unseq      31.33
Unseq          1.00
```

GCC 14.2 (Windows, TBB)

```
Sequential     1.00
Parallel       2.90
Par_Unseq      3.05
Unseq          0.97
```

Linux NVHPC 24.11 (-stdpar=multicore):

```
Sequential     1.00
Parallel       3.69
Par_Unseq      8.43
Unseq          0.98
```

Linux oneAPI 2025.0 (TBB):

```
Sequential     1.00
Parallel       8.43
Par_Unseq      29.50
Unseq          0.98
```

Windows oneAPI 2025.0 (TBB):

```
Sequential     1.00
Parallel       3.19
Par_Unseq      3.00
Unseq          1.05
```
