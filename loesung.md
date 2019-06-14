### FAT Main Memory Requirements
a)  250*1024*1024 (KB) -> 262.144.000 Blocks 

b)  As many as there are Blocks: 262.144.000 

c)  log2(Block Count) = log2(262.144.000) = 27,96 ~28 Next higher power of 2, wich is *32 Bit*.

d)  (EntrySize * Block Count) / 8 (Because it is in Bit, we need Byte) = 1.048.576.000 /1024/1024 == 1000 MB (a little less than 1GB)

### Random Acces of Files
a)  107834590 / 1024 (We know the Block# now) = 105308
    107834590 % 1024 (We know the Offset in the Block itself) = 222 Adress in the Block
    
    10 = Direct Blocks = 10
    1*256 =One Indirect= 256
    1*256*256 = DIB    = 65536
    1*256*256*256 = TIP= 16777216 => Block# is 105308, it has to be here
    
    
    
    
    
b)  107834590 / 1024 (We know the Block# now) = 105307.2168 (Blocks are not splitable, it is the **105308th Block**)
