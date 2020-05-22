# Optimized (glitch-robust) masked hardware gadgets

This repository contains the
[maskverif](https://gitlab.com/benjgregoire/maskverif/) description of
optimized glitch-robust SNI refresh gadgets for d=2,...,16 shares introduced in [4].
A human-readable description of the gadgets is available in <opt_refresh.pdf>.

We provide below a comparison of the randomness complexities of these gadgets
and state-of-the art for both software and hardware.
Bold font indicate cases where our gadgets improve the randomness
complexity compared to both HW and SW state-of-the-art.

| d  |  HW [1] | SW [2,3] | HW-Generic [4] | This |
|----|--------------|-----|----|---------|
| 2  |            1 |   1 |  1 |    1 |
| 3  |            3 |   3 |  3 |    **2** |
| 4  |            6 |   4 |  6 |    4 |
| 5  |           10 |   8 |  8 |    **5** |
| 6  |           15 |  12 | 12 |    **7** |
| 7  |           21 |  13 | 15 |    **9** |
| 8  |           28 |  16 | 20 |   **11** |
| 9  |           36 |  18 | 22 |   **13** |
| 10 |           45 |  20 | 26 |   **15** |
| 11 |           55 |  22 | 30 |   **17** |
| 12 |           66 |  24 | 36 |   **20** |
| 13 |           78 |  26 | 39 |   26 |
| 14 |           91 |  28 | 44 |   28 |
| 15 |          105 |  30 | 49 |   30 |
| 16 |          120 |  32 | 56 |   32 |

A verilog implementation of these gadgets is available [here](https://github.com/cassiersg/fullverif/blob/master/lib_v/MSKref.v).

[1] Faust, S., Grosso, V., Merino Del Pozo, S., Paglialonga, C., & Standaert,
F.-X. (2018). Composable Masking Schemes in the Presence of Physical Defaults &
the Robust Probing Model. IACR Transactions on Cryptographic Hardware and
Embedded Systems, 2018(3), 89-120.
<https://doi.org/10.13154/tches.v2018.i3.89-120>

[2] Barthe, G., Belaïd, S., Dupressoir, F. et al. Improved parallel mask
refreshing algorithms: generic solutions with parametrized non-interference and
automated optimizations. J Cryptogr Eng (2019).
<https://doi.org/10.1007/s13389-018-00202-2>

[3] Battistello A., Coron JS., Prouff E., Zeitoun R. (2016) Horizontal
Side-Channel Attacks and Countermeasures on the ISW Masking Scheme. In:
Gierlichs B., Poschmann A. (eds) Cryptographic Hardware and Embedded Systems –
CHES 2016. CHES 2016. Lecture Notes in Computer Science, vol 9813. Springer,
Berlin, Heidelberg
<https://doi.org/10.1007/978-3-662-53140-2_2>

[4] Cassiers G., Grégoire B., Levi I., Standaert FX. (2020) Hardware Private
Circuits: From Trivial Composition to Full Verification. IACR Eprint Archive
<https://eprint.iacr.org/2020/185>
