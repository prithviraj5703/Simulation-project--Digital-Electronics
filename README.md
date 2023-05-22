# TITTLE
IMPLEMENT EX NOR GATE USING NAND GATE ONLY
# THEORY
Step:1
In the implementation of EX NOR gate using NAND gate we can consider a and b are input wires and y is an output wire.

Step:2
The output y wire is assigned to the output of the final NAND gate which is implemented using the two intermediate NAND gates nand2 and nand3.

Step:3
The two inputs a and b are connected to the first NAND gate nand1.

Step:4
The ~ operator is used to negate the output of the NAND gates to implement the logical negation.
# LOGIC DIAGRAM
![image](https://github.com/prithviraj5703/Simulation-project--Digital-Electronics/assets/121418418/91a56124-3ce0-4e25-a553-0bac7d93e219)

# NETLIST DIAGRAM
![image](https://github.com/prithviraj5703/Simulation-project--Digital-Electronics/assets/121418418/4c7e4053-4482-4db8-813d-7d2b6f4125ef)

# TIMING DIAGRAM
![image](https://github.com/prithviraj5703/Simulation-project--Digital-Electronics/assets/121418418/39cb8f33-28ad-4ed2-a502-387700d9c34a)

# PROGRAM
```python
module ass1(a,b,y);
input a,b;
output y;
wire nand1, nand2, nand3;
assign nand1 = ~(a & b);
assign nand2 = ~(a & nand1);
assign nand3 = ~(b & nand1);
assign y = ~(nand2 & nand3);
endmodule
```
# REFERENCE
Thus the implementation of Ex Nor gate using Nand gate is obtained.
