3RAD Libraries with Molecular ID Tags Protocol
(with modifications by Simon Joly, March 2024)


1. Normalize all DNA samples to 20 ng/μL (quantified on Qubit), placing $\geq$20 ng/$\mu$L in plates or strip tubes.  Protocol will work with much less DNA, but $\geq$5 ng/$\mu$L is best.

2. Double Enzyme Digest Recipe (per DNA sample & unique adapter combo):
1.5 &muL  NEB 10x CutSmart Buffer 
5.0 $\mu$L  dH2O
0.5 $\mu$L  XbaI (or another Read1 enzyme)
0.5 $\mu$L  EcoRI-HF (or another Read 2 enzyme)
0.5 $\mu$L  NheI-HF (or another Read 1 adapter dimer cutting enzyme)	
1.0 $\mu$L ds iTru NheI # adapter (5 $\mu$M) (# = A, B, ... H; see Table 2)
1.0 $\mu$L ds iTru EcoRI # adapter (5 $\mu$M) (# = 1, 2, ... 12; see Table 2)
5.0 $\mu$L genomic DNA (20 ng/$\mu$L; if dilute, use more volume & take out water) 

3. Incubate samples at $37^oC$ for 2 hr [Note Simon: This is double the incubation time compared to the original protocol]. in a thermal cycler, then immediately...

4. Add Ligation mix (recipe per sample): 
2.0 $\mu$L dH2O 
1.5 $\mu$L ATP (10 mM); note: rATP, NOT dATP
0.5 $\mu$L 10x Ligase Buffer (ensure components are in solution [warm it up!])
1.0 $\mu$L DNA ligase [100 units/$\mu$L; make from 400 units/$\mu$L stock]
5.0 $\mu$L Total  [makes a grand total of 20 $\mu$L in each tube]

5. Perform 4 cycles of $22^oC$ for 20 min., $37^oC$ for 10 min.), followed by $80^oC$ for 20 min., $10^oC$ forever. [Note Simon: This is two times more cycles of ligation than the original protocol]

6. Pooling step 1:  Using the multi-channel pipette and changing tips each time, skloosh, then take 10 �L from each ligation and add it to a strip tube � thus from a 96-well plate, each tube in the strip will have 120 �L.  Seal the plate with foil, label it well, and freeze it for potential use later.

7. Pooling step 2:  Use and label two new 1.5mL tubes. Into each one, pool 60 �L from each tube of the strip from step 6.  This should yield 480 �L of ligation product into each 1.5 mL tube.  Label one of the 1.5mL tube well and freeze it for potential use later. [Note Simon: if using less DNA, I adjust the volume to purify at the following step to continue the protocol with the same amount of DNA as the original protocol.]

8. Split the pooled ligation products into two new 1.5 mL tubes with 240 �L of pool each (measured as 2 x 120 �L), then add 300 �L of SpeedBeads (i.e. 1.25x speedbeads; measured as 2 x 150 �L).  Purify as normal & resuspend each in 30 �L of dH2O, then combine into one tube (total of 60 �L). [Note Simon: Even if I purify a greater volume of reaction, I resuspend in the same total volume � 60 �L].

9. PCR recipe to add complete Illumina adapters & indexes (6 per ligation plate): 
	10.0 ?L  5x Kapa HiFi Buffer (Kapa Biosystems, Wilmington, MA)
	1.5 ?L  dNTP�s  (10 ?M stock from Kapa kit)
	22.5 ?L  dH2O  (to make final total volume 50�L)
	1.0 ?L  Kapa HiFi DNA Polymerase (1 unit/?L from Kapa kit) 
	5.0 �L  iTru5 8N Primer (5�M -> 0.5 �M final; note zero iTru7 primer) 
	10.0 ?L  Linker ligated DNA fragments from step 8 (placed on magnet).  

1 cycle of:  98?C for 60 sec., 60?C for 30 sec., 72?C for 6 min. Hold at 15?C.

