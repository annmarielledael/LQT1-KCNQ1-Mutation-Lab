# From Gene Mutation to Disease: Investigating How DNA Sequence Changes Affect Protein Products and Human Phenotypes

## 1. Disease Background

Long QT Syndrome Type 1 (LQT1) is a form of Long QT Syndrome associated with pathogenic variants in the KCNQ1 gene. It is characterized by abnormal cardiac repolarization and a prolonged QT interval on an electrocardiogram. The condition can affect the normal electrical activity of the heart and may cause symptoms such as fainting and abnormal heart rhythms.

LQT1 primarily affects cardiac muscle cells because KCNQ1 contributes to potassium ion movement involved in cardiac repolarization. KCNQ1-related LQT1 is usually inherited in an autosomal dominant manner.

## 2. Gene and Normal Protein Function

The gene investigated in this project is **KCNQ1** (potassium voltage-gated channel subfamily Q member 1), located on chromosome 11.

KCNQ1 encodes the Kv7.1 voltage-gated potassium channel protein. In cardiac muscle cells, KCNQ1 contributes to the slowly activating delayed rectifier potassium current (IKs), which helps cardiac cells repolarize after each heartbeat. Proper KCNQ1 function is therefore important for normal cardiac electrical activity.

The reference transcript used in this analysis was **NM_000218.3**, and the reference protein was **NP_000209.2**.

## 3. Documented Mutation

The documented mutation investigated was:

**NM_000218.3:c.5C>G (p.Ala2Gly)**

The variant is a single-nucleotide substitution in which cytosine (C) is changed to guanine (G) at coding position 5. This changes the second codon from GCC to GGC and results in an amino-acid substitution from alanine to glycine at position 2.

The ClinVar Variation accession used was **VCV000431053.3**. The variant is classified as likely pathogenic in the ClinVar record used for this project.

## 4. Hypothesis

I hypothesized that the documented KCNQ1 c.5C>G mutation would change the predicted KCNQ1 protein sequence by replacing alanine with glycine at amino acid position 2. Because the mutation is a single-nucleotide substitution, I expected the reading frame and overall predicted protein length to remain unchanged.

## 5. Methods

The normal human KCNQ1 coding sequence was obtained from the NCBI RefSeq reference transcript **NM_000218.3**. The CDS region used was 92–2122, giving a CDS length of 2031 nucleotides.

The WT CDS was translated using the Galaxy tool **Translate nucleic acid sequences (transseq)** using Frame 1 and the Standard genetic code.

The documented mutation was reproduced manually by changing nucleotide position 5 from C to G in a copy of the WT CDS. The mutant CDS was then translated using the same Galaxy settings.

A separate artificial mutation was also created by deleting three nucleotides from the WT CDS. The artificial mutant was translated and compared with the WT sequence.

