The entry point calls the function FUN_00401921, which validates the inputted password with a check 
if (x == -0x212145453f353f22) ...
Since the number is negative, rewriting it in standart hex form gives
x = 0xdedebabac0cac0de
If correct x is entered, FUN_00401905 computes the salt, which is the flag in this case. FUN_00401905 itself is very simple, it just xors the vlaue with 0x6379626572737072
So to get the flag we can just compute
0xdedebabac0cac0de XOR 0x6379626572737072 = 
0xbda7d8dfb2b9b0ac without running the program

Decompiled code:
```c
undefined8 FUN_00401921(void)

{
  long salt;
  char input_str [128];
  long x;
  
  memset(input_str,0,0x88);
  printf_0("Enter Password: > ");
  FUN_0040b940(PTR_DAT_004be790);
  read(0,input_str,0x100);
  printf_0("x = %lx\n",x);
  salt = FUN_00404f90();
  printf_0("SALT = %lx\n",salt);
  if (x == -0x212145453f353f22) {
    printf_1("Welcome to cybersprint!");
    salt = FUN_00401905(0xdedebabac0cac0de);
    printf_0("FLAG = %lx\n",salt);
  }
  else {
    printf_1("Wrong password!");
  }
  return 0;
}
```