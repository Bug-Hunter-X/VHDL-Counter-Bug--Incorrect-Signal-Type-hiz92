# VHDL Counter Bug: Incorrect Signal Type

This repository demonstrates a common error in VHDL: using an integer signal where a std_logic_vector would be more appropriate. This can lead to unexpected behavior and synthesis issues.  The `buggy_counter.vhd` file contains the erroneous code, while `fixed_counter.vhd` shows the corrected version. 

The bug stems from using `integer` for the counter.  Synthesizers might handle this differently, leading to unpredictable results, especially in terms of resource utilization and timing.  Using `std_logic_vector` offers better control and is generally preferred for hardware designs.

**How to reproduce:** Synthesize and simulate both `buggy_counter.vhd` and `fixed_counter.vhd`. Observe the differences in synthesis reports and simulation waveforms.

**Key takeaway:** Choose the appropriate data type for your VHDL signals based on their intended use and the target hardware.