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
- Marepalli Kowndinya Vasudev (241CS133)
- Narra Shanmukha Srida (241CS238)

---

### Terminal Output

```
PS C:\Users\M K Vasudev\OneDrive\Desktop\daa\Sorting-algorithms-benchmark> python benchmark.py
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
  bubble_sort: Time = 0.000000 s, Comparisons = 4884
  heap_sort: Time = 0.000000 s, Comparisons = 1031
  insertion_sort: Time = 0.000000 s, Comparisons = 2454
  merge_sort: Time = 0.000000 s, Comparisons = 540
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 713
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 610
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 713
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 599
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
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 607
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
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 791
Benchmarking N=500, Type=random...
  bubble_sort: Time = 0.000000 s, Comparisons = 124614
  heap_sort: Time = 0.000000 s, Comparisons = 7442
  insertion_sort: Time = 0.000000 s, Comparisons = 61497
  merge_sort: Time = 0.000000 s, Comparisons = 3871
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 5405
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000000 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 4876
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 5405
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 4736
Benchmarking N=500, Type=reverse_sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 124750
  heap_sort: Time = 0.000000 s, Comparisons = 7010
  insertion_sort: Time = 0.000000 s, Comparisons = 124750
  merge_sort: Time = 0.000000 s, Comparisons = 2216
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 6790
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000000 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 124750
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 6790
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 4713
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
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 4433
Benchmarking N=1000, Type=random...
  bubble_sort: Time = 0.000571 s, Comparisons = 499149
  heap_sort: Time = 0.000000 s, Comparisons = 16858
  insertion_sort: Time = 0.000000 s, Comparisons = 249333
  merge_sort: Time = 0.000000 s, Comparisons = 8697
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 11903
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.000000 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000286 s, Comparisons = 11455
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 11903
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 10711
Benchmarking N=1000, Type=reverse_sorted...
  bubble_sort: Time = 0.000429 s, Comparisons = 499500
  heap_sort: Time = 0.000000 s, Comparisons = 15965
  insertion_sort: Time = 0.000000 s, Comparisons = 499500
  merge_sort: Time = 0.000143 s, Comparisons = 4932
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 15849
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.000714 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 499500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 15849
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 10917
Benchmarking N=1000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 999
  heap_sort: Time = 0.000000 s, Comparisons = 17583
  insertion_sort: Time = 0.000000 s, Comparisons = 999
  merge_sort: Time = 0.000000 s, Comparisons = 5044
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 9520
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.000000 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 499500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 9520
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 10797
Benchmarking N=5000, Type=random...
  bubble_sort: Time = 0.021857 s, Comparisons = 12494650
  heap_sort: Time = 0.001286 s, Comparisons = 107687
  insertion_sort: Time = 0.006143 s, Comparisons = 6254150
  merge_sort: Time = 0.002143 s, Comparisons = 55182
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 69918
  radix_sort: Time = 0.000000 s, Comparisons = 4999
  selection_sort: Time = 0.014143 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 72391
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 69918
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 77451
Benchmarking N=5000, Type=reverse_sorted...
  bubble_sort: Time = 0.029571 s, Comparisons = 12497500
  heap_sort: Time = 0.000714 s, Comparisons = 103227
  insertion_sort: Time = 0.016000 s, Comparisons = 12497500
  merge_sort: Time = 0.000571 s, Comparisons = 29804
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 106182
  radix_sort: Time = 0.000000 s, Comparisons = 4999
  selection_sort: Time = 0.012857 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.016714 s, Comparisons = 12497500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 106182
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 68595
Benchmarking N=5000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 4999
  heap_sort: Time = 0.000571 s, Comparisons = 112126
  insertion_sort: Time = 0.000000 s, Comparisons = 4999
  merge_sort: Time = 0.001286 s, Comparisons = 32004
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 60678
  radix_sort: Time = 0.000000 s, Comparisons = 4999
  selection_sort: Time = 0.015143 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.008714 s, Comparisons = 12497500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 60678
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 67455
Benchmarking N=10000, Type=random...
  bubble_sort: Time = 0.112143 s, Comparisons = 49991172
  heap_sort: Time = 0.000286 s, Comparisons = 235317
  insertion_sort: Time = 0.029714 s, Comparisons = 24755456
  merge_sort: Time = 0.000571 s, Comparisons = 120419
  quick_sort_median_of_three_pivot: Time = 0.000286 s, Comparisons = 152945
  radix_sort: Time = 0.000000 s, Comparisons = 9999
  selection_sort: Time = 0.044429 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.001000 s, Comparisons = 159072
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 152945
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 152386
Benchmarking N=10000, Type=reverse_sorted...
  bubble_sort: Time = 0.105286 s, Comparisons = 49995000
  heap_sort: Time = 0.000286 s, Comparisons = 226682
  insertion_sort: Time = 0.060286 s, Comparisons = 49995000
  merge_sort: Time = 0.000000 s, Comparisons = 64608
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 234923
  radix_sort: Time = 0.000000 s, Comparisons = 9999
  selection_sort: Time = 0.043286 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.075571 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 234923
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 163068
Benchmarking N=10000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 9999
  heap_sort: Time = 0.000143 s, Comparisons = 244460
  insertion_sort: Time = 0.000000 s, Comparisons = 9999
  merge_sort: Time = 0.000000 s, Comparisons = 69008
  quick_sort_median_of_three_pivot: Time = 0.001143 s, Comparisons = 131343
  radix_sort: Time = 0.000000 s, Comparisons = 9999
  selection_sort: Time = 0.040571 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.034571 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 131343
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 151302
Benchmarking N=25000, Type=random...
  bubble_sort: Time = 0.935857 s, Comparisons = 312485420
  heap_sort: Time = 0.000000 s, Comparisons = 654862
  insertion_sort: Time = 0.175429 s, Comparisons = 156401077
  merge_sort: Time = 0.006000 s, Comparisons = 334016
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 412492
  radix_sort: Time = 0.000000 s, Comparisons = 24999
  selection_sort: Time = 0.253857 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 414750
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 412492
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 425432
Benchmarking N=25000, Type=reverse_sorted...
  bubble_sort: Time = 0.639429 s, Comparisons = 312487500
  heap_sort: Time = 0.000000 s, Comparisons = 633719
  insertion_sort: Time = 0.361429 s, Comparisons = 312487500
  merge_sort: Time = 0.001571 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 660758
  radix_sort: Time = 0.000000 s, Comparisons = 24999
  selection_sort: Time = 0.267143 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.479286 s, Comparisons = 312487500
  quick_sort_median_of_three_pivot: Time = 0.000286 s, Comparisons = 660758
  quick_sort_random_pivot: Time = 0.001571 s, Comparisons = 429984
Benchmarking N=25000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 24999
  heap_sort: Time = 0.000571 s, Comparisons = 677688
  insertion_sort: Time = 0.000000 s, Comparisons = 24999
  merge_sort: Time = 0.000857 s, Comparisons = 188476
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 366397
  radix_sort: Time = 0.000000 s, Comparisons = 24999
  selection_sort: Time = 0.248429 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.212429 s, Comparisons = 312487500
  quick_sort_median_of_three_pivot: Time = 0.000429 s, Comparisons = 366397
  quick_sort_random_pivot: Time = 0.000286 s, Comparisons = 425968
Benchmarking N=50000, Type=random...
  bubble_sort: Time = 4.018571 s, Comparisons = 1249938144
  heap_sort: Time = 0.006286 s, Comparisons = 1409800
  insertion_sort: Time = 0.718714 s, Comparisons = 625170165
  merge_sort: Time = 0.006857 s, Comparisons = 718063
  quick_sort_median_of_three_pivot: Time = 0.005714 s, Comparisons = 898746
  radix_sort: Time = 0.001000 s, Comparisons = 49999
  selection_sort: Time = 1.015000 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 0.010571 s, Comparisons = 956552
  quick_sort_median_of_three_pivot: Time = 0.010286 s, Comparisons = 898746
  quick_sort_random_pivot: Time = 0.006286 s, Comparisons = 923837
Benchmarking N=50000, Type=reverse_sorted...
  bubble_sort: Time = 2.565000 s, Comparisons = 1249975000
  heap_sort: Time = 0.009429 s, Comparisons = 1366047
  insertion_sort: Time = 1.440714 s, Comparisons = 1249975000
  merge_sort: Time = 0.013143 s, Comparisons = 382512
  quick_sort_median_of_three_pivot: Time = 0.000286 s, Comparisons = 1433133
  radix_sort: Time = 0.002286 s, Comparisons = 49999
  selection_sort: Time = 1.061000 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 1.953571 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.002143 s, Comparisons = 1433133
  quick_sort_random_pivot: Time = 0.004286 s, Comparisons = 912885
Benchmarking N=50000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 49999
  heap_sort: Time = 0.006429 s, Comparisons = 1455438
  insertion_sort: Time = 0.000000 s, Comparisons = 49999
  merge_sort: Time = 0.006714 s, Comparisons = 401952
  quick_sort_median_of_three_pivot: Time = 0.000714 s, Comparisons = 782782
  radix_sort: Time = 0.001857 s, Comparisons = 49999
  selection_sort: Time = 1.006000 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 0.903857 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.003143 s, Comparisons = 782782
  quick_sort_random_pivot: Time = 0.002143 s, Comparisons = 932883
Benchmarking N=75000, Type=random...
  bubble_sort: Time = 9.712857 s, Comparisons = 2812382300
  heap_sort: Time = 0.015143 s, Comparisons = 2200249
  insertion_sort: Time = 1.612857 s, Comparisons = 1405331415
  merge_sort: Time = 0.015714 s, Comparisons = 1121150
  quick_sort_median_of_three_pivot: Time = 0.007714 s, Comparisons = 1395028
  radix_sort: Time = 0.006143 s, Comparisons = 74999
  selection_sort: Time = 2.276714 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 0.009286 s, Comparisons = 1530324
  quick_sort_median_of_three_pivot: Time = 0.004571 s, Comparisons = 1395028
  quick_sort_random_pivot: Time = 0.008571 s, Comparisons = 1421120
Benchmarking N=75000, Type=reverse_sorted...
  bubble_sort: Time = 5.746286 s, Comparisons = 2812462500
  heap_sort: Time = 0.009714 s, Comparisons = 2138650
  insertion_sort: Time = 3.229714 s, Comparisons = 2812462500
  merge_sort: Time = 0.007429 s, Comparisons = 594612
  quick_sort_median_of_three_pivot: Time = 0.004000 s, Comparisons = 2272487
  radix_sort: Time = 0.006571 s, Comparisons = 74999
  selection_sort: Time = 2.366143 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 4.267714 s, Comparisons = 2812462500
  quick_sort_median_of_three_pivot: Time = 0.004857 s, Comparisons = 2272487
  quick_sort_random_pivot: Time = 0.003143 s, Comparisons = 1425833
Benchmarking N=75000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 74999
  heap_sort: Time = 0.005429 s, Comparisons = 2268087
  insertion_sort: Time = 0.000000 s, Comparisons = 74999
  merge_sort: Time = 0.009143 s, Comparisons = 624316
  quick_sort_median_of_three_pivot: Time = 0.001429 s, Comparisons = 1195642
  radix_sort: Time = 0.003286 s, Comparisons = 74999
  selection_sort: Time = 2.249714 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 1.926714 s, Comparisons = 2812462500
  quick_sort_median_of_three_pivot: Time = 0.001429 s, Comparisons = 1195642
  quick_sort_random_pivot: Time = 0.008571 s, Comparisons = 1514283
Benchmarking N=100000, Type=random...
  bubble_sort: Time = 16.655000 s, Comparisons = 4999949594
  heap_sort: Time = 0.014857 s, Comparisons = 3019575
  insertion_sort: Time = 2.849714 s, Comparisons = 2503572522
  merge_sort: Time = 0.019429 s, Comparisons = 1536493
  quick_sort_median_of_three_pivot: Time = 0.008714 s, Comparisons = 2032796
  radix_sort: Time = 0.005286 s, Comparisons = 99999
  selection_sort: Time = 4.076857 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 0.010143 s, Comparisons = 2129236
  quick_sort_median_of_three_pivot: Time = 0.006571 s, Comparisons = 2032796
  quick_sort_random_pivot: Time = 0.013857 s, Comparisons = 1989485
Benchmarking N=100000, Type=reverse_sorted...
  bubble_sort: Time = 10.262429 s, Comparisons = 4999950000
  heap_sort: Time = 0.014143 s, Comparisons = 2926640
  insertion_sort: Time = 5.681143 s, Comparisons = 4999950000
  merge_sort: Time = 0.012857 s, Comparisons = 815024
  quick_sort_median_of_three_pivot: Time = 0.007000 s, Comparisons = 3107283
  radix_sort: Time = 0.001714 s, Comparisons = 99999
  selection_sort: Time = 4.204857 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 7.619000 s, Comparisons = 4999950000
  quick_sort_median_of_three_pivot: Time = 0.005000 s, Comparisons = 3107283
  quick_sort_random_pivot: Time = 0.005143 s, Comparisons = 2051865
Benchmarking N=100000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 99999
  heap_sort: Time = 0.011429 s, Comparisons = 3112517
  insertion_sort: Time = 0.000000 s, Comparisons = 99999
  merge_sort: Time = 0.013143 s, Comparisons = 853904
  quick_sort_median_of_three_pivot: Time = 0.002143 s, Comparisons = 1665551
  radix_sort: Time = 0.000714 s, Comparisons = 99999
  selection_sort: Time = 4.012000 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 3.371143 s, Comparisons = 4999950000
  quick_sort_median_of_three_pivot: Time = 0.001857 s, Comparisons = 1665551
  quick_sort_random_pivot: Time = 0.002143 s, Comparisons = 1994289

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
                 Bubble Sort         Random             100         0.000000                4884
                   Heap Sort         Random             100         0.000000                1031
              Insertion Sort         Random             100         0.000000                2454
                  Merge Sort         Random             100         0.000000                 540
Quick Sort (Median of Three)         Random             100         0.000000                 713
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
                 Bubble Sort         Random             500         0.000000              124614
                   Heap Sort         Random             500         0.000000                7442
              Insertion Sort         Random             500         0.000000               61497
                  Merge Sort         Random             500         0.000000                3871
Quick Sort (Median of Three)         Random             500         0.000000                5405
                  Radix Sort         Random             500         0.000000                 499
              Selection Sort         Random             500         0.000000              124750
                 Bubble Sort Reverse Sorted             500         0.000000              124750
                   Heap Sort Reverse Sorted             500         0.000000                7010
              Insertion Sort Reverse Sorted             500         0.000000              124750
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
                 Bubble Sort         Random            1000         0.000571              499149
                   Heap Sort         Random            1000         0.000000               16858
              Insertion Sort         Random            1000         0.000000              249333
                  Merge Sort         Random            1000         0.000000                8697
Quick Sort (Median of Three)         Random            1000         0.000000               11903
                  Radix Sort         Random            1000         0.000000                 999
              Selection Sort         Random            1000         0.000000              499500
                 Bubble Sort Reverse Sorted            1000         0.000429              499500
                   Heap Sort Reverse Sorted            1000         0.000000               15965
              Insertion Sort Reverse Sorted            1000         0.000000              499500
                  Merge Sort Reverse Sorted            1000         0.000143                4932
Quick Sort (Median of Three) Reverse Sorted            1000         0.000000               15849
                  Radix Sort Reverse Sorted            1000         0.000000                 999
              Selection Sort Reverse Sorted            1000         0.000714              499500
                 Bubble Sort         Sorted            1000         0.000000                 999
                   Heap Sort         Sorted            1000         0.000000               17583
              Insertion Sort         Sorted            1000         0.000000                 999
                  Merge Sort         Sorted            1000         0.000000                5044
Quick Sort (Median of Three)         Sorted            1000         0.000000                9520
                  Radix Sort         Sorted            1000         0.000000                 999
              Selection Sort         Sorted            1000         0.000000              499500
                 Bubble Sort         Random            5000         0.021857            12494650
                   Heap Sort         Random            5000         0.001286              107687
              Insertion Sort         Random            5000         0.006143             6254150
                  Merge Sort         Random            5000         0.002143               55182
Quick Sort (Median of Three)         Random            5000         0.000143               69918
                  Radix Sort         Random            5000         0.000000                4999
              Selection Sort         Random            5000         0.014143            12497500
                 Bubble Sort Reverse Sorted            5000         0.029571            12497500
                   Heap Sort Reverse Sorted            5000         0.000714              103227
              Insertion Sort Reverse Sorted            5000         0.016000            12497500
                  Merge Sort Reverse Sorted            5000         0.000571               29804
Quick Sort (Median of Three) Reverse Sorted            5000         0.000143              106182
                  Radix Sort Reverse Sorted            5000         0.000000                4999
              Selection Sort Reverse Sorted            5000         0.012857            12497500
                 Bubble Sort         Sorted            5000         0.000000                4999
                   Heap Sort         Sorted            5000         0.000571              112126
              Insertion Sort         Sorted            5000         0.000000                4999
                  Merge Sort         Sorted            5000         0.001286               32004
Quick Sort (Median of Three)         Sorted            5000         0.000000               60678
                  Radix Sort         Sorted            5000         0.000000                4999
              Selection Sort         Sorted            5000         0.015143            12497500
                 Bubble Sort         Random           10000         0.112143            49991172
                   Heap Sort         Random           10000         0.000286              235317
              Insertion Sort         Random           10000         0.029714            24755456
                  Merge Sort         Random           10000         0.000571              120419
Quick Sort (Median of Three)         Random           10000         0.000286              152945
                  Radix Sort         Random           10000         0.000000                9999
              Selection Sort         Random           10000         0.044429            49995000
                 Bubble Sort Reverse Sorted           10000         0.105286            49995000
                   Heap Sort Reverse Sorted           10000         0.000286              226682
              Insertion Sort Reverse Sorted           10000         0.060286            49995000
                  Merge Sort Reverse Sorted           10000         0.000000               64608
Quick Sort (Median of Three) Reverse Sorted           10000         0.000000              234923
                  Radix Sort Reverse Sorted           10000         0.000000                9999
              Selection Sort Reverse Sorted           10000         0.043286            49995000
                 Bubble Sort         Sorted           10000         0.000000                9999
                   Heap Sort         Sorted           10000         0.000143              244460
              Insertion Sort         Sorted           10000         0.000000                9999
                  Merge Sort         Sorted           10000         0.000000               69008
Quick Sort (Median of Three)         Sorted           10000         0.001143              131343
                  Radix Sort         Sorted           10000         0.000000                9999
              Selection Sort         Sorted           10000         0.040571            49995000
                 Bubble Sort         Random           25000         0.935857           312485420
                   Heap Sort         Random           25000         0.000000              654862
              Insertion Sort         Random           25000         0.175429           156401077
                  Merge Sort         Random           25000         0.006000              334016
Quick Sort (Median of Three)         Random           25000         0.000000              412492
                  Radix Sort         Random           25000         0.000000               24999
              Selection Sort         Random           25000         0.253857           312487500
                 Bubble Sort Reverse Sorted           25000         0.639429           312487500
                   Heap Sort Reverse Sorted           25000         0.000000              633719
              Insertion Sort Reverse Sorted           25000         0.361429           312487500
                  Merge Sort Reverse Sorted           25000         0.001571              178756
Quick Sort (Median of Three) Reverse Sorted           25000         0.000000              660758
                  Radix Sort Reverse Sorted           25000         0.000000               24999
              Selection Sort Reverse Sorted           25000         0.267143           312487500
                 Bubble Sort         Sorted           25000         0.000000               24999
                   Heap Sort         Sorted           25000         0.000571              677688
              Insertion Sort         Sorted           25000         0.000000               24999
                  Merge Sort         Sorted           25000         0.000857              188476
Quick Sort (Median of Three)         Sorted           25000         0.000000              366397
                  Radix Sort         Sorted           25000         0.000000               24999
              Selection Sort         Sorted           25000         0.248429           312487500
                 Bubble Sort         Random           50000         4.018571          1249938144
                   Heap Sort         Random           50000         0.006286             1409800
              Insertion Sort         Random           50000         0.718714           625170165
                  Merge Sort         Random           50000         0.006857              718063
Quick Sort (Median of Three)         Random           50000         0.005714              898746
                  Radix Sort         Random           50000         0.001000               49999
              Selection Sort         Random           50000         1.015000          1249975000
                 Bubble Sort Reverse Sorted           50000         2.565000          1249975000
                   Heap Sort Reverse Sorted           50000         0.009429             1366047
              Insertion Sort Reverse Sorted           50000         1.440714          1249975000
                  Merge Sort Reverse Sorted           50000         0.013143              382512
Quick Sort (Median of Three) Reverse Sorted           50000         0.000286             1433133
                  Radix Sort Reverse Sorted           50000         0.002286               49999
              Selection Sort Reverse Sorted           50000         1.061000          1249975000
                 Bubble Sort         Sorted           50000         0.000000               49999
                   Heap Sort         Sorted           50000         0.006429             1455438
              Insertion Sort         Sorted           50000         0.000000               49999
                  Merge Sort         Sorted           50000         0.006714              401952
Quick Sort (Median of Three)         Sorted           50000         0.000714              782782
                  Radix Sort         Sorted           50000         0.001857               49999
              Selection Sort         Sorted           50000         1.006000          1249975000
                 Bubble Sort         Random           75000         9.712857          2812382300
                   Heap Sort         Random           75000         0.015143             2200249
              Insertion Sort         Random           75000         1.612857          1405331415
                  Merge Sort         Random           75000         0.015714             1121150
Quick Sort (Median of Three)         Random           75000         0.007714             1395028
                  Radix Sort         Random           75000         0.006143               74999
              Selection Sort         Random           75000         2.276714          2812462500
                 Bubble Sort Reverse Sorted           75000         5.746286          2812462500
                   Heap Sort Reverse Sorted           75000         0.009714             2138650
              Insertion Sort Reverse Sorted           75000         3.229714          2812462500
                  Merge Sort Reverse Sorted           75000         0.007429              594612
Quick Sort (Median of Three) Reverse Sorted           75000         0.004000             2272487
                  Radix Sort Reverse Sorted           75000         0.006571               74999
              Selection Sort Reverse Sorted           75000         2.366143          2812462500
                 Bubble Sort         Sorted           75000         0.000000               74999
                   Heap Sort         Sorted           75000         0.005429             2268087
              Insertion Sort         Sorted           75000         0.000000               74999
                  Merge Sort         Sorted           75000         0.009143              624316
Quick Sort (Median of Three)         Sorted           75000         0.001429             1195642
                  Radix Sort         Sorted           75000         0.003286               74999
              Selection Sort         Sorted           75000         2.249714          2812462500
                 Bubble Sort         Random          100000        16.655000          4999949594
                   Heap Sort         Random          100000         0.014857             3019575
              Insertion Sort         Random          100000         2.849714          2503572522
                  Merge Sort         Random          100000         0.019429             1536493
Quick Sort (Median of Three)         Random          100000         0.008714             2032796
                  Radix Sort         Random          100000         0.005286               99999
              Selection Sort         Random          100000         4.076857          4999950000
                 Bubble Sort Reverse Sorted          100000        10.262429          4999950000
                   Heap Sort Reverse Sorted          100000         0.014143             2926640
              Insertion Sort Reverse Sorted          100000         5.681143          4999950000
                  Merge Sort Reverse Sorted          100000         0.012857              815024
Quick Sort (Median of Three) Reverse Sorted          100000         0.007000             3107283
                  Radix Sort Reverse Sorted          100000         0.001714               99999
              Selection Sort Reverse Sorted          100000         4.204857          4999950000
                 Bubble Sort         Sorted          100000         0.000000               99999
                   Heap Sort         Sorted          100000         0.011429             3112517
              Insertion Sort         Sorted          100000         0.000000               99999
                  Merge Sort         Sorted          100000         0.013143              853904
Quick Sort (Median of Three)         Sorted          100000         0.002143             1665551
                  Radix Sort         Sorted          100000         0.000714               99999
              Selection Sort         Sorted          100000         4.012000          4999950000

Full results table saved to graphs\csv_data\all_sorting_benchmark_results.csv

--- Correlation Analysis Summary ---
Algorithm                           | Correlation (r) | P-value
----------------------------------------------------------------------
Bubble Sort                         |          0.9658 | 3.5767e-16
Heap Sort                           |          0.9335 | 1.2355e-12
Insertion Sort                      |          1.0000 | 2.1023e-58
Merge Sort                          |          0.9479 | 6.3080e-14
Quick Sort (Median of Three)        |          0.7848 | 1.2560e-06
Radix Sort                          |          0.7497 | 6.7452e-06
Selection Sort                      |          0.9997 | 5.5843e-42

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
Merge Sort                          |          0.9479 | 6.3080e-14
Quick Sort (Median of Three)        |          0.7848 | 1.2560e-06
Radix Sort                          |          0.7497 | 6.7452e-06
Selection Sort                      |          0.9997 | 5.5843e-42

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
Quick Sort (Median of Three)        |          0.7848 | 1.2560e-06
Radix Sort                          |          0.7497 | 6.7452e-06
Selection Sort                      |          0.9997 | 5.5843e-42

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