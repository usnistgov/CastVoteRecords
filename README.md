# Voting - NIST Special Publication 1500-103 Cast Vote Records Common Data Format Specification Version 1

This repository holds the NIST Special Publication 1500-103 Cast Vote Record (CVR) Common Data Format Specification Version 1 and supporting files. Besides the PDF and Word versions of the specification located in this repository, there is an HTML version at

https://pages.nist.gov/CastVoteRecords

The CVR specification is also available using the following Digital Object Identifier (DOI):

https://doi.org/10.6028/NIST.SP.1500-103

NOTE: the version of the specification located in this repository has some minor documentation corrections that have not been corrected in the DOI version.

The CVR specification supports 3 general use cases:

1. Interoperable exports of CVRs from devices such as scanners, DREs (direct record electronic), or other devices that create CVRs and perform contest rule post-processing. Resultant interoperable import into tabulators, such as election management systems (EMS), or import into auditing systems, or import into adjudication systems.

2. Interoperable exports of aggregated collections of CVRs from aggregating devices such as EMS.

3. Interoperable export of CVRs from adjudication devices.


Please contact [John Wack](mailto:john.wack@nist.gov) or [John Dziurlaj](mailto:john@hiltonroscoe.com) for questions and more information.

## Repo Structure

|Name     |Description                                         |
|---------|----------------------------------------------------|
|CastVoteRecords_UML_Documentation_files|Images of UML classes|
|CastVoteRecords.png|Image of Cast Vote Records UML model          |
|CastVoteRecords_UML_Documentation.md|UML Documentation        |
|NIST.SP.1500-103-rev.docx|Word version of CVR specification|
|**NIST.SP.1500-103-rev.pdf**|PDF version of CVR specification|
|NIST V1.0 - CastVoteRecords.xml|MagicDraw UML Model           |
|**NIST_V0_cast_vote_records.json**|CVR JSON schema                    |
|**NIST_V0_cast_vote_records.xsd**|CVR XML schema                      |
|example_*.xml|Full listing of examples referenced in specification|