The WT and documented mutant protein sequences were compared using a sequence alignment (Galaxy's Needle Tool).

## 6. Results

### Wild-Type Sequence

The WT CDS was **2031 nucleotides** long and produced a predicted protein of **676 amino acids**.

The sequence began with the start codon **ATG** and ended with the stop codon **TGA**. Translation in Frame 1 produced the expected KCNQ1 protein sequence corresponding to reference protein **NP_000209.2**.

The first 10 amino acids were:

**MAAASSPPRA**

The last 10 amino acids were:

**VPRRGPDEGS**

### Documented Mutation

The documented mutation changed one nucleotide:

**C → G at coding position 5**

The mutant CDS remained **2031 nucleotides** long, and the predicted protein remained **676 amino acids** long.

The mutation changed amino-acid position 2:

**Alanine (A) → Glycine (G)**

The reading frame remained unchanged, and no premature stop codon was produced.

The mutant protein began with:

**MGAASSPPRA**

### Protein Alignment

Global alignment of the WT and documented mutant proteins produced:

- Alignment length: 677 positions
- Identity: 676/677 (99.9%)
- Similarity: 676/677 (99.9%)
- Gaps: 0/677 (0.0%)

The first and only amino-acid difference was at position 2, where alanine in the WT protein was replaced by glycine in the mutant protein.

The alignment contains 677 positions because the terminal stop symbol is included in the alignment output. The predicted protein itself remains 676 amino acids long.

### Artificial Mutation

The artificial mutation was a three-nucleotide deletion.

The artificial mutant CDS was **2028 nucleotides** long, compared with 2031 nucleotides for the WT sequence. The predicted protein was **675 amino acids** long.

Because three nucleotides were deleted, the reading frame was preserved. The mutation resulted in the deletion of one amino acid and did not produce a premature stop codon.

## 7. WT versus Mutant Protein Comparison

The documented KCNQ1 mutation affected only one amino acid. Alanine at position 2 was replaced by glycine, while the downstream amino-acid sequence remained aligned with the WT protein.

The artificial three-nucleotide deletion produced a different result. It removed one amino acid but preserved the reading frame. Therefore, the documented substitution and artificial deletion produced different effects on the predicted protein sequence.

## 8. Artificial Mutation Experiment

The artificial mutation demonstrated why the number of nucleotides affected can influence the resulting protein.

Deleting three nucleotides removes one complete codon and therefore preserves the reading frame. In this experiment, the result was a protein that was one amino acid shorter.

In contrast, deleting one or two nucleotides would be expected to shift the reading frame and potentially change many downstream amino acids.

## 9. Molecular Interpretation: Gene → Mutation → Protein → Cellular Effect → Phenotype

The KCNQ1 gene provides instructions for the Kv7.1 potassium channel protein. The documented mutation, NM_000218.3:c.5C>G, changes one nucleotide in the coding sequence. This changes the second codon and produces the amino-acid substitution Ala2Gly.

The computational analysis showed that the reading frame was preserved, no premature stop codon was produced, and the predicted protein remained 676 amino acids long.

KCNQ1 contributes to the IKs potassium current involved in cardiac repolarization. Therefore, a mutation that alters KCNQ1 protein function could potentially affect potassium-channel activity and cardiac repolarization, contributing to the abnormal electrical activity associated with LQT1.

However, the computational sequence analysis alone cannot demonstrate that the specific Ala2Gly substitution changes KCNQ1 channel activity or directly causes the clinical phenotype. Experimental and clinical evidence is needed to establish those specific effects.

## 10. Limitations

This analysis predicts protein sequence changes from DNA sequence changes. It does not directly measure protein expression, protein structure, potassium-channel activity, or cardiac-cell function.

The published sources used in this project provide information about KCNQ1 function and the molecular basis of LQT1, but they do not by themselves demonstrate the specific functional effect of the Ala2Gly substitution in this computational analysis.

Therefore, the predicted protein changes should be distinguished from experimentally demonstrated effects.

## 11. Conclusion

The analysis demonstrated how a single nucleotide change can produce a specific amino acid substitution without changing the reading frame or predicted protein length.

For the KCNQ1 c.5C>G mutation, the predicted change was Ala2Gly, with both the WT and documented mutant proteins remaining 676 amino acids long. The global alignment showed 99.9% identity and no gaps.

The artificial three-nucleotide deletion produced a different result: one amino acid was removed while the reading frame remained unchanged.

Overall, the analysis demonstrates the relationship between DNA sequence changes, codons, predicted protein sequences, and possible molecular consequences. The computational results support the sequence-level changes, while the specific effects on KCNQ1 function and the LQT1 phenotype require experimental and clinical evidence.

## 12. References

1. Wang, Q., et al. (2016). Molecular pathogenesis of long QT syndrome type 1. *Journal of Arrhythmia, 32*(5), 381–388. https://doi.org/10.1016/j.joa.2015.12.006 

2. Brewer, K. R., Kuenze, G., Vanoye, C. G., George, A. L. Jr., Meiler, J., & Sanders, C. R. (2020). Structures Illuminate Cardiac Ion Channel Functions in Health and in Long QT Syndrome. *Frontiers in Pharmacology, 11*, 550. https://doi.org/10.3389/fphar.2020.00550

3. National Center for Biotechnology Information (NCBI). RefSeq transcript **NM_000218.3** and protein **NP_000209.2** for KCNQ1. https://www.ncbi.nlm.nih.gov/clinvar/variation/431053/

4. ClinVar. KCNQ1 variant **NM_000218.3:c.5C>G (p.Ala2Gly)**, Variation accession **VCV000431053.3**. https://www.ncbi.nlm.nih.gov/clinvar/variation/431053/
