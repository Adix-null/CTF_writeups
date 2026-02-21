The log file is base64, which viewed in hexdump 
89504e470d0a1a0a0000000d49484452
is the header of a png, which visually contains the text
7069636F4354467B666F72656E736963735F616E616C797369735F69735F616D617A696E675F35646161346132667D
This is hex, and converting to text reveals the flag
picoCTF{forensics_analysis_is_amazing_5daa4a2f}