# Verilog- half adder code
design.sv
module ha(input a,b,output sum,carry);
xor x1(sum,a,b);
and and1(carry,a,b);
endmodule
testbench.sv
module t1;
reg a,b;
wire sum,carry;
ha ha2(a,b,sum,carry);
initial
begin
$monitor("time=%0t a=%b b=%b sum=%b carry=%b",$time,a,b,sum,carry);
a=1'b0; b=1'b0;
#1 a=1'b0; b=1'b1;
#1 a=1'b1; b=1'b0;
#1 a=1'b1; b=1'b1;
end
endmodule


