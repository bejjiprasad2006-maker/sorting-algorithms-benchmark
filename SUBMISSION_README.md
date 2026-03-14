# Sorting Algorithms Benchmarking - Submission Guide

This package contains the source code and benchmarking tools used for the CS-253 Practical Assignment.

## Project Structure
- `sorting_algorithms/`: C implementations of all 7 sorting algorithms and Quick Sort variants.
- `benchmark.py`: The main Python script that automates compilation, execution, and data analysis.
- `generate_test_data.py`: Script used to generate the random, sorted, and reverse-sorted datasets.
- `test_data/`: Directory containing the pre-generated input files.
- `graphs/`: (Generated after running) Contains the CSV results and visualization plots.

## Prerequisites
- **C Compiler**: `gcc` (MinGW for Windows or standard GCC for Linux/macOS).
- **Python 3.x**: With the following libraries installed:
  ```bash
  pip install matplotlib pandas numpy scipy
  ```

## How to Run the Benchmarks
1. **Navigate to the project directory**:
   ```bash
   cd Sorting-algorithms-benchmark
   ```
2. **Generate Test Data** (Optional, if not already present):
   ```bash
   python generate_test_data.py
   ```
3. **Run the Benchmark**:
   ```bash
   python benchmark.py
   ```
   *Note: The script will automatically compile the C files into an `executables/` folder and run them against the data in `test_data/`.*

4. **View Results**:
   - Numerical data will be saved in `graphs/csv_data/`.
   - Visualization plots will be available in `graphs/7_sorting_algo_comparisons/` and `graphs/quick_sort_analysis/`.

## Authors
- Ganala Durga Prasad (241CS124)
- Ala vishwajith (241CS106)

---

### Terminal Output

