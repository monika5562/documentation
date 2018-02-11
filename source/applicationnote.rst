############################################################
Sequence Variant Analysis (SVA) part I: Byonic™ Searches
############################################################
Marshall Bern, Ph.D., K. Ilker Sen, Ph.D., Eric Carlson, Ph.D., and Chris Becker, Ph.D.
Protein Metrics Inc. www.proteinmetrics.com
June 2016


++++++++++++++++++++++++++++
What's New in this version
++++++++++++++++++++++++++++

---------------------------------------------------------------------
Use of isotropically labeled acid as alkalyting agents
---------------------------------------------------------------------

This version illustrates a new method of searching for sequence variants. Refer to the :ref:`Discussion regarding the use of isotopically labeled iodoacetic acid or iodoacetimide as alkylating agents` section for details.


++++++++++++++++++++++++++++
Benefits summary
++++++++++++++++++++++++++++

•	Best practices for running a sequence variant search 
•	How-to for using Byonic™ software to effectively search for sequence variants, for subsequent inspection and quantification by Byologic® software.

++++++++++++++++++++++++++++
Method
++++++++++++++++++++++++++++

Almost all therapeutic protein data sets include mass spectra from peptides that differ from the corresponding database peptide by one amino acid substitution at some concentration.  Sequence variants may arise from mutations or mistranslations in the host cell line or problems with the bioreactor feed.  Searching for sequence variants is especially challenging, because there are a large number of possible amino acid substitutions, and many of the mass deltas are either exactly or approximately the same as the mass deltas from posttranslational modifications and sample preparation artifacts.  In this application note, we show how to search for sequence variants in biotherapeutics.
Sequence variant analysis aims to identify and quantify all the variant peptides down to very small percentages of their “wild type” (native or expected sequence) counterparts.  Because the protein database is very small for a therapeutic protein, typically only the product plus trypsin or other digestive enzyme and decoys, Byonic running time is not a concern. It is feasible to search for all possible one-AA-substitution peptides in a few minutes.  The challenge is distinguishing the relatively rare true sequence variants from false positives.  
This Application Note focuses on the first step, the Byonic search for SVA.

.. csv-table:: Summary of best practice steps for sequence variant Byonic searches
    :header: "Step", "Detail"
    :widths: 10 30
    
         
            
    "Choice of alkylating agent", "Many amino acid substitutions have the exact same mass difference as the common alkylating agents. We recommend choosing one based on the desired analysis:
    
    *    Ideally, use C13 labeled Iodoacetic acid.
    *    Iodoacetic acid tends to generate fewer over-alkylated peptides than iodoacetamide, and has fewer delta mass overlaps with all possible amino acid substitutions list.
    *    If, however, only single base substitutions that lead to sequence variants will be considered, rather than the entire list, carbamidomethyl may be the desired agent as there are no conflicting masses within this shorter list." 
        "Use a high resolution mass spectrometer", "Use high resolution MS1.  Ideally, also use high resolution MS2.  Make sure the instrument is well calibrated and operating near peak performance."  
        "MSMS Search: Modification rules settings.","Identify artifacts first with Protein Metrics’ Preview™ or Byonic Wildcard Search™.
        
        *    Do not include deamidation in the list of variants (Asn->Asp). Instead include them as named rare1 modifications. Include all the types of non-variant modifications known to be present in your sample, including all the sample preparation artifacts particular to your laboratory. Use rare1 for all modifications and sequence variants except common1 for pyro-glu modifications.
        *    Use common max 1 and rare max 1.
        *    See example in Table 2 for a typical modification list.  Have the sequence variants in the search as rare1 modifications (see Figure 1 below for the full list, and an exemplary short list in Table 3).
        *    A list of modifications for sequence variants is available from Protein Metrics.  This list can be copied from a text editor and pasted into the Modification pop-up box in Byonic.
        *    In addition, for mAbs with N-glycosylation, include the table of 50 N-glycans on the Glycan tab, and check Show all N-glycopeptides on the Advanced tab. Use common1 setting."
        
        
Refer to `ABC-1234 <www.jira.com>`_ for details.
                

.. _Discussion regarding the use of isotopically labeled iodoacetic acid or iodoacetimide as alkylating agents:

----------------------------------------------------------------------------------------------------------------------------------------------------
Discussion regarding the use of isotopically labeled iodoacetic acid or iodoacetimide as alkylating agents
----------------------------------------------------------------------------------------------------------------------------------------------------

We suggest using iodoacetic acid for alkylation of Cysteines because this typically produces fewer sample preparation artifacts compared to iodoacetimide.  In either case however, there are a significant number of confusable masses of sequence variants with alkylation artifacts.  Table 4 below lists confusable masses for unlabeled and C13-labeled alkylations and sequence variants.  Examination of the table shows that for commercially available labeled iodoacetic acid and iodoacetimide, that the single-C13-labeled iodoacetic acid will give the best separation and hence the fewest (or none) confusion with sequence variants.  Note that if a three-C13-labeled iodoacetic acid is available, the +61 modification has no confusable masses with sequence variants.

.. figure:: files_static/images/Picture1.png
        :align: center
        
.. figure:: files_static/images/Picture1.png
        :align: center
        
        List of all possible one-letter sequence variants, for the case of cysteine alkylation by unlabeled iodoacetic acid.  The % symbol signifies a comment line and instances corresponding to deamidation have been commented out (see yellow highlight on the next page).  These variants are pasted into the modification pop-up box (as a single column).  Continued on the next page. 
