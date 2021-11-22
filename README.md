# TNCY-I
The dataset used for benchmarking Hybrid Flow Shop problem with time-varying resources and chaining exact time-lag (noted FHc-EV)

# Problem description
Given `A` jobs arrived as multiple chains ` Q[n] (1 <= n <= N) ` at the beginning of horizon. Each chain `Q[n]` is a sequence of `a[n]` jobs `J[n][i] (1 <= i <= a[n])` with exact time-lag `l[n][i]` between two consecutive jobs `J[n][i]` and ` J[n][i+1]`. Each job ` J[n][i]` consists of `m` operations. Each operation `o` of the job `J[n][i]` has a non-preemptive processing time `p[n][i][o]`. For each resource `v`, each operation `o` needs a certain amount `u[o][v]` per unit of time during its processing time. The resources' capacity of any resource `v` at any time `t` is denoted by `R[v][t]`. The criterion is minimizing the total completion time.

# Data description

Parameter | Type | Description
--- | --- | ---
T | int | The length of horizon
m | int | The number of operations per job
V | int | The number of renewable resources
R | int[v][t] | The capacity of resource `v` at time `t`
u | int[o][v] | The usage per unit time of operation `o` of resource `v`
N | int | The number of chains
a | int[n] | The lengths of chains
p | int[n][i][o] | The processing time of operation `o` of job `i` of chain `n`
l | int[n][i] | The time-lag between job `i` and `i+1` of chain `n`