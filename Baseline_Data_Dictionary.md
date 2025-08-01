## Data Dictionary

> **Example values shown for the 2016 election.**

| Feature | Description | Example Value (2016) |
|---------|-------------|----------------------|
| **year** | The election year | `2016` |
| **Poll_Leading_Margin** | The difference between the average polling percent for the Democratic candidate and the Republican candidate that year. Positive means Dem was ahead. | `3.3` |
| **Poll_Leader** | Party leading in average national polls (`0` = Democrat, `1` = Republican) | `0` |
| **EC_election_winner** | Electoral College winner (`0` = Democrat, `1` = Republican) | `1` |
| **PC_election_winner** | Popular Vote winner (`0` = Democrat, `1` = Republican) | `0` |
| **EC_Poll_Accurate** | 1 if the poll leader matched the EC winner, 0 if not | `0` |
| **PC_Poll_Accurate** | 1 if the poll leader matched the popular vote winner, 0 if not | `1` |
| **Democratic** | Average national polling percent for Democratic candidate | `48.2` |
| **Republican** | Average national polling percent for Republican candidate | `44.9` |
| **Republican_Electoral** | Electoral votes won by Republican | `304` |
| **Democrat_Electoral** | Electoral votes won by Democrat | `227` |
| **Republican_Popular** | Popular votes for Republican | `62,984,828` |
| **Democrat_Popular** | Popular votes for Democrat | `65,853,514` |
| **Total_Popular_Vote (Total votes cast in Presidential Election)** | Total votes cast in the election | `136,669,237` |
| **Republican_Electoral_pct (out of 270)** | Republican EC votes as percent of 270 | `112.6` |
| **Democrat_Electoral_pct (out of 270)** | Democrat EC votes as percent of 270 | `84.1` |
| **Republican_Popular_pct (Out of total votes cast in Presidential Election)** | Republican share of total popular vote (%) | `46.1` |
| **Democrat_Popular_pct (Out of total votes cast in Presidential Election)** | Democrat share of total popular vote (%) | `48.2` |
| **Electoral_Leading_Margin (difference between dem and rep electorial pct)** | Dem EC percent minus Rep EC percent | `-28.5` |
| **Popular_Leading_Margin (difference between dem and rep popular vote pct)** | Dem popular vote percent minus Rep | `2.1` |
| **Poll_vs_Electoral_Margin_Diff** | Poll margin minus EC margin | `31.8` |
| **Poll_vs_Popular_Margin_Diff** | Poll margin minus popular vote margin | `1.2` |

---

**Legend for binary variables:**  
- `0` = Democrat  
- `1` = Republican  

**Legend for _Poll_Accurate columns_:**  
- `1` = Accurate (poll leader matched winner)  
- `0` = Not accurate (poll leader did not match winner)
