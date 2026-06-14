## 2023-10-27 - Array method allocations in game loops
**Learning:** In hot loops like `getPossibleWords`, chaining `filter()`, `map()`, and `new Set()` creates severe GC overhead due to intermediate array allocations. Combined with `split()` inside custom comparators, it kills performance.
**Action:** Replace functional array pipelines with single imperative loops using string operations (`indexOf` and `slice`) for large dictionary filtering.
