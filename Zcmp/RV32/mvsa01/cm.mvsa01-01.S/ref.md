
# Data Propagation Report

- **STAT1** : Number of instructions that hit unique coverpoints and update the signature
- **STAT2** : Number of instructions that hit covepoints which are not unique but still update the signature (completely or partially)
- **STAT3** : Number of instructions that hit a unique coverpoint but do not update the signature completely
- **STAT4** : Number of multiple signature updates for the same coverpoint
- **STAT5** : Number of times the signature was overwritten

| Param                     | Value    |
|---------------------------|----------|
| XLEN                      | 32      |
| TEST_REGION               | [('0x80000000', '0x80000018')]      |
| SIG_REGION                | [('0x80003110', '0x80003140', '12 words')]      |
| COV_LABELS                | cm.mvsa01      |
| TEST_NAME                 | /media/saravana/Non-os/ACT_Test_Reports/Zcmp/RV32/mvsa01/cm.mvsa01-01.S/ref.S    |
| Total Number of coverpoints| 17     |
| Total Coverpoints Hit     | 17      |
| Total Signature Updates   | 0      |
| STAT1                     | 8      |
| STAT2                     | 0      |
| STAT3                     | 0     |
| STAT4                     | 0     |
| STAT5                     | 0     |

## Details for STAT2:

```


```

## Details of STAT3

```


```

## Details of STAT4:

```

```

## Details of STAT5:



## Details of STAT1:

- The first column indicates the signature address(es) and the data at that location in hexadecimal in the following format:
  ```
  [Address1]
  Data1

  [Address2]
  Data2

  ...
  ```

- The second column captures all the coverpoints which have been captured by that particular signature location

- The third column captures all the insrtuctions since the time a coverpoint was
  hit to the point when a store to the signature was performed. Each line has
  the following format:
  ```
  [PC of instruction] : mnemonic
  ```
- The order in the table is based on the order of signatures occuring in the
  test. These need not necessarily be in increasing or decreasing order of the
  address in the signature region.

|s.no|signature|                       coverpoints                       |           code            |
|---:|---------|---------------------------------------------------------|---------------------------|
|   1|         |- mnemonic : cm.mvsa01<br> - rs1 : s6<br> - rs2 : s1<br> |[0x80000008]:cm.mvsa01<br> |
|   2|         |- rs1 : s1<br> - rs2 : s0<br>                            |[0x8000000a]:cm.mvsa01<br> |
|   3|         |- rs1 : s0<br> - rs2 : s4<br>                            |[0x8000000c]:cm.mvsa01<br> |
|   4|         |- rs1 : s5<br> - rs2 : s6<br>                            |[0x8000000e]:cm.mvsa01<br> |
|   5|         |- rs1 : s7<br> - rs2 : s3<br>                            |[0x80000010]:cm.mvsa01<br> |
|   6|         |- rs1 : s4<br> - rs2 : s5<br>                            |[0x80000012]:cm.mvsa01<br> |
|   7|         |- rs1 : s2<br> - rs2 : s7<br>                            |[0x80000014]:cm.mvsa01<br> |
|   8|         |- rs1 : s3<br> - rs2 : s2<br>                            |[0x80000016]:cm.mvsa01<br> |
