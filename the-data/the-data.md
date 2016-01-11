The Data
The Australian Node contains information on genetic variants that have been discovered during genetic testing for both diagnostic and research purposes, along with their effects (both known and predicted) on human health.

The data within the Australian Node repositories comes directly from participating laboratories in Australia.

Data upload to the Australian Node repository is initiated by the laboratory staff at their discretion.  When initiated, the HVP Exporter connects to the labs internal Laboratory Information Management System (LIMS) and extracts a defined set of data elements from new records added to the LIMS since the last upload cycle.

Extracted Data Elements
Variant Name	Gene Name
Variant Class	Reference Sequence ID
Variant Location	Test method
Pathogenicity determination	Sample tissue
Date of pathogenicity determination	Sample Source
Age of patient at time of test	Whether lab still has sample left
Justification for pathogenicity determination	Whether organisation has pedigree data/td>
PubMed/DOI ids for supporting evidence	Whether pedigree was considered during diagnosis of pathogenicity
Whether variant is recorded in disease specific or gene specific database	Whether histograms are stored
The data elements required for a submission to the HVPA Node are based primarily on the minimum reporting requirements specified in the National Pathology Accreditation Advisory Council guidelines Requirements for the Medical Testing of Human Nucleic Acids. 

For each variant to be uploaded to the HVPA Node, a "Linkage Key" is generated. These linkage keys are coded identifiers that are generated from a subset of personally identifying information that have been non-reversibly encrypted. This process allows data within the HVPA Node to be linked at the patient level to records in other datasets without using personally identifying information and thus protecting the privacy and confidentiality of patients.

Example Record
VariantInstance
ID	193
HashCode	YWwQFMTwdL4THvE5s09z8jBEdO5lo7aK==
Variant_id	3
InstanceDate	2013-01-01
PatientAge	NULL
TestMethod_id	NULL
SampleTissue_id	NULL
SampleSource_id	NULL
Pathogenicity_id	Class 1 - Certainly not pathogenic
Justification	NULL
PubMed	NULL
RecordedInDatabase	NULL
SampleStored	NULL
PedigreeAvailable	NULL
VariantSegregatesWithDisease	NULL
HistologyStored	NULL
Patient_id	Lar0uXraIRIHI5RO2lmK==
Organisation_id	46dvEpZCg4BAqJgAqEkH
Variant
ID	3
Gene_id	1721
cDNA	c.4987-68A>G
mRNA	NULL
Genomic	g.-38473306A>G
Protein	NULL
VariantClass_id	Genomic
Location	NULL
Comments	NULL
Pathogenicity_id	NULL
Patient
HashCode	Lar0uXraIRIHI5RO2lmK==
Ethnicity_id	Null
Organisation
HashCode	46dvEpZCg4BAqJgAqEkH
Gene
ID	1721
GeneName	BRCA1
GeneDescription	breast cancer 1, early onset
RefSeqName	NM_007294
RefSeqVer	2
RefSeqValidStart	NULL
RefSeqValidEnd	NULL
HGNC_ID	HGNC:1100
AlternateSymbols	RNF53, BRCC1
AlternateNames	BRCA1/BRCA2-containing complex, subunit 1
Chromosome	17q21-q24
PreviousSymbols	 
PreviousNames	 
GenBankName	NG_005905
GenBankVer	1
Entity Relationship Diagram
