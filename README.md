# TITTLE: 16:1 MULTIPLEXER

# THEORY:
A 16:1 multiplexer is a digital circuit that allows the selection of one out of 16 input lines to be routed to a single output line. It is commonly abbreviated as "16x1 MUX." The number before the colon represents the number of input lines, and the number after the colon represents the number of output lines.

In the case of a 16:1 multiplexer, there are 16 input lines and 1 output line. The control inputs of the multiplexer are used to select which input line is connected to the output line. The number of control inputs required is determined by the number of input lines. In this case, with 16 input lines, you would need 4 control inputs because 2^4 equals 16.

The control inputs are usually represented as binary numbers. For example, if the control inputs are labeled A, B, C, and D, then the 16 possible combinations of the control inputs (0000 to 1111) correspond to selecting one of the 16 input lines.

The truth table for a 16:1 multiplexer would have 16 rows, with each row representing an input line, and the output column indicating which input line is selected based on the control inputs. The other input lines that are not selected will have their outputs disconnected.

To implement a 16:1 multiplexer, you can use a combination of smaller multiplexers, such as 4:1 or 8:1 multiplexers. By cascading these smaller multiplexers together and appropriately connecting their control inputs, you can create a 16:1 multiplexer.

# LOGIC DIAGRAM:



# NETLIST DIAGRAM
![mux1](https://github.com/LavanyaMuraleedharan/Simulation-project--Digital-Electronics/assets/120103862/82eab42d-02ee-44e1-b373-fa6e586b1b16)
![mux2](https://github.com/LavanyaMuraleedharan/Simulation-project--Digital-Electronics/assets/120103862/161a13d3-ea93-4c1f-a562-e52c752ecd0c)


# TIMING DIAGRAM

# PROGRAM:
```
module mux(i0,i1,i2,i3,i4,i5,i6,i7,i8,i9,i10,i11,i12,i13,i14,i15,s0,s1,s2,s3,y);
input i0,i1,i2,i3,i4,i5,i6,i7,i8,i9,i10,i11,i12,i13,i14,i15,s0,s1,s2,s3;
output y;
wire a,b,c,d,e,f,g,h,i,j,k,l,m,n,o,p,s0c,s1c,s2c,s3c;
not(s0c,s0);
not(s1c,s1);
not(s2c,s2);
not(s3c,s3);
and(a,s0c,s1c,s2c,s3c,i0);
and(b,s0c,s1c,s2c,s3,i1);
and(c,s0c,s1c,s2,s3c,i2);
and(d,s0c,s1c,s2,s3,i3);
and(e,s0c,s1,s02,s03,i4);
and(f,s0c,s1,s02,s3,i5);
and(g,s0c,s1,s2,s3c,i6);
and(h,s0c,s1,s2,s3,i7);
and(i,s0,s1c,s2c,s3c,i8);
and(j,s0,s1c,s2c,s3,i9);
and(k,s0,s1c,s2,s3c,i10);
and(l,s0,s1c,s2,s3,i11);
and(m,s0,s1,s2c,s3c,i12);
and(n,s0,s1,s2c,s3,i13);
and(o,s0,s1,s2,s3c,i14);
and(p,s0,s1,s2,s3,i15);
or(y,a,b,c,d,e,f,g,h,i,j,k,l,m,n,o,p);
endmodule  
```
# REFERENCE
