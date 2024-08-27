query-sort-by:: block
query-table:: true
query-sort-desc:: false
query-properties:: [:block :finish :remark]

- ---
- {{query (and [[Calibration/HMP]] #cal-due )}}
  query-sort-by:: due
  query-table:: true
  query-sort-desc:: false
  query-properties:: [:finish :block :due :out :sn :remark]