
# Data Propagation Report

- **STAT1** : Number of instructions that hit unique coverpoints and update the signature
- **STAT2** : Number of instructions that hit covepoints which are not unique but still update the signature (completely or partially)
- **STAT3** : Number of instructions that hit a unique coverpoint but do not update the signature completely
- **STAT4** : Number of multiple signature updates for the same coverpoint
- **STAT5** : Number of times the signature was overwritten

| Param                     | Value    |
|---------------------------|----------|
| XLEN                      | 32      |
| TEST_REGION               | [('0x8000013c', '0x8000016a')]      |
| SIG_REGION                | [('0x80003110', '0x80003130', '8 words')]      |
| COV_LABELS                | cm.push      |
| TEST_NAME                 | /media/saravana/Non-os/ACT_Test_Reports/RVOPCODEDECODER/Zcmp/RV32/push/cm.push-01.S/ref.S    |
| Total Number of coverpoints| 17     |
| Total Coverpoints Hit     | 9      |
| Total Signature Updates   | 0      |
| STAT1                     | 5      |
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

|s.no|signature|                        coverpoints                        |          code           |
|---:|---------|-----------------------------------------------------------|-------------------------|
|   1|         |- mnemonic : cm.push<br> - rs1 : x8<br> - imm_val == 0<br> |[0x80000160]:cm.push<br> |
|   2|         |- rs1 : x9<br> - imm_val == 1<br>                          |[0x80000162]:cm.push<br> |
|   3|         |- rs1 : x22<br> - imm_val == 2<br>                         |[0x80000164]:cm.push<br> |
|   4|         |- imm_val == 3<br>                                         |[0x80000166]:cm.push<br> |
|   5|         |- rs1 : x1<br>                                             |[0x80000168]:cm.push<br> |