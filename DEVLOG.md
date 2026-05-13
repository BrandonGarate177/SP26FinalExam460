# Development Log – The Torchbearer

**Student Name:** Brandon Garate 
**Student ID:** 130364309

---

## Entry 1 – [May 13, 3pm]: Initial Plan


Math: 
    - One Dijkstra from `S` is only fixing for distance from `S`. It does NOT select an order to visit all relics. 
    - After precomputation we will still need to search over permutations / the orders. 

Implementation: 
    - `run_dijkstra` should be created first. 
    - `select_sources` && `precompute_distances`. 
    - `find_optical_route` / `_explore`, these should state where we are, which relics are done, and the cost so far. 
        the goal is that all relics are collected, and then pay costs to T. 

How are we supposed to preform the precalculation? How do we determine which nodes we need to run Dijkstra FROM so that every lef the search needs exists in our table? 






---

## Entry 2 – [May 13, evening]: Part 2 design assumptions

I briefly treated the exit as a candidate Dijkstra **source** so we would have a row for “leaving T,” but the planner never needs that: we only need cheapest costs **to** the exit from wherever we currently are (spawn or a relic). I kept `select_sources` as spawn plus each distinct relic and rely on `dist_table[u][exit_node]` for the final leg. I also almost wrote README Part 2b about the nested `dist_table` until I re-checked the handout mapping and aligned 2b with the single-source `dict` returned by `run_dijkstra`.

---

## Entry 3 – [Date]: [Short description]

_Your entry here._

---

## Entry 4 – [Date]: Post-Implementation Reflection

> Required. Written after your implementation is complete. Describe what you would
> change or improve given more time.

_Your entry here._

---

## Final Entry – [Date]: Time Estimate

> Required. Estimate minutes spent per part. Honesty is expected; accuracy is not graded.

| Part | Estimated Hours |
|---|---|
| Part 1: Problem Analysis | |
| Part 2: Precomputation Design | |
| Part 3: Algorithm Correctness | |
| Part 4: Search Design | |
| Part 5: State and Search Space | |
| Part 6: Pruning | |
| Part 7: Implementation | |
| README and DEVLOG writing | |
| **Total** | |
