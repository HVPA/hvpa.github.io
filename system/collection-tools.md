---
layout: subpage
title: Collection Tools
---

##HVP Exporter

Data from participating laboratories in Australia is submitted to the HVPA Node repository through the use of a special collection tool: the HVPA Exporter. The HVPA Exporter was developed by HVPA under the NeAT grant scheme and is owned by the HVPA.  This tool is provided by HVPA free to participating laboratories and provides connection directly to the existing laboratory information system (LIMS) already in use at the participating laboratory and mediates the secure data transfer from the laboratory’s computer network to the HVPA Node repository.

The HVP Exporter is a lightweight tool that can be installed on a desktop computer within the laboratory network (for example, on the primary workstation used by the senior medical scientist). Administrator privileges are not required for installation or operation of the tool. If desired by the laboratory, the HVPA Exporter can also be installed on a virtual machine that has only a minimal set of security privileges, effectively segregating the tool from the remainder of the network.

The specific connection parameters for each laboratory’s LIMS are encoded in a configuration plug-in that is developed by the HVPA development team with guidance from the laboratory staff. This plug-in architecture allows new laboratory sites to be connected in a rapid manner.

Data upload to the HVPA Node repository is initiated by the laboratory staff at their discretion.  When initiated, the HVP Exporter connects to the LIMS and extracts new data added since the last upload cycle. The Exporter extracts only a defined set of data elements from the LIMS and packages them into an XML file for transport to the HVPA Node. The data elements required for a submission to the HVPA Node are based primarily on the minimum reporting requirements specified in the National Pathology Accreditation Advisory Council guidelines Requirements for the Medical Testing of Human Nucleic Acids.  During the packaging process, the Exporter will alert the user to any errors it encounters in the way that the data elements are described, for example if a variant is named incorrectly. Upon completion, a complete list of the data to be uploaded is presented to the user for final review and confirmation. If desired, the user can set individual records to be excluded from the upload.

##HVP Importer

The HVP Importer is the complimentary tool to the HVP Exporter. It sits on the HVPA Node server and receives all incoming XML files from the participating laboratories. Upon receiving a file, the Importer decrypts the file and inserts the data into the repository database. In doing so, the Importer maps any variants described by the submitting laboratory using a reference sequence that differs from the reference sequence used by the HVPA Node to the correct sequence.