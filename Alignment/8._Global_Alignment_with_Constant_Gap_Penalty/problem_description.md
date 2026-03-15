# Global Alignment with Constant Gap Penalty
    
        <nobr></nobr>

## Penalizing Large Insertions and Deletions


In dealing with global alignment in “Global Alignment with Scoring Matrix”, we encountered a linear gap penalty, in
which the insertion or deletion of a gap is penalized by some constant times the length
of the gap.  However, this model is not necessarily the most practical model,
as one large rearrangement could have inserted or 
deleted a long gap in a single step to transform one genetic string into another.

## Problem


In a constant gap penalty, every gap receives some predetermined constant penalty,
regardless of its length. Thus, the insertion or deletion of 1000 contiguous symbols
is penalized equally to that of a single symbol.
**Given:** Two protein strings $s$ and $t$ in FASTA format (each of length at most 1000 aa).
**Return:** The maximum alignment score between $s$ and $t$. Use:



The BLOSUM62 scoring matrix.
Constant gap penalty equal to 5.
