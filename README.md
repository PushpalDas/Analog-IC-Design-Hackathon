# Analog-IC-Design-Hackathon
Cloud Based Hackathon based on fixed parameters provided on analog IC designs.
# Table of contents
- [Abstract](https://github.com/PushpalDas/blob/main.Abstract)
- [Introduction](https://github.com/PushpalDas/blob/main/README.md#introdution)
- [Truth Table of 3 bit binary to gray code converter](https://github.com/PushpalDas/blob/main/README.md#Truth-Table-of-3-bit-binary-to-gray-code-converter) 
- [Reference Circuit](https://github.com/PushpalDas/blob/main/README.md#Reference-Circuit)
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
gates

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

# Reference
![WhatsApp Image 2022-02-19 at 22 52 52](https://user-images.githubusercontent.com/90308885/155963005-f3328bc7-3ef8-401e-9e51-3cb5ea0df0df.jpeg)
 Circuit 

# Waveforms
![WhatsApp Image 2022-02-19 at 22 53 24](https://user-images.githubusercontent.com/90308885/155963128-9e137ebd-4ea5-4f62-abbd-13f0e049877e.jpeg)

# References
[1] J.Wang, S.Fang and W.Feng, “New EfEcient Designs for XOR and XNOR Functions on the Transistor Level, ,” IEEE Journal on SolidState Circuits, vol. 29, No.7, pp. 780–786, July 1994.
[2] Hanho Lee and G. E. Sobelman, ”New low-voltage circuits for XOR and XNOR,” Proceedings IEEE SOUTHEASTCON ’97. ’Engineering the New Century’, 1997, pp. 225-229, doi: 10.1109/SECON.1997.598676.
[3] L. Li and J. Hu, ”A transmission gate flip-flop based on dual-threshold CMOS techniques,” 2009 52nd IEEE International Midwest Symposium on Circuits and Systems, 2009, pp. 539-542, doi: 10.1109/MWSCAS.2009.5236037
