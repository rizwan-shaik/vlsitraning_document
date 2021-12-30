1. IC (integrated circuit),An integrated circuit or monolithic integrated circuit  is a set of electronic circuits on one small flat piece (or "chip")
of semiconductor material, usually silicon.Large numbers of tiny MOSFETs integrate into a small chip.
2. To design an IC we need to develop a code(programe),for this code we use verilog language which is HDL(Hard Description Language).
3. This IC are build with transistors in it with the gates too,we use the gates in verilog logics codes 
4. lets use design a Hafe Adder circuit  
                            ![image](https://user-images.githubusercontent.com/93262817/147666166-c30646a2-cc2b-401e-9438-b4e3d1bfa64e.png)
5. In this image (or code) we first write module which is keyword and and next in side the bracets we write all inputs and outputs which is called port list,
    next we write all i/p and o/p and then the gates which are used in the ic and then endmodule
6. we also write testbench for it which is written to verify wether the dsign is perfectly working or not
7.             `timescale 1ns/1ps
                 module half_adder_tb;
                 reg a,b;
                wire sum,co;
                half_adder ha1(a,b,sum,co);
                initial
                begin
                $dumpfile("ha.vcd");
                $dumpvars(1);
                end
                initial
                begin
               {a,b}=2'b00;
               #5 {a,b}=2'b01;
               #5 {a,b}=2'b10;
               #5 {a,b}=2'b11;
               end
               initial
            $monitor("simtime=%0g, a=%b, b=%b, sum=%b, co=%b", $time, a,b,sum,co);
               endmodule 
8. In this testbench we need to write first timescale in every testbenchs for every ic design codes, next we write module and all i/p and o/p,next we write $dumpfile 
   to get vcd file which is for graph and $dumpvars to take module next we give input values and $monitor to view output of the programe and endmodule to end the code 
9. we various tools to run and check the programe we use a simple tool called edaplayground tool 
10. Which looks like as the below picture 
11.                 ![image](https://user-images.githubusercontent.com/93262817/147734125-2308e55d-8ed4-4ab6-a93e-8b86080a29e5.png)

















                     
