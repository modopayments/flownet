# testdata

There are two types of test in this folder, `.flow` tests and `.circ` tests. This file explains the format of both.

### .flow tests

A `.flow` test describes a flow network and (optionally) its expected max-flow. The file format does not admit inline comments (although we use them in the example below.)

```
4      # we expect a max flow of 4
0 1 3  # edge from 0 -> 1 with capacity 3
1 2 5  # edge from 1 -> 2 with capacity 5
0 6 7  # edge from 0 -> 6 with capacity 7
```

### .circ tests

A `.circ` test describes a flow network with edge demands and a lower bound on its
expected outflow. The file format does not admit inline comments or trailing spaces
prior to a newline (although we use them in the example below.)

```
7        # we expect an outflow of at least 7
0 1 3 3  # edge from 0 -> 1 with capacity 3 and demand 3
1 2 5 2  # edge from 1 -> 2 with capacity 5 and demand 2
0 6 7 0  # edge from 0 -> 6 with capacity 7 and demand 0
```