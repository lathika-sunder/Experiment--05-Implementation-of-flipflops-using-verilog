# Experiment--05-Implementation-of-flipflops-using-verilog

#### Lathika Sunder, 212221230054
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure

1.Using nand gates and wires construct sr flip flop.

2.Repeat same steps to construct JK,D,T flipflops.

3.Find Rtl logic and timing diagram for all flipflops.

4.end the program.


~~~
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Aavula Tharun.
RegisterNumber:212221240003  
*/
~~~ 

# SR Flip-flop
## Program:

~~~
module EX_SR(s,r,clock,q,qbar);
input s,r,clock;
output q,qbar;
wire x,y;
nand(x,s,clock);
nand(y,r,clock);
nand(q,x,qbar);
nand(qbar,y,q);
endmodule
~~~

### RTL LOGIC FOR FLIPFLOPS:
![SR output](https://user-images.githubusercontent.com/93427201/168079268-ff1517fe-ef63-4fd5-84db-898a715132b5.png)

### TIMING DIGRAMS FOR FLIP FLOPS:

![SR timming](https://user-images.githubusercontent.com/93427201/168079350-8cd353f4-005c-409f-ac71-ad056b1d5319.png)


# D Flip-flop
## program:
~~~
module DF(d,clock,q,qbar);
input d,clock;
output q,qbar;
assign dbar=!d;
wire x,y;
nand(x,d,clock);
nand(y,dbar,clock);
nand(q,x,qbar);
nand(qbar,y,q);
endmodule
~~~


### RTL LOGIC FOR FLIPFLOPS:

![DF output](https://user-images.githubusercontent.com/93427201/168080200-78df2809-7201-4613-8528-f5da941d888b.png)


### TIMING DIGRAMS FOR FLIP FLOPS:

![DF timming](https://user-images.githubusercontent.com/93427201/168080272-fea8fe64-1a98-4425-9b05-16f47a3efadd.png)


# J Flip-flop

## Program:
~~~
module JK(J,K,Clk,Q,Qbar);
input J,K,Clk;
output Q,Qbar;
wire P,S;
nand(P,J,Clk,Qbar);
nand(S,K,Clk,Q);
nand(Q,P,Qbar);
nand(Qbar,Q,S);
endmodule
~~~


### RTL LOGIC FOR FLIPFLOPS:

![JK output](https://user-images.githubusercontent.com/93427201/168080321-ec2d0923-573c-4234-b25f-908bb2288216.png)


### TIMING DIGRAMS FOR FLIP FLOPS:

![JK timming](https://user-images.githubusercontent.com/93427201/168080372-fdd4a701-00ec-4b43-9d10-73c87876684f.png)



# T Flip-flop
## Program:
~~~
module TF(T,Clk,Q,Qbar);
input T,Clk;
output Q,Qbar;
wire P,S;
nand(P,T,Clk,Qbar);
nand(S,T,Clk,Q);
nand(Q,P,Qbar);
nand(Qbar,S,Q);
endmodule
~~~

### RTL LOGIC FOR FLIPFLOPS:

![TF output](https://user-images.githubusercontent.com/93427201/168080414-59b1d5a2-6673-417c-8852-3e1b6407d1d9.png)


### TIMING DIGRAMS FOR FLIP FLOPS:

![TF TIMMING](https://user-images.githubusercontent.com/93427201/168080441-47ba8a2e-d786-47f9-aba0-ed00f1900a74.png)


### RESULTS 

All the flipflops are implementde using verilog and their functionality has been validated using their functional tables.
