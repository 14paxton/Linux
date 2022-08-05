## get all deletes and changes
```bash
git log --shortstat --author "bpaxton"  --since "35 days ago" --until "today" \\
    | egrep "file[s]* changed" \\
    | sed 's/changed, \([0-9]\+ deletions\)/changed, 0 insertions(+), \1/g' \\
    | awk '{files+=$1; inserted+=$4; deleted+=$6} END {print "files changed", files,"total: " inserted - deleted , "lines inserted:", inserted, "lines deleted:", deleted}'
    ```
