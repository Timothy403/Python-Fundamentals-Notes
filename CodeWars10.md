("TTTT") -> ("UUUU")
 ("GCAT") -> ("GCAU")
("GACCGCCGCC") -> ("GACCGCCGCC")

```Python
def dna_to_rna(dna):
    seen = []
    for c in dna:
        if "T" in c:
            seen.append("U")
        else:
            seen.append(c)
    return "".join(seen)    
```
It works but its far from concise, use .replace()
