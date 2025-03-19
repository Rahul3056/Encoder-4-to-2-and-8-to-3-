 Encoder (4-to-2 and 8-to-3) - Theory, Design & Implementation

### Concept Overview
An **Encoder** is a combinational circuit that converts multiple input signals into a smaller number of output signals. Encoders are the reverse of decoders and are widely used in communication systems, data compression, and priority circuits.

### Detailed Explanation

#### ✅ 4-to-2 Encoder
- **Definition:** A 4-to-2 encoder has 4 input lines (`I0` to `I3`) and 2 output lines (`Y1`, `Y0`). Each output represents the binary equivalent of the active input line.
- **Boolean Expressions:**
  - `Y1 = I2 + I3`
  - `Y0 = I1 + I3`
- **Truth Table:**

| I3 | I2 | I1 | I0 | Y1 | Y0 |
|:--:|:--:|:--:|:--:|:--:|:--:|
|  0 |  0 |  0 |  1 |  0 |  0 |
|  0 |  0 |  1 |  0 |  0 |  1 |
|  0 |  1 |  0 |  0 |  1 |  0 |
|  1 |  0 |  0 |  0 |  1 |  1 |

**Example Application:** Used in keyboards to convert keypresses into binary codes.

#### ✅ 8-to-3 Encoder
- **Definition:** An 8-to-3 encoder has 8 input lines (`I0` to `I7`) and 3 output lines (`Y2`, `Y1`, `Y0`). Each output represents the binary equivalent of the active input line.
- **Boolean Expressions:**
  - `Y2 = I4 + I5 + I6 + I7`
  - `Y1 = I2 + I3 + I6 + I7`
  - `Y0 = I1 + I3 + I5 + I7`

- **Truth Table:**

| I7 | I6 | I5 | I4 | I3 | I2 | I1 | I0 | Y2 | Y1 | Y0 |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
|  0 |  0 |  0 |  0 |  0 |  0 |  0 |  1 |  0 |  0 |  0 |
|  0 |  0 |  0 |  0 |  0 |  0 |  1 |  0 |  0 |  0 |  1 |
|  0 |  0 |  0 |  0 |  1 |  0 |  0 |  0 |  0 |  1 |  1 |
|  1 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  1 |  1 |  1 |

**Example Application:** Used in priority encoders and interrupt controllers.


### Code Explanation
- **`assign` Statements:** Implements the logic for each encoder output based on the active input.
- **`$monitor` Task:** Displays real-time changes in encoder inputs and outputs.
- **Test Cases:** Verifies both 4-to-2 and 8-to-3 encoder logic for various combinations.

### Execution Steps
1. Copy the Verilog code into your simulator (e.g., ModelSim, Xilinx Vivado, etc.).
2. Compile and run the code.
3. Verify that the outputs match the expected truth table values.

### Real-World Example for Practice
- Design a **16-to-4 Priority Encoder** that prioritizes higher-order inputs if multiple inputs are active.


