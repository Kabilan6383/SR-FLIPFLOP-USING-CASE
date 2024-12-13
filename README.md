# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![Screenshot 2024-12-13 225433](https://github.com/user-attachments/assets/4a14ee62-9368-46b1-97d8-494f288a0f7d)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![Screenshot 2024-12-13 225452](https://github.com/user-attachments/assets/a2acf68d-5097-4ab2-ad09-6a53ec6287ed)


 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![Screenshot 2024-12-13 225503](https://github.com/user-attachments/assets/c833f175-df05-4070-adae-5bed69f3d0ed)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![Screenshot 2024-12-13 225518](https://github.com/user-attachments/assets/ee9b7f66-9574-48f5-8866-92c49c849d1e)


 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

/* write all the steps invloved */

**PROGRAM**
```
module sr(S,R,clk,Q,Qbar);
input S,R,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=S|((~R)&Q);
Qbar=~Q;
end
endmodule
```
/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:KABILAN P
RegisterNumber: 24900859
*/

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot 2024-12-13 225530](https://github.com/user-attachments/assets/f02ad147-e24b-41be-8949-7df2ac7ead82)


**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2024-12-13 225552](https://github.com/user-attachments/assets/056b62a0-9050-44fd-b9ce-285e10ef5488)

**RESULTS**
Thus the SR flipflop using verilog and validating their functionality using their functional tables are verified
