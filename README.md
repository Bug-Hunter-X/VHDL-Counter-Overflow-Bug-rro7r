# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL: an unsigned counter without overflow protection. The `counter.vhdl` file contains the buggy code, while `counter_fixed.vhdl` shows the corrected version.

**Bug:** The counter uses a generic `N` to define the bit width but doesn't explicitly handle the case where `internal_count` exceeds the maximum value (2**N - 1). This leads to an undefined behavior, potentially wrapping around or causing simulation issues.

**Solution:** The corrected code includes a modulo operation to ensure `internal_count` stays within the defined range.