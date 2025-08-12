3RAD Libraries with Molecular ID Tags Protocol\
(with modifications by Simon Joly, March 2024)


1. Normalize all DNA samples to 20 ng/μL (quantified on Qubit), placing $\geq$20 ng/μL in plates or strip tubes.  Protocol will work with much less DNA, but $\geq$5 ng/μL is best.

2. Double Enzyme Digest Recipe (per DNA sample & unique adapter combo):  
1.5 μL  NEB 10x CutSmart Buffer\
5.0 μL  dH2O\
0.5 μL  XbaI (or another Read1 enzyme)\
0.5 μL  EcoRI-HF (or another Read 2 enzyme)\
0.5 μL  NheI-HF (or another Read 1 adapter dimer cutting enzyme)\
1.0 μL ds iTru NheI # adapter (5 μM) (# = A, B, ... H; see Table 2)\
1.0 μL ds iTru EcoRI # adapter (5 μM) (# = 1, 2, ... 12; see Table 2)\
5.0 μL genomic DNA (20 ng/μL; if dilute, use more volume & take out water)

4. Incubate samples at $37^oC$ for 2 hr [Note Simon: This is double the incubation time compared to the original protocol]. in a thermal cycler, then immediately...

5. Add Ligation mix (recipe per sample):\
2.0 μL dH2O\
1.5 μL ATP (10 mM); note: rATP, NOT dATP\
0.5 μL 10x Ligase Buffer (ensure components are in solution [warm it up!])\
1.0 μL DNA ligase [100 units/μL; make from 400 units/μL stock]\
5.0 μL Total  [makes a grand total of 20 μL in each tube]

6. Perform 4 cycles of $22^oC$ for 20 min., $37^oC$ for 10 min.), followed by $80^oC$ for 20 min., $10^oC$ forever. [Note Simon: This is two times more cycles of ligation than the original protocol]

7. Pooling step 1:  Using the multi-channel pipette and changing tips each time, skloosh, then take 10 μL from each ligation and add it to a strip tube. Thus, from a 96-well plate, each tube in the strip will have 120 μL. Seal the plate with foil, label it well, and freeze it for potential use later.

8. Pooling step 2:  Use and label two new 1.5 mL tubes. Into each one, pool 60 μL from each tube of the strip from step 6.  This should yield 480 μL of ligation product into each 1.5 mL tube. Freeze one of the 1.5 mL tubes for potential use later. [Note Simon: if using less DNA, I adjust the volume to purify at the following step to continue the protocol with the same amount of DNA as the original protocol.]

9. Split the pooled ligation products into two new 1.5 mL tubes with 240 μL of pool each (measured as 2 x 120 μL), then add 300 μL of SpeedBeads (i.e. 1.25x speedbeads; measured as 2 x 150 μL).  Purify as normal & resuspend each in 30 μL of dH2O, then combine into one tube (total of 60 μL). [Note Simon: Even if I purify a greater volume of reaction, I resuspend in the same total volume i.e. 60 μL].

10. PCR recipe to add complete Illumina adapters & indexes (6 per ligation plate):\
	10.0 μL  5x Kapa HiFi Buffer (Kapa Biosystems, Wilmington, MA)\
	1.5 μL  dNTPs  (10 μM stock from Kapa kit)\
	22.5 μL  dH2O  (to make final total volume 50μL)\
	1.0 μL  Kapa HiFi DNA Polymerase (1 unit/μL from Kapa kit)\
	5.0 μL  iTru5 8N Primer (5 μM -> 0.5 μM final; note zero iTru7 primer)\
	10.0 μL  Linker ligated DNA fragments from step 8 (placed on magnet).  

1 cycle of:  $98^oC$ for 60 sec., $60^oC$ for 30 sec., $72^oC$ for 6 min. Hold at $15^oC$.

It may be easier to program this: $98^oC$ for 40 sec.; then, 1 cycle of:  $98^oC$ for 20 sec., $60^oC$ for 30 sec., $72^oC$ for 60 sec.; followed by $72^oC$ for 5 min. Hold at $15^oC$.

10. Pool all six reactions from above & purify with speedbeads (1:1.5):  Add 450 μL of SpeedBeads, then adding the 6x50 μL PCR amplicons & sklooshing; purifying as normal, and resuspending in 33 μL dH2O.  

11. PCR recipe to add complete Illumina adapters & indexes (three per ligation plate):\
	10.0 μL  5x Kapa HiFi Buffer\
	1.5 μL  dNTPs  (10 μM stock from Kapa kit)\
	17.5 μL  dH2O  (to make final total volume 50μL)\
	1.0 μL  Kapa HiFi DNA Polymerase (1 unit/μL from Kapa kit)\
	5.0 μL  P5 Primer (5 μM -> 0.5 μM final)\
	5.0 μL  iTru7 Primer(s) (5 μM -> 0.5 μM final; Note *details at end of protocol)\
	10.0 μL  Linker ligated DNA fragments from step 10 (placed on magnet).  

