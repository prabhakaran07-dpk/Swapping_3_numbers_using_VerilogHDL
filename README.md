# Swapping_3_numbers
## Experiment: Write and Simulate Swapping of Three Numbers using Verilog HDL and Verify with Testbench

## Aim

To write, simulate, and verify the swapping of three numbers using Verilog HDL and validate the functionality using a testbench in Xilinx Vivado.

## Apparatus Required

* Xilinx Vivado Design Suite
* Computer System (Windows/Linux)
* Verilog HDL Simulator (Integrated in Vivado)

## Procedure

1. Open Xilinx Vivado and create a new RTL project.
2. Create a Verilog source file named **swap3.v**.
3. Write the Verilog HDL code for swapping three numbers.
4. Save the design file.
5. Create a testbench file named **swap3_tb.v**.
6. Apply different input values through the testbench.
7. Run **Behavioral Simulation**.
8. Observe the waveform and verify whether the values are swapped correctly.
9. Record the simulation results.

## Verilog HDL Code

```verilog
module swap3;

reg [7:0] a, b, c;
reg [7:0] temp;

initial
begin
    a = 8'd10;
    b = 8'd20;
    c = 8'd30;

    $display("Before Swapping");
    $display("A=%d B=%d C=%d", a, b, c);

    temp = a;
    a = b;
    b = c;
    c = temp;

    #10;

    $display("After Swapping");
    $display("A=%d B=%d C=%d", a, b, c);
end

endmodule
```

## Testbench Code

```verilog
`timescale 1ns/1ps

module swap3_tb;

swap3 uut();

initial
begin
    #20;
    $finish;
end

endmodule
```

## Expected Output

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/16712dad-b2c7-4968-a6f0-ff3e04ab6f83" />


## Result

The swapping operation is successfully simulated using Verilog HDL.

## Conclusion

Thus, the Verilog HDL program for swapping three numbers was implemented and simulated successfully using Xilinx Vivado. The output waveform and simulation results verified the correct cyclic swapping of the three numbers using the testbench.