```
PS C:\Users\Durga Prasad\OneDrive\Desktop\practicals\sorting-algorithms-benchmark> python .\benchmark.py
Compiling sorting_algorithms\bubble_sort.c...
Successfully compiled sorting_algorithms\bubble_sort.c to executables\bubble_sort
Compiling sorting_algorithms\heap_sort.c...
Successfully compiled sorting_algorithms\heap_sort.c to executables\heap_sort
Compiling sorting_algorithms\insertion_sort.c...
Successfully compiled sorting_algorithms\insertion_sort.c to executables\insertion_sort
Compiling sorting_algorithms\merge_sort.c...
Successfully compiled sorting_algorithms\merge_sort.c to executables\merge_sort
Compiling sorting_algorithms\quick_sort_median_of_three_pivot.c...
Successfully compiled sorting_algorithms\quick_sort_median_of_three_pivot.c to executables\quick_sort_median_of_three_pivot
Compiling sorting_algorithms\radix_sort.c...
Successfully compiled sorting_algorithms\radix_sort.c to executables\radix_sort
Compiling sorting_algorithms\selection_sort.c...
Successfully compiled sorting_algorithms\selection_sort.c to executables\selection_sort
Compiling sorting_algorithms\quick_sort_first_pivot.c...
Successfully compiled sorting_algorithms\quick_sort_first_pivot.c to executables\quick_sort_first_pivot
Compiling sorting_algorithms\quick_sort_median_of_three_pivot.c...
Successfully compiled sorting_algorithms\quick_sort_median_of_three_pivot.c to executables\quick_sort_median_of_three_pivot
Compiling sorting_algorithms\quick_sort_random_pivot.c...
Successfully compiled sorting_algorithms\quick_sort_random_pivot.c to executables\quick_sort_random_pivot

Starting benchmarking...
Benchmarking N=100, Type=random...
  bubble_sort: Time = 0.000000 s, Comparisons = 4914
  heap_sort: Time = 0.000000 s, Comparisons = 1026
  insertion_sort: Time = 0.000000 s, Comparisons = 2705
  merge_sort: Time = 0.000000 s, Comparisons = 538
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 765
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 601
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 765
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 722
Benchmarking N=100, Type=reverse_sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 4950
  heap_sort: Time = 0.000000 s, Comparisons = 944
  insertion_sort: Time = 0.000000 s, Comparisons = 4950
  merge_sort: Time = 0.000000 s, Comparisons = 316
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 868
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 4950
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 868
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 597
Benchmarking N=100, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 99
  heap_sort: Time = 0.000000 s, Comparisons = 1081
  insertion_sort: Time = 0.000000 s, Comparisons = 99
  merge_sort: Time = 0.000000 s, Comparisons = 356
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 669
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 4950
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 669
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 598
Benchmarking N=500, Type=random...
  bubble_sort: Time = 0.000571 s, Comparisons = 124560
  heap_sort: Time = 0.000000 s, Comparisons = 7364
  insertion_sort: Time = 0.000000 s, Comparisons = 66406
  merge_sort: Time = 0.000000 s, Comparisons = 3866
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 4969
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000000 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 4708
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 4969
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 5476
Benchmarking N=500, Type=reverse_sorted...
  bubble_sort: Time = 0.000143 s, Comparisons = 124750
  heap_sort: Time = 0.000000 s, Comparisons = 7010
  insertion_sort: Time = 0.001143 s, Comparisons = 124750
  merge_sort: Time = 0.000000 s, Comparisons = 2216
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 6790
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000000 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000143 s, Comparisons = 124750
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 6790
  quick_sort_random_pivot: Time = 0.000143 s, Comparisons = 4859
Benchmarking N=500, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 499
  heap_sort: Time = 0.000000 s, Comparisons = 7756
  insertion_sort: Time = 0.000000 s, Comparisons = 499
  merge_sort: Time = 0.000000 s, Comparisons = 2272
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 4263
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000000 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 124750
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 4263
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 4887
Benchmarking N=1000, Type=random...
  bubble_sort: Time = 0.001714 s, Comparisons = 498275
  heap_sort: Time = 0.000000 s, Comparisons = 16861
  insertion_sort: Time = 0.000143 s, Comparisons = 238589
  merge_sort: Time = 0.000000 s, Comparisons = 8723
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 11035
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.000143 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 11276
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 11035
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 10482
Benchmarking N=1000, Type=reverse_sorted...
  bubble_sort: Time = 0.002714 s, Comparisons = 499500
  heap_sort: Time = 0.000000 s, Comparisons = 15965
  insertion_sort: Time = 0.002429 s, Comparisons = 499500
  merge_sort: Time = 0.000000 s, Comparisons = 4932
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 15849
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.001286 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.002571 s, Comparisons = 499500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 15849
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 10341
Benchmarking N=1000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 999
  heap_sort: Time = 0.000000 s, Comparisons = 17583
  insertion_sort: Time = 0.000000 s, Comparisons = 999
  merge_sort: Time = 0.000000 s, Comparisons = 5044
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 9520
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.000286 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.002143 s, Comparisons = 499500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 9520
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 11076
Benchmarking N=5000, Type=random...
  bubble_sort: Time = 0.029571 s, Comparisons = 12495355
  heap_sort: Time = 0.001857 s, Comparisons = 107681
  insertion_sort: Time = 0.012286 s, Comparisons = 6201418
  merge_sort: Time = 0.000000 s, Comparisons = 55201
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 69555
  radix_sort: Time = 0.000286 s, Comparisons = 4999
  selection_sort: Time = 0.026143 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 70105
  quick_sort_median_of_three_pivot: Time = 0.001000 s, Comparisons = 69555
  quick_sort_random_pivot: Time = 0.000429 s, Comparisons = 67272
Benchmarking N=5000, Type=reverse_sorted...
  bubble_sort: Time = 0.034714 s, Comparisons = 12497500
  heap_sort: Time = 0.000429 s, Comparisons = 103227
  insertion_sort: Time = 0.026429 s, Comparisons = 12497500
  merge_sort: Time = 0.000000 s, Comparisons = 29804
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 106182
  radix_sort: Time = 0.000857 s, Comparisons = 4999
  selection_sort: Time = 0.024143 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.027429 s, Comparisons = 12497500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 106182
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 67575
Benchmarking N=5000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 4999
  heap_sort: Time = 0.001429 s, Comparisons = 112126
  insertion_sort: Time = 0.000000 s, Comparisons = 4999
  merge_sort: Time = 0.000000 s, Comparisons = 32004
  quick_sort_median_of_three_pivot: Time = 0.000286 s, Comparisons = 60678
  radix_sort: Time = 0.000429 s, Comparisons = 4999
  selection_sort: Time = 0.028143 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.026000 s, Comparisons = 12497500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 60678
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 73502
Benchmarking N=10000, Type=random...
  bubble_sort: Time = 0.138000 s, Comparisons = 49981959
  heap_sort: Time = 0.001571 s, Comparisons = 235343
  insertion_sort: Time = 0.049000 s, Comparisons = 24900959
  merge_sort: Time = 0.002286 s, Comparisons = 120522
  quick_sort_median_of_three_pivot: Time = 0.000714 s, Comparisons = 153931
  radix_sort: Time = 0.001143 s, Comparisons = 9999
  selection_sort: Time = 0.079714 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.001714 s, Comparisons = 149274
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 153931
  quick_sort_random_pivot: Time = 0.001000 s, Comparisons = 164042
Benchmarking N=10000, Type=reverse_sorted...
  bubble_sort: Time = 0.121571 s, Comparisons = 49995000
  heap_sort: Time = 0.002857 s, Comparisons = 226682
  insertion_sort: Time = 0.102286 s, Comparisons = 49995000
  merge_sort: Time = 0.000571 s, Comparisons = 64608
  quick_sort_median_of_three_pivot: Time = 0.000857 s, Comparisons = 234923
  radix_sort: Time = 0.000429 s, Comparisons = 9999
  selection_sort: Time = 0.088857 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.101286 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 234923
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 149003
Benchmarking N=10000, Type=sorted...
Benchmarking N=10000, Type=reverse_sorted...
  bubble_sort: Time = 0.121571 s, Comparisons = 49995000
  heap_sort: Time = 0.002857 s, Comparisons = 226682
  insertion_sort: Time = 0.102286 s, Comparisons = 49995000
  merge_sort: Time = 0.000571 s, Comparisons = 64608
  quick_sort_median_of_three_pivot: Time = 0.000857 s, Comparisons = 234923
  radix_sort: Time = 0.000429 s, Comparisons = 9999
  selection_sort: Time = 0.088857 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.101286 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 234923
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 149003
Benchmarking N=10000, Type=sorted...
  merge_sort: Time = 0.000571 s, Comparisons = 64608
  quick_sort_median_of_three_pivot: Time = 0.000857 s, Comparisons = 234923
  radix_sort: Time = 0.000429 s, Comparisons = 9999
  selection_sort: Time = 0.088857 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.101286 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 234923
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 149003
Benchmarking N=10000, Type=sorted...
  quick_sort_median_of_three_pivot: Time = 0.000857 s, Comparisons = 234923
  radix_sort: Time = 0.000429 s, Comparisons = 9999
  selection_sort: Time = 0.088857 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.101286 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 234923
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 149003
Benchmarking N=10000, Type=sorted...
  radix_sort: Time = 0.000429 s, Comparisons = 9999
  selection_sort: Time = 0.088857 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.101286 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 234923
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 149003
Benchmarking N=10000, Type=sorted...
  quick_sort_first_pivot: Time = 0.101286 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 234923
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 149003
Benchmarking N=10000, Type=sorted...
Benchmarking N=10000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 9999
  heap_sort: Time = 0.001429 s, Comparisons = 244460
  insertion_sort: Time = 0.000000 s, Comparisons = 9999
  merge_sort: Time = 0.000429 s, Comparisons = 69008
  quick_sort_median_of_three_pivot: Time = 0.001429 s, Comparisons = 131343
  radix_sort: Time = 0.001714 s, Comparisons = 9999
  selection_sort: Time = 0.085714 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.091000 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000429 s, Comparisons = 131343
  quick_sort_random_pivot: Time = 0.001714 s, Comparisons = 151649
Benchmarking N=25000, Type=random...
  bubble_sort: Time = 1.126286 s, Comparisons = 312476622
  heap_sort: Time = 0.004571 s, Comparisons = 654560
  insertion_sort: Time = 0.338571 s, Comparisons = 156511617
  merge_sort: Time = 0.004571 s, Comparisons = 334203
  quick_sort_median_of_three_pivot: Time = 0.001571 s, Comparisons = 414956
  radix_sort: Time = 0.001571 s, Comparisons = 24999
  selection_sort: Time = 0.576143 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.002429 s, Comparisons = 452171
  quick_sort_median_of_three_pivot: Time = 0.001714 s, Comparisons = 414956
  quick_sort_random_pivot: Time = 0.002714 s, Comparisons = 432063
Benchmarking N=25000, Type=reverse_sorted...
  bubble_sort: Time = 0.764286 s, Comparisons = 312487500
  heap_sort: Time = 0.004143 s, Comparisons = 633719
  insertion_sort: Time = 0.669714 s, Comparisons = 312487500
  merge_sort: Time = 0.004429 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 660758
  merge_sort: Time = 0.004571 s, Comparisons = 334203
  quick_sort_median_of_three_pivot: Time = 0.001571 s, Comparisons = 414956
  radix_sort: Time = 0.001571 s, Comparisons = 24999
  selection_sort: Time = 0.576143 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.002429 s, Comparisons = 452171
  quick_sort_median_of_three_pivot: Time = 0.001714 s, Comparisons = 414956
  quick_sort_random_pivot: Time = 0.002714 s, Comparisons = 432063
Benchmarking N=25000, Type=reverse_sorted...
  bubble_sort: Time = 0.764286 s, Comparisons = 312487500
  heap_sort: Time = 0.004143 s, Comparisons = 633719
  insertion_sort: Time = 0.669714 s, Comparisons = 312487500
  merge_sort: Time = 0.004429 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 660758
  selection_sort: Time = 0.576143 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.002429 s, Comparisons = 452171
  quick_sort_median_of_three_pivot: Time = 0.001714 s, Comparisons = 414956
  quick_sort_random_pivot: Time = 0.002714 s, Comparisons = 432063
Benchmarking N=25000, Type=reverse_sorted...
  bubble_sort: Time = 0.764286 s, Comparisons = 312487500
  heap_sort: Time = 0.004143 s, Comparisons = 633719
  insertion_sort: Time = 0.669714 s, Comparisons = 312487500
  merge_sort: Time = 0.004429 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 660758
  quick_sort_random_pivot: Time = 0.002714 s, Comparisons = 432063
Benchmarking N=25000, Type=reverse_sorted...
  bubble_sort: Time = 0.764286 s, Comparisons = 312487500
  heap_sort: Time = 0.004143 s, Comparisons = 633719
  insertion_sort: Time = 0.669714 s, Comparisons = 312487500
  merge_sort: Time = 0.004429 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 660758
  bubble_sort: Time = 0.764286 s, Comparisons = 312487500
  heap_sort: Time = 0.004143 s, Comparisons = 633719
  insertion_sort: Time = 0.669714 s, Comparisons = 312487500
  merge_sort: Time = 0.004429 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 660758
  insertion_sort: Time = 0.669714 s, Comparisons = 312487500
  merge_sort: Time = 0.004429 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 660758
  merge_sort: Time = 0.004429 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 660758
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 660758
  radix_sort: Time = 0.003286 s, Comparisons = 24999
  selection_sort: Time = 0.591286 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.731143 s, Comparisons = 312487500
  quick_sort_median_of_three_pivot: Time = 0.001714 s, Comparisons = 660758
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 414025
Benchmarking N=25000, Type=sorted...
  bubble_sort: Time = 0.000286 s, Comparisons = 24999
  heap_sort: Time = 0.003286 s, Comparisons = 677688
  insertion_sort: Time = 0.000000 s, Comparisons = 24999
  merge_sort: Time = 0.002000 s, Comparisons = 188476
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 366397
  radix_sort: Time = 0.000571 s, Comparisons = 24999
  selection_sort: Time = 0.638857 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.600714 s, Comparisons = 312487500
  quick_sort_median_of_three_pivot: Time = 0.000714 s, Comparisons = 366397
  quick_sort_random_pivot: Time = 0.001143 s, Comparisons = 444941
Benchmarking N=50000, Type=random...
  bubble_sort: Time = 5.260571 s, Comparisons = 1249925230
  heap_sort: Time = 0.008857 s, Comparisons = 1409784
  insertion_sort: Time = 1.389286 s, Comparisons = 623471392
  merge_sort: Time = 0.010571 s, Comparisons = 718070
  quick_sort_median_of_three_pivot: Time = 0.006000 s, Comparisons = 895518
  radix_sort: Time = 0.003000 s, Comparisons = 49999
  selection_sort: Time = 6.049714 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 0.007143 s, Comparisons = 976163
  quick_sort_median_of_three_pivot: Time = 0.003714 s, Comparisons = 895518
  quick_sort_random_pivot: Time = 0.007714 s, Comparisons = 941985
Benchmarking N=50000, Type=reverse_sorted...
  bubble_sort: Time = 3.445143 s, Comparisons = 1249975000
  heap_sort: Time = 0.007000 s, Comparisons = 1366047








  quick_sort_random_pivot: Time = 0.007714 s, Comparisons = 941985
Benchmarking N=50000, Type=reverse_sorted...
  bubble_sort: Time = 3.445143 s, Comparisons = 1249975000
  heap_sort: Time = 0.007000 s, Comparisons = 1366047


  quick_sort_random_pivot: Time = 0.007714 s, Comparisons = 941985
Benchmarking N=50000, Type=reverse_sorted...
  bubble_sort: Time = 3.445143 s, Comparisons = 1249975000
  quick_sort_random_pivot: Time = 0.007714 s, Comparisons = 941985
Benchmarking N=50000, Type=reverse_sorted...
  bubble_sort: Time = 3.445143 s, Comparisons = 1249975000
  heap_sort: Time = 0.007000 s, Comparisons = 1366047
  insertion_sort: Time = 2.510571 s, Comparisons = 1249975000
  merge_sort: Time = 0.003286 s, Comparisons = 382512
  quick_sort_median_of_three_pivot: Time = 0.006143 s, Comparisons = 1433133
  radix_sort: Time = 0.002429 s, Comparisons = 49999
  selection_sort: Time = 2.502571 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 2.849714 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.001000 s, Comparisons = 1433133
  quick_sort_random_pivot: Time = 0.002000 s, Comparisons = 934485
Benchmarking N=50000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 49999
  heap_sort: Time = 0.006571 s, Comparisons = 1455438
  insertion_sort: Time = 0.000000 s, Comparisons = 49999
  merge_sort: Time = 0.005286 s, Comparisons = 401952
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 782782
  radix_sort: Time = 0.001143 s, Comparisons = 49999
  selection_sort: Time = 2.608714 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 2.591857 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.001857 s, Comparisons = 782782
  quick_sort_random_pivot: Time = 0.003286 s, Comparisons = 933743
Benchmarking N=75000, Type=random...
  bubble_sort: Time = 12.290286 s, Comparisons = 2812454372
  heap_sort: Time = 0.012857 s, Comparisons = 2200668
  insertion_sort: Time = 2.710286 s, Comparisons = 1407599583
  merge_sort: Time = 0.011571 s, Comparisons = 1121213
  quick_sort_median_of_three_pivot: Time = 0.005143 s, Comparisons = 1361888
  radix_sort: Time = 0.003429 s, Comparisons = 74999
  selection_sort: Time = 5.119571 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 0.007286 s, Comparisons = 1461763
  quick_sort_median_of_three_pivot: Time = 0.004000 s, Comparisons = 1361888
  quick_sort_random_pivot: Time = 0.010286 s, Comparisons = 1471572
Benchmarking N=75000, Type=reverse_sorted...
  bubble_sort: Time = 6.726429 s, Comparisons = 2812462500
  heap_sort: Time = 0.009714 s, Comparisons = 2138650
  insertion_sort: Time = 5.377143 s, Comparisons = 2812462500
  merge_sort: Time = 0.009571 s, Comparisons = 594612
  quick_sort_median_of_three_pivot: Time = 0.003000 s, Comparisons = 2272487
  radix_sort: Time = 0.003857 s, Comparisons = 74999
  selection_sort: Time = 5.156143 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 5.986571 s, Comparisons = 2812462500
  quick_sort_median_of_three_pivot: Time = 0.005714 s, Comparisons = 2272487
  quick_sort_random_pivot: Time = 0.004143 s, Comparisons = 1471042
Benchmarking N=75000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 74999
  heap_sort: Time = 0.006429 s, Comparisons = 2268087
  insertion_sort: Time = 0.000429 s, Comparisons = 74999
  merge_sort: Time = 0.009857 s, Comparisons = 624316
  quick_sort_median_of_three_pivot: Time = 0.001714 s, Comparisons = 1195642
  radix_sort: Time = 0.003857 s, Comparisons = 74999
  selection_sort: Time = 5.198571 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 5.047857 s, Comparisons = 2812462500
  quick_sort_median_of_three_pivot: Time = 0.005571 s, Comparisons = 1195642
  quick_sort_random_pivot: Time = 0.003429 s, Comparisons = 1446837
Benchmarking N=100000, Type=random...
  bubble_sort: Time = 21.618429 s, Comparisons = 4999912872
  heap_sort: Time = 0.020571 s, Comparisons = 3019435
  insertion_sort: Time = 6.544143 s, Comparisons = 2496913910
  merge_sort: Time = 0.027571 s, Comparisons = 1536083
  quick_sort_median_of_three_pivot: Time = 0.009857 s, Comparisons = 1871871
  radix_sort: Time = 0.004286 s, Comparisons = 99999
  selection_sort: Time = 9.175286 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 0.010429 s, Comparisons = 2075281
  quick_sort_median_of_three_pivot: Time = 0.008000 s, Comparisons = 1871871
  quick_sort_random_pivot: Time = 0.010857 s, Comparisons = 2171456
Benchmarking N=100000, Type=reverse_sorted...
  bubble_sort: Time = 11.762143 s, Comparisons = 4999950000
  heap_sort: Time = 0.013857 s, Comparisons = 2926640
  insertion_sort: Time = 11.499286 s, Comparisons = 4999950000
  merge_sort: Time = 0.014857 s, Comparisons = 815024
  quick_sort_median_of_three_pivot: Time = 0.009571 s, Comparisons = 3107283
  radix_sort: Time = 0.007714 s, Comparisons = 99999
  selection_sort: Time = 13.471429 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 16.343429 s, Comparisons = 4999950000
  quick_sort_median_of_three_pivot: Time = 0.009571 s, Comparisons = 3107283
  quick_sort_random_pivot: Time = 0.013714 s, Comparisons = 2090027
Benchmarking N=100000, Type=sorted...
  bubble_sort: Time = 0.000143 s, Comparisons = 99999
  heap_sort: Time = 0.017857 s, Comparisons = 3112517
  insertion_sort: Time = 0.000000 s, Comparisons = 99999
  merge_sort: Time = 0.015714 s, Comparisons = 853904
  quick_sort_median_of_three_pivot: Time = 0.003714 s, Comparisons = 1665551
  radix_sort: Time = 0.007857 s, Comparisons = 99999
  selection_sort: Time = 10.595000 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 9.327857 s, Comparisons = 4999950000
  quick_sort_median_of_three_pivot: Time = 0.008000 s, Comparisons = 1665551
  quick_sort_random_pivot: Time = 0.007714 s, Comparisons = 2042424

Benchmarking complete. Generating plots...
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_average_case_(random_input)_case_time.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_average_case_(random_input)_case_time_log_scale.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_worst_case_(reverse_sorted_input)_case_time.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_worst_case_(reverse_sorted_input)_case_time_log_scale.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_best_case_(sorted_input)_case_time.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_best_case_(sorted_input)_case_time_log_scale.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_average_case_(random_input)_case_comparisons.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_average_case_(random_input)_case_comparisons_log_scale.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_worst_case_(reverse_sorted_input)_case_comparisons.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_worst_case_(reverse_sorted_input)_case_comparisons_log_scale.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_best_case_(sorted_input)_case_comparisons.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_best_case_(sorted_input)_case_comparisons_log_scale.png
Generated correlation plot: graphs\7_sorting_algo_comparisons\time_vs_comparisons_correlation.png

Generating QuickSort variant plots...
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_average_case_(random_input)_case_time.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_average_case_(random_input)_case_time_log_scale.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_worst_case_(reverse_sorted_input)_case_time.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_worst_case_(reverse_sorted_input)_case_time_log_scale.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_best_case_(sorted_input)_case_time.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_best_case_(sorted_input)_case_time_log_scale.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_average_case_(random_input)_case_comparisons.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_average_case_(random_input)_case_comparisons_log_scale.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_worst_case_(reverse_sorted_input)_case_comparisons.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_worst_case_(reverse_sorted_input)_case_comparisons_log_scale.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_best_case_(sorted_input)_case_comparisons.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_best_case_(sorted_input)_case_comparisons_log_scale.png
Generated correlation plot: graphs\quick_sort_analysis\time_vs_comparisons_correlation.png

All plots generated successfully.
Results are in the 'graphs' directory.
  - 7 sorting algorithm comparisons: 'graphs\7_sorting_algo_comparisons'
  - Quick sort analysis: 'graphs\quick_sort_analysis'
  - CSV data: 'graphs\csv_data'

--- Benchmarking Methodology ---
Each experiment was repeated 7 times, and the average execution time is reported.
Timing mechanism: C's `clock()` function from <time.h> is used to measure algorithm execution time.
Comparison counting: Instrumented C code tracks all element comparisons.
Input selection: Pre-generated test data from the 'test_data/' directory was used.
Same inputs were used for all sorting algorithms to ensure a fair comparison.

Note on Best/Worst Case Definitions:
  - Average Case: Represented by 'random' input data.
  - Worst Case: Represented by 'reverse_sorted' input data.
  - Best Case: Represented by 'sorted' input data.

Correlation Analysis:
  The correlation plots show the relationship between the number of comparisons
  and execution time. A high correlation (close to 1.0) indicates that comparisons
  are a strong predictor of execution time for that algorithm.

--- Benchmarking Results Table ---
                   Algorithm     Input Type  Input Size (N) Average Time (s) Average Comparisons
                 Bubble Sort         Random             100         0.000000                4914
                   Heap Sort         Random             100         0.000000                1026
              Insertion Sort         Random             100         0.000000                2705
                  Merge Sort         Random             100         0.000000                 538
Quick Sort (Median of Three)         Random             100         0.000000                 765
                  Radix Sort         Random             100         0.000000                  99
              Selection Sort         Random             100         0.000000                4950
                 Bubble Sort Reverse Sorted             100         0.000000                4950
                   Heap Sort Reverse Sorted             100         0.000000                 944
              Insertion Sort Reverse Sorted             100         0.000000                4950
                  Merge Sort Reverse Sorted             100         0.000000                 316
Quick Sort (Median of Three) Reverse Sorted             100         0.000000                 868
                  Radix Sort Reverse Sorted             100         0.000000                  99
              Selection Sort Reverse Sorted             100         0.000000                4950
                 Bubble Sort         Sorted             100         0.000000                  99
                   Heap Sort         Sorted             100         0.000000                1081
              Insertion Sort         Sorted             100         0.000000                  99
                  Merge Sort         Sorted             100         0.000000                 356
Quick Sort (Median of Three)         Sorted             100         0.000000                 669
                  Radix Sort         Sorted             100         0.000000                  99
              Selection Sort         Sorted             100         0.000000                4950
                 Bubble Sort         Random             500         0.000571              124560
                   Heap Sort         Random             500         0.000000                7364
              Insertion Sort         Random             500         0.000000               66406
                  Merge Sort         Random             500         0.000000                3866
Quick Sort (Median of Three)         Random             500         0.000000                4969
                  Radix Sort         Random             500         0.000000                 499
              Selection Sort         Random             500         0.000000              124750
                 Bubble Sort Reverse Sorted             500         0.000143              124750
                   Heap Sort Reverse Sorted             500         0.000000                7010
              Insertion Sort Reverse Sorted             500         0.001143              124750
                  Merge Sort Reverse Sorted             500         0.000000                2216
Quick Sort (Median of Three) Reverse Sorted             500         0.000000                6790
                  Radix Sort Reverse Sorted             500         0.000000                 499
              Selection Sort Reverse Sorted             500         0.000000              124750
                 Bubble Sort         Sorted             500         0.000000                 499
                   Heap Sort         Sorted             500         0.000000                7756
              Insertion Sort         Sorted             500         0.000000                 499
                  Merge Sort         Sorted             500         0.000000                2272
Quick Sort (Median of Three)         Sorted             500         0.000000                4263
                  Radix Sort         Sorted             500         0.000000                 499
              Selection Sort         Sorted             500         0.000000              124750
                 Bubble Sort         Random            1000         0.001714              498275
                   Heap Sort         Random            1000         0.000000               16861
              Insertion Sort         Random            1000         0.000143              238589
                  Merge Sort         Random            1000         0.000000                8723
Quick Sort (Median of Three)         Random            1000         0.000000               11035
                  Radix Sort         Random            1000         0.000000                 999
              Selection Sort         Random            1000         0.000143              499500
                 Bubble Sort Reverse Sorted            1000         0.002714              499500
                   Heap Sort Reverse Sorted            1000         0.000000               15965
              Insertion Sort Reverse Sorted            1000         0.002429              499500
                  Merge Sort Reverse Sorted            1000         0.000000                4932
Quick Sort (Median of Three) Reverse Sorted            1000         0.000000               15849
                  Radix Sort Reverse Sorted            1000         0.000000                 999
              Selection Sort Reverse Sorted            1000         0.001286              499500
                 Bubble Sort         Sorted            1000         0.000000                 999
                   Heap Sort         Sorted            1000         0.000000               17583
              Insertion Sort         Sorted            1000         0.000000                 999
                  Merge Sort         Sorted            1000         0.000000                5044
Quick Sort (Median of Three)         Sorted            1000         0.000000                9520
                  Radix Sort         Sorted            1000         0.000000                 999
              Selection Sort         Sorted            1000         0.000286              499500
                 Bubble Sort         Random            5000         0.029571            12495355
                   Heap Sort         Random            5000         0.001857              107681
              Insertion Sort         Random            5000         0.012286             6201418
                  Merge Sort         Random            5000         0.000000               55201
Quick Sort (Median of Three)         Random            5000         0.000143               69555
                  Radix Sort         Random            5000         0.000286                4999
              Selection Sort         Random            5000         0.026143            12497500
                 Bubble Sort Reverse Sorted            5000         0.034714            12497500
                   Heap Sort Reverse Sorted            5000         0.000429              103227
              Insertion Sort Reverse Sorted            5000         0.026429            12497500
                  Merge Sort Reverse Sorted            5000         0.000000               29804
Quick Sort (Median of Three) Reverse Sorted            5000         0.000000              106182
                  Radix Sort Reverse Sorted            5000         0.000857                4999
              Selection Sort Reverse Sorted            5000         0.024143            12497500
                 Bubble Sort         Sorted            5000         0.000000                4999
                   Heap Sort         Sorted            5000         0.001429              112126
              Insertion Sort         Sorted            5000         0.000000                4999
                  Merge Sort         Sorted            5000         0.000000               32004
Quick Sort (Median of Three)         Sorted            5000         0.000286               60678
                  Radix Sort         Sorted            5000         0.000429                4999
              Selection Sort         Sorted            5000         0.028143            12497500
                 Bubble Sort         Random           10000         0.138000            49981959
                   Heap Sort         Random           10000         0.001571              235343
              Insertion Sort         Random           10000         0.049000            24900959
                  Merge Sort         Random           10000         0.002286              120522
Quick Sort (Median of Three)         Random           10000         0.000714              153931
                  Radix Sort         Random           10000         0.001143                9999
              Selection Sort         Random           10000         0.079714            49995000
                 Bubble Sort Reverse Sorted           10000         0.121571            49995000
                   Heap Sort Reverse Sorted           10000         0.002857              226682
              Insertion Sort Reverse Sorted           10000         0.102286            49995000
                  Merge Sort Reverse Sorted           10000         0.000571               64608
Quick Sort (Median of Three) Reverse Sorted           10000         0.000857              234923
                  Radix Sort Reverse Sorted           10000         0.000429                9999
              Selection Sort Reverse Sorted           10000         0.088857            49995000
                 Bubble Sort         Sorted           10000         0.000000                9999
                   Heap Sort         Sorted           10000         0.001429              244460
              Insertion Sort         Sorted           10000         0.000000                9999
                  Merge Sort         Sorted           10000         0.000429               69008
Quick Sort (Median of Three)         Sorted           10000         0.001429              131343
                  Radix Sort         Sorted           10000         0.001714                9999
              Selection Sort         Sorted           10000         0.085714            49995000
                 Bubble Sort         Random           25000         1.126286           312476622
                   Heap Sort         Random           25000         0.004571              654560
              Insertion Sort         Random           25000         0.338571           156511617
                  Merge Sort         Random           25000         0.004571              334203
Quick Sort (Median of Three)         Random           25000         0.001571              414956
                  Radix Sort         Random           25000         0.001571               24999
              Selection Sort         Random           25000         0.576143           312487500
                 Bubble Sort Reverse Sorted           25000         0.764286           312487500
                   Heap Sort Reverse Sorted           25000         0.004143              633719
              Insertion Sort Reverse Sorted           25000         0.669714           312487500
                  Merge Sort Reverse Sorted           25000         0.004429              178756
Quick Sort (Median of Three) Reverse Sorted           25000         0.001286              660758
                  Radix Sort Reverse Sorted           25000         0.003286               24999
              Selection Sort Reverse Sorted           25000         0.591286           312487500
                 Bubble Sort         Sorted           25000         0.000286               24999
                   Heap Sort         Sorted           25000         0.003286              677688
              Insertion Sort         Sorted           25000         0.000000               24999
                  Merge Sort         Sorted           25000         0.002000              188476
Quick Sort (Median of Three)         Sorted           25000         0.000571              366397
                  Radix Sort         Sorted           25000         0.000571               24999
              Selection Sort         Sorted           25000         0.638857           312487500
                 Bubble Sort         Random           50000         5.260571          1249925230
                   Heap Sort         Random           50000         0.008857             1409784
              Insertion Sort         Random           50000         1.389286           623471392
                  Merge Sort         Random           50000         0.010571              718070
Quick Sort (Median of Three)         Random           50000         0.006000              895518
                  Radix Sort         Random           50000         0.003000               49999
              Selection Sort         Random           50000         6.049714          1249975000
                 Bubble Sort Reverse Sorted           50000         3.445143          1249975000
                   Heap Sort Reverse Sorted           50000         0.007000             1366047
              Insertion Sort Reverse Sorted           50000         2.510571          1249975000
                  Merge Sort Reverse Sorted           50000         0.003286              382512
Quick Sort (Median of Three) Reverse Sorted           50000         0.006143             1433133
                  Radix Sort Reverse Sorted           50000         0.002429               49999
              Selection Sort Reverse Sorted           50000         2.502571          1249975000
                 Bubble Sort         Sorted           50000         0.000000               49999
                   Heap Sort         Sorted           50000         0.006571             1455438
              Insertion Sort         Sorted           50000         0.000000               49999
                  Merge Sort         Sorted           50000         0.005286              401952
Quick Sort (Median of Three)         Sorted           50000         0.001286              782782
                  Radix Sort         Sorted           50000         0.001143               49999
              Selection Sort         Sorted           50000         2.608714          1249975000
                 Bubble Sort         Random           75000        12.290286          2812454372
                   Heap Sort         Random           75000         0.012857             2200668
              Insertion Sort         Random           75000         2.710286          1407599583
                  Merge Sort         Random           75000         0.011571             1121213
Quick Sort (Median of Three)         Random           75000         0.005143             1361888
                  Radix Sort         Random           75000         0.003429               74999
              Selection Sort         Random           75000         5.119571          2812462500
                 Bubble Sort Reverse Sorted           75000         6.726429          2812462500
                   Heap Sort Reverse Sorted           75000         0.009714             2138650
              Insertion Sort Reverse Sorted           75000         5.377143          2812462500
                  Merge Sort Reverse Sorted           75000         0.009571              594612
Quick Sort (Median of Three) Reverse Sorted           75000         0.003000             2272487
                  Radix Sort Reverse Sorted           75000         0.003857               74999
              Selection Sort Reverse Sorted           75000         5.156143          2812462500
                 Bubble Sort         Sorted           75000         0.000000               74999
                   Heap Sort         Sorted           75000         0.006429             2268087
              Insertion Sort         Sorted           75000         0.000429               74999
                  Merge Sort         Sorted           75000         0.009857              624316
Quick Sort (Median of Three)         Sorted           75000         0.001714             1195642
                  Radix Sort         Sorted           75000         0.003857               74999
              Selection Sort         Sorted           75000         5.198571          2812462500
                 Bubble Sort         Random          100000        21.618429          4999912872
                   Heap Sort         Random          100000         0.020571             3019435
              Insertion Sort         Random          100000         6.544143          2496913910
                  Merge Sort         Random          100000         0.027571             1536083
Quick Sort (Median of Three)         Random          100000         0.009857             1871871
                  Radix Sort         Random          100000         0.004286               99999
              Selection Sort         Random          100000         9.175286          4999950000
                 Bubble Sort Reverse Sorted          100000        11.762143          4999950000
                   Heap Sort Reverse Sorted          100000         0.013857             2926640
              Insertion Sort Reverse Sorted          100000        11.499286          4999950000
                  Merge Sort Reverse Sorted          100000         0.014857              815024
Quick Sort (Median of Three) Reverse Sorted          100000         0.009571             3107283
                  Radix Sort Reverse Sorted          100000         0.007714               99999
              Selection Sort Reverse Sorted          100000        13.471429          4999950000
                 Bubble Sort         Sorted          100000         0.000143               99999
                   Heap Sort         Sorted          100000         0.017857             3112517
              Insertion Sort         Sorted          100000         0.000000               99999
                  Merge Sort         Sorted          100000         0.015714              853904
Quick Sort (Median of Three)         Sorted          100000         0.003714             1665551
                  Radix Sort         Sorted          100000         0.007857               99999
              Selection Sort         Sorted          100000        10.595000          4999950000

Full results table saved to graphs\csv_data\all_sorting_benchmark_results.csv

--- Correlation Analysis Summary ---
Algorithm                           | Correlation (r) | P-value
----------------------------------------------------------------------
Bubble Sort                         |          0.9514 | 2.6773e-14
Heap Sort                           |          0.9595 | 2.8490e-15
Insertion Sort                      |          0.9942 | 8.8371e-26
Merge Sort                          |          0.9698 | 7.8421e-17
Quick Sort (Median of Three)        |          0.8620 | 7.5784e-09
Radix Sort                          |          0.9171 | 1.7690e-11
Selection Sort                      |          0.9672 | 2.1298e-16

Interpretation:
  r close to 1.0: Strong positive correlation (more comparisons → more time)
  r close to 0.0: Weak/no correlation
  p-value < 0.05: Statistically significant correlation

================================================================================
IMPORTANT NOTES ON RESULTS
================================================================================

⚠️  TIMING MEASUREMENT:
  - Timing is measured INSIDE C code using clock() from <time.h>
  - The clock() function measures CPU time used by the program
  - Python is only used to run the executable and collect results
  - This avoids Python subprocess overhead affecting algorithm timing

⚠️  RADIX SORT 'COMPARISONS' NOTE:
  - Radix sort is a NON-COMPARATIVE sorting algorithm
  - It does NOT use element comparisons (like other algorithms)
  - The 'comparisons' count represents operations in getMax() function
  - This value (~n) is NOT comparable to other algorithms' comparisons
  - Use TIME metric, not COMPARISONS, to evaluate radix sort performance

✓ EXPECTED BEHAVIOR:
  - O(n²) algorithms: Bubble, Insertion, Selection Sort
  - O(n log n) algorithms: Heap, Merge, Quick Sort
  - O(n+k) algorithm: Radix Sort (where k is key range)
  - Best case optimized: Bubble & Insertion sort show O(n) for sorted input
================================================================================