---
layout: subpage
title: Data Dictionary
---

<div class="table-responsive">
<table class="table table-condensed table-striped">
  <thead>
    <tr>
      <th scope="col">Table</th>
      <th scope="col">Access<br>
        (Site Only vs Node)<a href="#note1">[1]</a></th>
      <th scope="col">Data Originates From <a href="#note1">[2]</a></th>
      <th scope="col">Mandatory</th>
      <th scope="col">Field Name</th>
      <th scope="col">Description</th>
      <th scope="col">Data Type</th>
      <th scope="col">Value Domain</th>
      <th scope="col">Examples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Patient</td>
      <td>Node</td>
      <td>HVP Auto</td>
      <td>Mandatory</td>
      <td>HashCode</td>
      <td>HVP Codified value of patient to hide patient identity</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Patient</td>
      <td>Node</td>
      <td>Lab Extractor</td>
      <td>Optional</td>
      <td>ResearchHashCode</td>
      <td>HVP Codified value of patient to allow de-identified linkage</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Patient)</td>
      <td>Site only</td>
      <td>Lab</td>
      <td>Mandatory</td>
      <td>PatientID</td>
      <td>Internal ID used within the lab. Only exists within the lab</td>
      <td>-</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Patient)</td>
      <td>Site only</td>
      <td>Clinic/Lab</td>
      <td>Optional</td>
      <td>FirstName</td>
      <td>Only exists within the lab for Research hashcode (GRHANITE)</td>
      <td>-</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Patient)</td>
      <td>Site only</td>
      <td>Clinic/Lab</td>
      <td>Optional</td>
      <td>LastName</td>
      <td>Only exists within the lab for Research hashcode (GRHANITE)</td>
      <td>-</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Patient)</td>
      <td>Site only</td>
      <td>Clinic/Lab</td>
      <td>Optional</td>
      <td>Gender</td>
      <td>Only exists within the lab for Research hashcode (GRHANITE)</td>
      <td>-</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Patient)</td>
      <td>Site only</td>
      <td>Clinic/Lab</td>
      <td>Optional</td>
      <td>DOB</td>
      <td>Only exists within the lab for Research hashcode (GRHANITE)</td>
      <td>-</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Patient)</td>
      <td>Site only</td>
      <td>Clinic/Lab</td>
      <td>Optional</td>
      <td>Postcode</td>
      <td>Only exists within the lab for Research hashcode (GRHANITE)</td>
      <td>-</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Patient)</td>
      <td>Site only</td>
      <td>Clinic/Lab</td>
      <td>Optional</td>
      <td>Digits 5-9 of the Medicare ID</td>
      <td>Only exists within the lab for Research hashcode (GRHANITE)</td>
      <td>-</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>HVP Auto</td>
      <td>Mandatory</td>
      <td>HashCode</td>
      <td>De-identified code of the Test ID</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>HVP Auto</td>
      <td>Mandatory</td>
      <td>VariantID</td>
      <td>The ID of the variant on HVP Node</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Mandatory</td>
      <td>InstanceDate</td>
      <td>Date instance was tested</td>
      <td>DateTime</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>PatientAge</td>
      <td>Age of patient when test was taken</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>RefTestMethodID</td>
      <td>Foreign key to TestMethod</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>RefSampleTissueID</td>
      <td>Foreign key to SampleTissue</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>RefSampleSourceID</td>
      <td>Foreign key to SampleSource</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Mandatory</td>
      <td>RefPathogenicityID</td>
      <td>Foreign key to estimated level of pathogenicity</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>Justification</td>
      <td>Justification by medical scientist</td>
      <td>VARCHAR(65535)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>PubMed</td>
      <td>PubMed Identifier/Data Object Identifier</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>RecordedInDatabase</td>
      <td>Whether it is recorded in disease specific or gene specific</td>
      <td>Boolean</td>
      <td>Yes/No</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>SampleStored</td>
      <td>Whether lab still has sample left</td>
      <td>Boolean</td>
      <td>Yes/No</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Clinic/Lab</td>
      <td>Optional</td>
      <td>PedigreeAvailable</td>
      <td>Whether organisation has pedigree data</td>
      <td>Boolean</td>
      <td>Yes/No</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>VariantSegregatesWithDisease</td>
      <td>Whether pedigreee was consideed during diagnosis of pathogenicity</td>
      <td>Boolean</td>
      <td>Yes/No</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>HistologyStored</td>
      <td>Whether histograms are stored</td>
      <td>Boolean</td>
      <td>Yes/No</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>HVP Auto</td>
      <td>Mandatory</td>
      <td>PatientID</td>
      <td>The ID of the patient on HVP Node</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>VariantInstance</td>
      <td>Node</td>
      <td>HVP Auto</td>
      <td>Mandatory</td>
      <td>Organisation_ID</td>
      <td>The ID of the organisation on HVP Node</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(VariantInstance)</td>
      <td>Site only</td>
      <td>Lab</td>
      <td>Mandatory</td>
      <td>TestID</td>
      <td>Internal to diagnostic lab</td>
      <td>-</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Variant</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>ID</td>
      <td>Internal ID for table</td>
      <td>INT32 (auto)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Variant</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>GeneID</td>
      <td>The ID of the gene on HVP</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Variant</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Mandatory</td>
      <td>cDNA</td>
      <td>As cDNA</td>
      <td>VARCHAR(255)</td>
      <td>HGVS</td>
      <td>c.128delGA</td>
    </tr>
    <tr>
      <td>Variant</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Alternate cDNA</td>
      <td>mRNA</td>
      <td>As mRNA</td>
      <td>VARCHAR(255)</td>
      <td>HGVS</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Variant</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Alternate cDNA</td>
      <td>Genomic</td>
      <td>As genomic sequence</td>
      <td>VARCHAR(255)</td>
      <td>HGVS</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Variant</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Alternate cDNA</td>
      <td>Protein</td>
      <td>As protein sequence</td>
      <td>VARCHAR(255)</td>
      <td>HGVS</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Variant</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>RefVariantClassID</td>
      <td>Foreign key to VariantClass</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Variant</td>
      <td>Node</td>
      <td>Lab</td>
      <td>Optional</td>
      <td>Location</td>
      <td>Exon or intron number</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>1..3099</td>
    </tr>
    <tr>
      <td>Variant</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Optional</td>
      <td>Comments</td>
      <td>By community consensus</td>
      <td>VARCHAR(65535)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Variant</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Optional</td>
      <td>RefPathogenicityID</td>
      <td>By community consensus</td>
      <td>INT32</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Gene</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>ID</td>
      <td>Internal ID for table</td>
      <td>INT32 (auto)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>Gene</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>GeneName</td>
      <td>Standard gene symbol used for gene in HVP system</td>
      <td>VARCHAR(20)</td>
      <td>&nbsp;</td>
      <td>MC1R</td>
    </tr>
    <tr>
      <td>Gene</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>GeneDescription</td>
      <td>Descriptive name for gene</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>melanocortin 1 receptor (alpha melanocyte stimulating hormone receptor)</td>
    </tr>
    <tr>
      <td>Gene</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>RefSeqName</td>
      <td>Name of reference sequence (NCBI's RefSeq project)</td>
      <td>VARCHAR(20)</td>
      <td>&nbsp;</td>
      <td>NM_002386</td>
    </tr>
    <tr>
      <td>Gene</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>RefSeqVer</td>
      <td>Version of reference sequence (RefSeq)</td>
      <td>VARCHAR(20)</td>
      <td>&nbsp;</td>
      <td>3</td>
    </tr>
    <tr>
      <td>Gene</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>RefSeqValidStart</td>
      <td>Date range of when this version of sequence is valid (Start)</td>
      <td>DateTime</td>
      <td>&nbsp;</td>
      <td>1/01/2010</td>
    </tr>
    <tr>
      <td>Gene</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
      <td>RefSeqValidEnd</td>
      <td>Date range of when this version of sequence is valid (End)</td>
      <td>DateTime</td>
      <td>&nbsp;</td>
      <td>31/12/2010</td>
    </tr>
    <tr>
      <td>Organisation</td>
      <td>Node</td>
      <td>HVP Auto</td>
      <td>Mandatory</td>
      <td>HashCode</td>
      <td>De-identified code for organisation</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Organisation)</td>
      <td>HVP Internal</td>
      <td>Lab</td>
      <td>Mandatory</td>
      <td>Name</td>
      <td>Name of diagnostic laboratory</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Organisation)</td>
      <td>HVP Internal</td>
      <td>Lab</td>
      <td>Mandatory</td>
      <td>Address</td>
      <td>Address of diagnostic laboratory</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Organisation)</td>
      <td>HVP Internal</td>
      <td>Lab</td>
      <td>Mandatory</td>
      <td>Email</td>
      <td>Email of laboratory/main contact</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Organisation)</td>
      <td>HVP Internal</td>
      <td>Lab</td>
      <td>Mandatory</td>
      <td>Phone</td>
      <td>Phone of laboratory/main contact</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>(Organisation)</td>
      <td>HVP Internal</td>
      <td>Lab</td>
      <td>Mandatory</td>
      <td>ContactPerson</td>
      <td>Name of main contact person</td>
      <td>VARCHAR(255)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>RefVariantClass</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>ID</td>
      <td>Internal ID for table</td>
      <td>INT32 (auto)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>RefVariantClass</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>VariantClass</td>
      <td>The descript of the variant class</td>
      <td>VARCHAR(20)</td>
      <td>genomic, mitochrondrial</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>RefTestMethod</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>ID</td>
      <td>Internal ID for table</td>
      <td>INT32 (auto)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>RefTestMethod</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>TestMethod</td>
      <td>The name of the test method used</td>
      <td>VARCHAR(20)</td>
      <td>DHPLC, PTT, CCM,…</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>RefPathogenicity</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>ID</td>
      <td>Internal ID for table</td>
      <td>INT32 (auto)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>RefPathogenicity</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>Pathogenicity</td>
      <td>Level of pathogenicity</td>
      <td>VARCHAR(20)</td>
      <td>Class 1 - Certainly not Pathogenic<br>
        Class 2 - Unlikely Pathogenic<br>
        Class 3 - Unknown<br>
        Class 4 - Likely Pathogenic<br>
        Class 5 - Certainly Pathogenic</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>RefSampleTissue</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>ID</td>
      <td>Internal ID for table</td>
      <td>INT32 (auto)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>RefSampleTissue</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>SampleTissue</td>
      <td>Type of sample taken</td>
      <td>VARCHAR(20)</td>
      <td>Blood, tumour tissue...</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>RefSampleSource</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>ID</td>
      <td>Internal ID for table</td>
      <td>INT32 (auto)</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>RefSampleSource</td>
      <td>Node</td>
      <td>HVP</td>
      <td>Mandatory</td>
      <td>SampleSource</td>
      <td>The source of the sample</td>
      <td>VARCHAR(20)</td>
      <td>DNA, g.DNA, RNA...</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>
</div>

<h3> Notes </h3>

<ol>
  <li id="note1">

  Site Only: Only the local site (lab/clinic) may see this data; Node: Visible at the Australian Node; HVP Internal: Held by HVP but not accessible via the Australian Node portal

  </li>
  <li id="note2">

  Lab: Data cames from the laboratory; Clinic: Data originally came from the clinic—however this may be a paper or electronic request which can be captured at the lab; HVP: Data that will be setup by the HVP organisers; HVP Auto: Data that is automatically generated by the system

  </li>
</ol>