Cycle: $98^oC$ for  2 minutes.; then, 20 cycles [Note Simon: Original protocol use 6 cycles] of:  $98^oC$ for 20 sec., $60^oC$ for 15 sec., $72^oC$ for 30 sec.; followed by $72^oC$ for 5 min. Hold at $15^oC$.  [Note: Adjust the number of cycles based on the amount of input DNA, more cycles if less input DNA was used.] 

[Note Simon: You can put 5 - 10 μL on gel at this step to ensure the product has amplified well, and you can do more cycles if needed. See gel image of the 10μL of PCR product after 14 cycles on the right.]

12. Pool all three reactions from above & purify with SpeedBeads (Thermo-Scientific, Waltham, MA, USA) to a 1:1.5 ration, dna:speedbead. Add 225 μL of SpeedBeads, then add the 3x50 μL PCR amplicons & skloosh; purify as normal, and resuspend in 55 μL dH2O, then place on magnet and pull off all liquid (~45 μL), transferring the clean solution to a new labeled tube and leaving the beads behind.

13. Run 5μL on agarose gel to ensure each sample worked. [Note Simon: not necessary if you put on gel after step 11.]

14. Quantify with Qubit, normalize, pool, SpeedBeads (1:1.25, dna:speedbead), and size select on Pippin Prep (525 bp +/- 10%).  [change size as necessary to avoid bright bands; we do not know that choosing a narrow size-range is best]. [Note Simon: For the Pippin Prep, we use internal standards and select a broad range between 450 bp and 650 bp.]

15. Quantify the size-selected libraries with Qubit.

16. Optional step: If the library is not concentrated enough, it is possible to perform a PCR to increase the library concentration. Clean the size-select library with SpeedBeads (1:1.5, dna:speedbead), then perform a PCR (two per library):\
	10.0 μL  5x Kapa HiFi Buffer\
	1.5 μL  dNTPs  (10 μM stock from Kapa kit)\
	17.5 μL  dH2O  (to make final total volume 50μL)\
	1.0 μL  Kapa HiFi DNA Polymerase (1 unit/μL from Kapa kit)\ 
	5.0 μL  P5 Primer (5 μM -> 0.5 μM final)\
	5.0 μL  P7 Primer (5 μM -> 0.5 μM final)\
	10.0 μL  Library from step 14 (placed on magnet).  

Cycle: $98^oC$ for  2 minutes.; then, 15 cycles of:  $98^oC$ for 20 sec., $60^oC$ for 15 sec., $72^oC$ for 30 sec.; followed by $72^oC$ for 5 min. Hold at $15^oC$.  [Note Simon: Adjust the number of cycles based on the amount of DNA in the library, more cycles if the library is less concentrated. I used 15 cycles with a Qbit concentration of 0.184 ng/μL]

You can put 4 μL on gel to confirm that it has worked (see gel image).

Mix the two PCR reactions, SpeedBeads (1:1.25, dna:speedbead).

Quantify the cleaned libraries with Qubit (and qPCR).


17. Run an agarose gel on each library to make sure it looks ok.

18. Mix libraries in appropriate proportions following the sequencing facilities requirements and send for sequencing.


Special notes & considerations:

*How many iTru7 primers to use (step 11) will vary depending on how many plates will be pooled together for sequencing.  If you are running:
1) ?12 plates in (or no single plate you produce will take up ?10% of) a HiSeq lane or NextSeq/MiSeq/MiniSeq/NovaSeq run, then use a single iTru7 primer for all 3 PCR reactions.  This will make your life easiest.
2) Only a few plates in a HiSeq lane or NextSeq/MiSeq/MiniSeq/NovaSeq run, then you will want to use multiple iTru7s.  In general, you need base diversity of the indexes to be complex for them to sequence correctly.  Read the note for a single plate of samples, and use the index diversity calculator for your scenario.
3) A single plate of samples in a HiSeq lane or NextSeq/MiSeq/MiniSeq/NovaSeq run, then either use 3 different iTru7�s that you verify can sequence together correctly (i.e., by using the index diversity calculator), or by using pools of iTru7 primers to yield a full set of 12 (we do not know if it is best to use 3 different groups of 4 or the same group of 12 in all 3 PCRs).  It may seem stupid to do this because you will demultiplex then repool (concatenate) the reads back together, but this is necessary to generate usable iTru7 index data, which then behave appropriately in stacks and ipyrad.



Dept. Environmental Health Science
EHS Bldg., 150 East Green
Athens, GA  30602-2102


EHS DNA Lab


Telephone (706) 583-0662
Fax (706) 542-7472
http://baddna.uga.edu





