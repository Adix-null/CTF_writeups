Opening the binary file in ghydra from the entry point at adress 0x0010133d it is visible the inputted adress will call a function. Looking at the code there is a function win at adress 0x001012a7.

0x0010133d - 0x001012a7 = 0x96

Subtracting 0x96 from the entry point adress printed in netcat and entering it gives the flag
picoCTF{b4s1c_p051t10n_1nd3p3nd3nc3_f8845f06}