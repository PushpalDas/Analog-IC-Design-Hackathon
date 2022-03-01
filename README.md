# Analog-IC-Design-Hackathon
Cloud Based Hackathon based on fixed parameters provided on analog IC designs.
# Table of contents
- [Abstract](https://github.com/PushpalDas/blob/main.Abstract)
- [Introduction](https://github.com/PushpalDas/blob/main/README.md#introdution)
- [Truth Table of 3 bit binary to gray code converter](https://github.com/PushpalDas/blob/main/README.md#Truth-Table-of-3-bit-binary-to-gray-code-converter) 
- [Schematic](https://github.com/PushpalDas/blob/main/README.md#Reference-Circuit)
- [Waveforms](https://github.com/PushpalDas/blob/main/README.md#Waveforms)
- [Author](https://github.com/PushpalDas/blob/main/README.md#Author)
- [References](https://github.com/PushpalDas/blob/main/README.md#References)
# Abstract 
This paper gives an idea of binary to gray code
converter. The binary to gray code converter is based on a
very common transmission gate technology. For operating at
low supply voltages( 2V), double pass-transistor(DPL) XOR
and XNOR circuits have been developed to improve circuit
performance. In this paper, the binary to gray code converter
is achieved using such a transistor-based approach. Utilizing 6
transistors in place of the conventional 10, this circuit not only
has low-power operational capability, but also a reduced area.
Index Terms—CMOS Transmission Gate, design, CMOS logic
gates.

# Introduction 
Gray codes are very useful for creating a normal sequence
of binary numbers that may result in an error when two successive values differ by only one bit (binary digit). Recognizing
Gray codes is very easy since they refer to an ordering of
binary numbers in which successive values differ by only one
In a 3-bit binary number, the binary digits will be B2, B1,
B0, where B2 is the most significant bit (MSB) and B0 is the
least significant bit (LSB). The gray code digits are G2, G1,
G0, where G2 is the most significant bit (MSB) and G0 is the
least significant bit (LSB) of Gray code.

# Truth Table of 3 bit binary to gray code converter
![Truth table](https://user-images.githubusercontent.com/90308885/155962120-6d318271-cd8b-4a9b-a2fd-6daba497a411.png)

# Schematic
![FINAL SCHEMATIC](https://user-images.githubusercontent.com/90308885/156212115-2cfb9102-de99-4986-aa13-491ebf7bfeaf.jpeg)

# Netlist
``` 
*  Generated for: PrimeSim
*  Design library name: pushpal_lib
*  Design cell name: code_converter
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Tue Mar  1 16:29:10 2022

.global gnd! vdd!
********************************************************************************
* Library          : pushpal_lib
* Cell             : code_converter
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xm11 g0 net29 net25 vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm10 net29 net31 b0 vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm9 net29 b0 net31 vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm8 net31 b1 net25 vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm3 g1 net21 net25 vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm2 net21 net13 b1 vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm1 net21 b1 net13 vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm0 net13 b2 net25 vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm15 g0 net29 gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm14 net29 b1 b0 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm13 net29 b0 b1 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm12 net31 b1 gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm5 net21 b1 b2 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm7 g1 net21 gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm6 net21 b2 b1 gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm4 net13 b2 gnd! gnd! n105 w=0.1u l=0.03u nf=1 m=1
v18 b0 gnd! dc=0 pat ( 1.2 0 0 0.1u 0.1u 1u b01010101 )
v17 b1 gnd! dc=0 pat ( 1.2 0 0 0.1u 0.1u 1u b00110011 )
v16 b2 gnd! dc=0 pat ( 1.2 0 0 0.1u 0.1u 1u b00001111 )
v19 net25 gnd! dc=1.5
c29 b2 gnd! c=1p
c28 g1 gnd! c=1p
c27 g0 gnd! c=1p








.tran '1' '18' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(b0) v(b1) v(b2) v(g0) v(g1)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL







.end
```

# Waveforms
![Waveform](https://user-images.githubusercontent.com/90308885/156213745-46591852-3092-4fca-852d-34e30911232c.jpeg)
Input voltage = 1.2V <br />
Supply voltage = 1.5V <br />
Rise time = 0.1u <br />
Fall time = 0.1u <br />

# References
[1] J.Wang, S.Fang and W.Feng, “New EfEcient Designs for XOR and XNOR Functions on the Transistor Level, ,” IEEE Journal on SolidState Circuits, vol. 29, No.7, pp. 780–786,July 1994. <br />
[2] Hanho Lee and G. E. Sobelman, ”New low-voltage circuits for XOR and XNOR,” Proceedings IEEE SOUTHEASTCON ’97. ’Engineering the New Century’, 1997, pp. 225-229, doi:10.1109/SECON.1997.598676. <br />
[3] L. Li and J. Hu, ”A transmission gate flip-flop based on dual-threshold CMOS techniques,” 2009 52nd IEEE International Midwest Symposium on Circuits and Systems, 2009, pp.539-542, doi: 10.1109/MWSCAS.2009.5236037
