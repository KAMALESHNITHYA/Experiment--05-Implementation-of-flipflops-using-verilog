## NAME : KAMALESH R
## REGISTER NUMBER : 212223230094
## Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: 
To implement all the flipflops using verilog and validating their functionality using their functional tables

 HARDWARE  – PC, Cyclone II , USB flasher
 
 
 SOFTWARE  -Quartus prime

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

1.Using nand gates and wires construct SR flip flop.

2.Repeat same steps to construct JK,D,T flipflops.

3.Find RTL logic and timing diagram for all flipflops.


## PROGRAM 

## SR FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/56fff2fc-7475-4c21-9ab2-f9934cf0c238)

## JK FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/3c6eda55-cd13-45c8-9119-213204a27466)

## D FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/888a8f1b-2055-48f9-8296-0c57d4eaa4a7)

## T FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/cbe180db-839f-4b15-9d51-3a335a17e547)


## RTL LOGIC FOR FLIPFLOPS 

## SR FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/c5cd37cd-647a-478f-ba2f-6555dd957262)

## JK FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/86baa6f6-d734-4011-8eb1-4cb65e5c6237)


## D FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/79ac371a-e653-48ca-9102-318b136b972f)


## T FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/0953a3d0-d429-4418-85f5-14d2db3d9d8b)

### TIMING DIGRAMS FOR FLIP FLOPS 

## SR FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/2c76b160-7dfa-42e6-8ed3-781f18fe70d7)

## JK FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/c1159a44-5e5a-4da0-8af1-97c83b13b43b)

## D FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/944f5a05-7f41-462c-bce5-4d4786c49809)

## T FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/d13d6682-99e6-4023-9e43-d15cc7a854f2)

## OUTPUT 

## SR FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/56f8dc0e-6129-4774-9bf1-22f8a3bf0764)

## JK FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/be9bb9bb-f12c-4c9a-b999-d71cf988e0c4)

## D FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/7fdf434d-09b4-4142-8667-9af96e353f74)

## T FLIPFLOP

![image](https://github.com/KAMALESHNITHYA/Experiment--05-Implementation-of-flipflops-using-verilog/assets/145743119/8ad8da83-a913-4128-ab94-3e3a237b59d9)









## RESULTS 
Thus, the implementation of SR,JK,D and T flipflops using nand gates are done sucessfully.

