#NPC Visibility Recovery Simulator

The core idea behind this logic is to preserve fair viewport visibility distribution even after items become unavailable post-shuffle.

Instead of rebuilding the carousel from scratch, the system attempts to recover the layout while ensuring that:

no row gets disproportionately favored
items do not unfairly drift toward the viewport too often
visibility probability remains relatively balanced over repeated renders

To achieve this:

top and bottom rows shuffle independently to maintain randomness
both rows are interleaved to preserve local contextual proximity
unavailable items are removed after shuffle generation
the carousel reconstructs itself while compacting gaps and preserving structural continuity

The logic also ensures that empty slots can only accumulate toward the bottom-right side of the layout, helping maintain a visually stable carousel structure.
