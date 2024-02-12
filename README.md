# miniswitchpy
- I managed to implement only the first task, the one with the switching table.
- I took the pseudocode and translated it into python.
- Instead, the only thing that would be original would be the verification function if it is a unicast address. After some documentation on the internet, I found the formula of check for the unicast address, if it is 0 or 1. So, the first byte of the MAC address is shifted to the right by 0 bits, although it has no influence on the value, but it is more the clarity of the code.
- A logical "and" operation is performed between the shift result and the value 1, checking if the least significant bit of the first byte is even or odd. How can it be 0 or 1, 0 even, 1 odd.

**The pseudocode:**
```
 # Cadrul F este primit pe portul P
# MAC_Table : Tabela MAC ce face maparea adresa MAC -> port
# Ports : lista tuturor porturilor de pe switch
src = F.SourceAddress
dst = F.DestinationAddress
 
# Am aflat portul pentru adresa MAC src
 
MAC_Table[src] = P
if is_unicast(dst):
    if dst in MAC_Table:
        forward_frame(F, MAC_Table[dst])
    else:
        for o in Ports:
          if o != P:
               forward_frame(F, o)
else:
    # trimite cadrul pe toate celelalte porturi
    for o in Ports:
        if o != P:
            forward_frame(F, o)
```
