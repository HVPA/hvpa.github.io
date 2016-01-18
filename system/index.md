---
layout: page
title: The System
---

To comply with legal and ethical requirements for the clinical and research use of the data in Australia, the system has been designed to maintain the privacy of the patient. This is done through de-identification of the patient and instead, the usage of computed hash-codes. Public/private key technologies are used to protect the transfer of data from the laboratory to the Node.

<h2> What kind of data is collected? </h2>
The data model revolves around the Variant instance: Gene, cDNA/Genome position, and classification of pathogenicity under the 5-class system. Metadata for this instance such as the hash-coded patient, testing date and organisation is also tagged. The data model also provides a number of optional fields to provide context around this instance such as Sample source type, or brief justification of results.

For more information, see <http://www.hvpaustralia.org.au/data/> 

<h2> How is the data collected? </h2>
Laboratories around Australia have a diverse range of systems and databases where variants are stored after clinical reports have been issued. The labour behind parsing, translating terminology and data entry of this information is a time consuming problem. In response to this, the HVP Australia tool chain includes an application called the VariantExporter which can be customised through plugins to fetch data from local data sources and streamline the collection process. A custom plugin can be written to collect data from any source such as LIMS, databases, and Microsoft Excel spreadsheets. The translation of terminology can be automated and removed from the laboratory’s burden.

The VariantExporter is also responsible for de-identification of the patient. Instead of using a patient’s name and other identifying details, a hash-code is generated. An algorithm is used to take the patient’s details and convert it into a sequence of numbers and letters that is irreversible. 

<h2> How does the data gets to the Node? </h2>
Diagnostic Laboratories sign up to participate in the HVP Australian Node. Using the customised VariantExporter tool, a user at the laboratory can choose to upload data to the Node at any time. The VariantExporter will only pick up new instance records that have not already been sent before. 

The data is processed: translation of terms, de-identification of the patient, packaged into XML format and compressed for transfer. The resulting compressed file is encrypted with RSA public/private key technology and sent to the Australian Node.

The Node receives the data and reverses the process: decrypting and uncompressing the data as XML.

A nightly process imports all files received from the previous data into the Node database.

<img alt="The Human Variome Project" src="/img/the-system.jpg">