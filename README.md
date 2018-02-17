vndecorrelator
==============

# Introduction
A Verilog implementation of a von Neumann decorrelator.
This tiny module consumes bits and outputs decorrelated bits.

The [Von Neumann decorrelator](http://www1.spms.ntu.edu.sg/~kkhoongm/Entropy.pdf)
consumes pairs of bits and outputs bits based on the pattern in th bit pairs:

- 00 and 11: No output of a bit.
- 10 and 01: Output the first bit in the pair

In the best case with random bits, the output bitrate will be 1/4. For
heavily biased input bits, the rate will be much slower.

This implementation operates on streams of single bits and creates pairs
internally.


# Status

Implementation done. Tested in FPGA designs and works.
