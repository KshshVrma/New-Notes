=sum(a1:a5)
=average(a1:a5)
=if(c4>100,"yes","no')
=concatenate(a1," ",b1)
=countif(c1:c100,">90")
=LEN(A1)
=Trim(a1)
=round(a2,2)// this rounds to 2 decimal points.

=VLOOKUP(102, A2:B4, 2, FALSE)

**Meaning of each part:**

- `102` → What you are searching for (Employee ID 102)
    
- `A2:B4` → Where you are searching (the table)
    
- `2` → Column number from which to get the result (2nd column = Name)
    
- `FALSE` → Exact match (only find exactly 102, not something similar)



to apply the formulas, just control + double click at the right corner of the excel column
this will apply the formula across all the rows in that particular column