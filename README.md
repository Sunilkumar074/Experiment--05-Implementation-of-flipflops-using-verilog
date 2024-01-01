Developed by:SUNIL KUMAR P.B.<br>

Refrence number:212223040213

# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/598be6f9-6d0a-4c16-81fa-969774bb81ff)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/dc19ea26-850c-43fc-b970-339889755674)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/a7762c53-62af-492b-95db-29d3844f1fe0)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/185ea7e7-3a85-4d5a-9227-dc7304f6faec)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/57375f99-30e7-4836-89f3-51065c9e9fb0)

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/379d23db-a5d6-4adf-b514-ba62daa50c0a)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/9720dab4-127c-414e-af3b-b452085f535c)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/f56f860b-8998-47c2-a30d-2e6a2db7a003)

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/90a62e8b-c227-41ed-b569-e1fa16f80dc1)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/266c0d47-377c-4c77-a7b4-3c20f84d9a03)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/4e701243-2d98-496b-99d2-f38127d6df07)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/10508176-8814-4430-b7fd-53fea55debb6)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/c6a10ba5-6b9e-4e08-a61a-df230e15460f)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
1.Using nand gates and wires construct sr flip flop.
2.Repeat same steps to construct JK,D,T flipflops.
3.Find Rtl logic and timing diagram for all flipflops.
4.end the program
### PROGRAM 
SR Flip-Flop:
module SR_flipflop(S,R,clk,Q,Qbar);
input S,R,clk;
output Q,Qbar;
wire X,Y;
nand (X,S,clk);
nand (Y,R,clk);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule

D Flip-Flop:
module D_flipflop(D,clk,Q,Qbar);
input D,clk;
output Q,Qbar;
assign Dbar=~D;
wire X,Y;
nand (X,D,clk);
nand (Y,Dbar,clk);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule

JK Flip-Flop:
module JK_flipflop(J,K,clk,Q,Qbar);
input J,K,clk;
output Q,Qbar;
wire X,Y;
nand (X,J,clk,Qbar);
nand (Y,K,clk,Q);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule

T Flip-Flop:
module T_flipflopo(T,clk,Q,Qbar);
input T,clk;
output Q,Qbar;
wire S,R;
nand (S,T,clk,Qbar);
nand (R,T,clk,Q);
nand (Q,S,Qbar);
nand (Qbar,R,Q);
endmodule

### RTL LOGIC FOR FLIPFLOPS 
SR Flip-Flop:

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/2419b148-b6fc-4e3f-9eae-d82ff39e1440)

D Flip-Flop:

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/a5c71a4e-1a57-4755-88b2-b7055c78bd83)

JK Flip-Flop:

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/91ea23d9-9ea7-46e4-8bfc-35a58b9eed1e)

T Flip-Flop:

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/7ae4c624-c7d3-4ad1-8cb4-60a84c7aed3f)

### TIMING DIGRAMS FOR FLIP FLOPS 
SR Flip-Flop:

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/359a39b6-ff7d-40fc-a891-644bb534cb6a)

D Flip-Flop:

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/042d73eb-2a37-4d63-ab15-f550d2bcd363)

JK Flip-Flop:

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/b609b17c-0b9c-4745-8c14-6e4aaec0c8e7)

T Flip-Flop:

![image](https://github.com/Sunilkumar074/Experiment--05-Implementation-of-flipflops-using-verilog/assets/152241049/692ba39b-b7cb-46b9-b63f-a7df76d9803d)

### RESULTS 
Thus implementation of SR, JK, D and T flipflops using nand gates are done sucessfully.
