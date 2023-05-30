# TITLE: 1x16 demultiplexer

# THEORY:
A De-multiplexer is a combinational circuit that has only 1 input line and 2^N output lines. Simply, the multiplexer is a single-input and multi-output combinational circuit. The information is received from the single input lines and directed to the output line. On the basis of the values of the selection lines, the input will be connected to one of these outputs. De-multiplexer is opposite to the multiplexer.

Unlike encoder and decoder, there are n selection lines and 2n outputs. So, there is a total of 2n possible combinations of inputs. De-multiplexer is also treated as De-mux.

There are various types of De-multiplexer which are as follows:
A 1x16 demultiplexer, also known as a 1-to-16 demultiplexer, is a digital circuit that takes a single input signal and directs it to one of the 16 possible output lines based on the control inputs. It is commonly represented using the shorthand notation "1:16 DEMUX."

The demultiplexer has one input line and four control lines. The number of control lines required in a demultiplexer is determined by the formula 2^N, where N is the number of control lines. In this case, N = 4, so the demultiplexer has 2^4 = 16 output lines.

The control lines determine which output line the input signal is routed to. The 1x16 demultiplexer has four control lines, often labeled as A, B, C, and D. These control lines can take binary values (0 or 1), which allows for the selection of one of the 16 output lines.

![image](https://github.com/LavanyaMuraleedharan/Simulation-project--Digital-Electronics/assets/120103862/0850fc4f-0f7a-4122-8aee-5f702c5f9f2c)

## Truth table:
![image](https://github.com/LavanyaMuraleedharan/Simulation-project--Digital-Electronics/assets/120103862/866b540b-b0b6-4af0-895e-38d926b745be)

The logical expression of the term Y is as follows:

Y0=A.S0'.S1'.S2'.S3'
Y1=A.S0'.S1'.S2'.S3
Y2=A.S0'.S1'.S2.S3'
Y3=A.S0'.S1'.S2.S3
Y4=A.S0'.S1.S2'.S3'
Y5=A.S0'.S1.S2'.S3
Y6=A.S0'.S1.S2.S3'
Y7=A.S0'.S1.S2.S3
Y8=A.S0.S1'.S2'.S3'
Y9=A.S0.S1'.S2'.S3
Y10=A.S0.S1'.S2.S3'
Y11=A.S0.S1'.S2.S3
Y12=A.S0.S1.S2'.S3'
Y13=A.S0.S1.S2'.S3
Y14=A.S0.S1.S2.S3'
Y15=A.S0.S1.S2'.S3


# LOGIC DIAGRAM:
![image](https://github.com/LavanyaMuraleedharan/Simulation-project--Digital-Electronics/assets/120103862/df9a4bdb-8430-40ff-86f6-2dd05305de12)

# NETLIST DIAGRAM
![demux1](https://github.com/LavanyaMuraleedharan/Simulation-project--Digital-Electronics/assets/120103862/e1eefb4b-5c77-4131-857d-39d003c4e954)
![demux2](https://github.com/LavanyaMuraleedharan/Simulation-project--Digital-Electronics/assets/120103862/8d874746-32ac-450d-9d42-284b7007dc18)

# TIMING DIAGRAM
![Screenshot (18)](https://github.com/LavanyaMuraleedharan/Simulation-project--Digital-Electronics/assets/120103862/ea332dd0-950c-4064-89ec-35d642a9503f)


# PROGRAM:
```
Developed by: Lavanya M
Refernce number: 212222110021
module mux(out,a,s);
input  a;
input [3:0] s;
output reg [15:0] out;
always @(a,s)
begin
case(s)
4'b 0000:out[0]= a;
4'b 0001:out[1]=a ;
4'b 0010:out[2]= a;
4'b 0011:out[3]=a ;
4'b 0100:out[4]= a;
4'b 0101:out[5]= a;
4'b 0110:out[6]=a ;
4'b 0111:out[7]=a ;
4'b 1000:out[8]=a;
4'b 1001:out[9]=a ;
4'b 1010:out[10]= a;
4'b 1011:out[11]=a;
4'b 1100:out[12]= a;
4'b 1101:out[13]=a;
4'b 1110:out[14]=a;
4'b 1111:out[15]=a;
endcase
end
endmodule
 
```
# REFERENCE
https://technobyte.org/verilog-code-for-demultiplexer-using-behavioral-modeling/
