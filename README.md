# 4-Bit Digital Counter Using Verilog HDL

## 📌 Project Overview
This project implements a 4-bit digital counter using Verilog Hardware Description Language (HDL). It demonstrates fundamental concepts of digital logic design, sequential circuits, clock signals, and reset operation.

## 🎯 Objectives
- Understand sequential logic design using Verilog HDL.
- Implement a 4-bit counter with clock and reset inputs.
- Learn RTL coding practices for digital design.
- Explore the fundamentals of VLSI design.

## ⚙️ Design Specifications
- **Design:** 4-Bit Digital Counter
- **Language:** Verilog HDL
- **Inputs:** Clock (`clk`), Reset (`reset`)
- **Output:** 4-bit counter value (`count[3:0]`)
- **Counter Range:** 0 to 15
- **Operation:** Increments on each active clock edge; resets to zero when reset is asserted.

## 🧠 Working Principle
The counter updates its value on the rising edge of the clock. When reset is asserted, the counter value becomes `0000`. Otherwise, the counter increments by one. After reaching `1111` (decimal 15), the 4-bit counter wraps around to `0000`.

## 💻 Verilog Code
The design uses a clocked procedural block and a non-blocking assignment to describe sequential behavior.

```verilog
module counter (
    input clk,
    input reset,
    output reg [3:0] count
);

always @(posedge clk) begin
    if (reset)
        count <= 4'b0000;
    else
        count <= count + 1'b1;
end

endmodule
```

## 🛠️ Tools and Technologies
- Verilog HDL
- RTL Design
- Digital Logic Design
- [Add your simulator or EDA tool here, if used]

## 🧪 Verification
Verify the counter by checking that:
- Reset sets the count to zero.
- The count increments on each rising clock edge when reset is inactive.
- The count wraps from 15 back to zero.

Add simulation waveforms or testbench results here if available.

## 📚 Key Learning Outcomes
- Sequential circuit design
- Clock and reset behavior
- Verilog RTL coding
- Binary counting and overflow
- Fundamentals of digital IC design

## 👨‍💻 Author
Shivanand Kadam

---

*This project was developed for learning and exploring digital design concepts using Verilog HDL.*
