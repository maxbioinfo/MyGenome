# Raw reads single end
To determine the sequence # of raw reads in the single end I did 

```bash
zgrep UFVPY677_1.fq.gz | grep -c 'X' 
```
The number determined was 12973340.

## Number of cleaned reads in single end used for assembly
To find this I did  

```bash
grep -c '@A00261:902:HGC52DSX7:2:' UFVPY677_1_p.fq
```

The number determined was 11458918.


### Total bases in cleaned reads

To find this I did 
```bash 
cat *_p.fq | grep ^@A00261:902:HGC52DSX7:2: -A 1 | grep -v ^@A00261:902:HGC52DSX7:2: | grep -v '-' | grep [ATCG] | wc 
```

The number determined was 3458414260. 


## Pics of Reads before cleaning in fastqc



## Pics of Reads after cleaning in fastqc