It may be easier to program this: 98?C for 40 sec.; then, 1 cycle of:  98?C for 20 sec., 60?C for 30 sec., 72?C for 60 sec.; followed by 72?C for 5 min. Hold at 15?C.

10. Pool all six reactions from above & purify with speedbeads (1:1.5):  Add 450 �L of SpeedBeads, then adding the 6x50 �L PCR amplicons & sklooshing; purifying as normal, and resuspending in 33 �L dH2O.  

11. PCR recipe to add complete Illumina adapters & indexes (three per ligation plate): 
	10.0 ?L  5x Kapa HiFi Buffer 
	1.5 ?L  dNTP�s  (10 ?M stock from Kapa kit)
	17.5 ?L  dH2O  (to make final total volume 50�L)
	1.0 ?L  Kapa HiFi DNA Polymerase (1 unit/?L from Kapa kit) 
	5.0 �L  P5 Primer (5�M -> 0.5 �M final) 
	5.0 �L  iTru7 Primer(s) (5�M -> 0.5 �M final; Note *details at end of protocol)
	10.0 ?L  Linker ligated DNA fragments from step 10 (placed on magnet).  

Cycle: 98?C for  2 minutes.; then, 20 cycles [Note Simon: Original protocol use 6 cycles] of:  98?C for 20 sec., 60?C for 15 sec., 72?C for 30 sec.; followed by 72?C for 5 min. Hold at 15?C.  [Note: Adjust the number of cycles based on the amount of input DNA, more cycles if less input DNA was used.] 

[Note Simon: You can put 5 - 10 �L on gel at this step to ensure the product has amplified well, and you can do more cycles if needed. See gel image of the 10�L of PCR product after 14 cycles on the right.]

12. Pool all three reactions from above & purify with SpeedBeads (Thermo-Scientific, Waltham, MA, USA) to a 1:1.5 ration, dna:speedbead. Add 225 �L of SpeedBeads, then add the 3x50 �L PCR amplicons & skloosh; purify as normal, and resuspend in 55 �L dH2O, then place on magnet and pull off all liquid (~45 �L), transferring the clean solution to a new labeled tube and leaving the beads behind.

13. Run 5�L on agarose gel to ensure each sample worked. [Note Simon: not necessary if you put on gel after step 11.]

14. Quantify with Qubit, normalize, pool, SpeedBeads (1:1.25, dna:speedbead), and size select on Pippin Prep (525 bp +/- 10%).  [change size as necessary to avoid bright bands; we do not know that choosing a narrow size-range is best]. [Note Simon: For the Pippin Prep, we use internal standards and select a broad range between 450 bp and 650 bp.]

15. Quantify the size-selected libraries with Qubit.

16. Optional step: If the library is not concentrated enough, it is possible to perform a PCR to increase the library concentration. Clean the size-select library with SpeedBeads (1:1.5, dna:speedbead), then perform a PCR (two per library):
	10.0 ?L  5x Kapa HiFi Buffer 
	1.5 ?L  dNTP�s  (10 ?M stock from Kapa kit)
	17.5 ?L  dH2O  (to make final total volume 50�L)
	1.0 ?L  Kapa HiFi DNA Polymerase (1 unit/?L from Kapa kit) 
	5.0 �L  P5 Primer (5�M -> 0.5 �M final) 
	5.0 �L  P7 Primer (5�M -> 0.5 �M final)
	10.0 ?L  Library from step 14 (placed on magnet).  

Cycle: 98?C for  2 minutes.; then, 15 cycles of:  98?C for 20 sec., 60?C for 15 sec., 72?C for 30 sec.; followed by 72?C for 5 min. Hold at 15?C.  [Note Simon: Adjust the number of cycles based on the amount of DNA in the library, more cycles if the library is less concentrated. I used 15 cycles with a Qbit concentration of 0.184 ng/�L]

You can put 4 �L on gel to confirm that it has worked (see gel image).

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





