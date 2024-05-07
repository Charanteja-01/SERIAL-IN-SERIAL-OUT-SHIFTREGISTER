# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**
1.Initialize the shift register to a known state (e.g., all zeros).<br>
2.Input a bit serially into the shift register.<br>
3.Shift the contents of the register one position to the right (or left). <br>
4.Output the shifted bit from the last stage of the register. <br>
5.Repeat steps 2-4 for each bit you want to input and shift.<br>

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by:YEDLAPALLI CHARAN TEJA 
RegisterNumber:212223040247

*/
```
module ex10(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule
```

**RTL LOGIC FOR SISO Shift Register**

![328374161-85ed714a-bf7e-4676-bcce-bb7b262a2138](https://github.com/Charanteja-01/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/145693038/521f8071-554b-4947-9fa4-e8db95656b75)


**TIMING DIGRAMS FOR SISO Shift Register**

![328374209-dc708476-e275-4e09-9c97-660a30471c03](https://github.com/Charanteja-01/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/145693038/8cb91aca-482f-4535-81b9-c7e582b61f45)


**RESULTS**
SISO Shift Register using verilog and validating their functionality using their functional tables has successful execution of the program.
