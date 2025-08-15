## An idiot's guide to 3RAD libraries by sufflox

Restriction enzymes, of which I have 2 -- a Read-1-enzyme and a Read-2-enzyme.
  * Xba-I is a restriction enzyme that cuts DNA at a specific cut site (the Read-1-site). It creates "sticky ends" compatible with the Read-1-adapter.
  * Eco-R-I is another restriction enzyme that cuts DNA at the Read-2-site. It's sticky ends are compatible with the Read-2-adapter.
  * We also use a third restriction enzyme, Nhe-I, to improve ligation efficiency because the enzyme cuts adapter-dimers, which are formed when adapters ligate to each other instead of DNA.

The Read-1 and -2 adapters are the iTru adapters.
  * ds iTru-Nhe-I is the double-stranded adapter that will stick to Xba-I cut sites. It barcodes the 8 rows (A, B, ... H) on the 96-well plate.
  * ds iTru-EcoR-I is the double-stranded adapter that will stick to EcoR-I cut sites. It barcodes the 12 columns on the 96-well plate.
    
The 8x12=96 combinations of the two adapters generate unique sequences that identify each individual sample on a 96-well plate.

------------------------------------------------------------------------------------------------
...& so on and so forth.

This repo is meant to contain text docs related to the most recent things I'm working on and researching for my msc project at the JBM. The themes are going to vary (3RAD labwork, thoughts and maybe blogposts for my website). 
