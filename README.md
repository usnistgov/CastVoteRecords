# Voting - Cast Vote Records(CVR) CDF Specification

This directory holds cast vote record (CVR) specification common data format and related information and files that are being created by NIST and collaborators.  

The CVR specification supports 3 general use cases:

1. Interoperable exports of CVRs from devices such as scanners, DREs (direct record electronic), or other devices that create CVRs and perform contest rule post-processing. Resultant interoperable import into tabulators, such as election management systems (EMS), or import into auditing systems, or import into adjudication systems.

2. Interoperable exports of aggregated collections of CVRs from aggregating devices such as EMS.

3. Interoperable export of CVRs from adjudication devices.

The CVR specification is complete and now being published as NIST Special Publication 1500-103.  

The nist-pages branch holds documentation files for an upcoming HTML version located on https://pages.nist.gov/CastVoteRecords.

Contact [John P. Wack](mailto:john.wack@nist.gov) for questions and more information.

## Repo Structure

|Name     |Description                                         |
|---------|----------------------------------------------------|
|**CastVoteRecords_UML_Documentation_files**|Images of UML classes|
|CastVoteRecords_UML_Documentation.md|UML Documentation        |
|CastVoteRecords.png|Image of Cast Vote Records model          |
|NIST 1500-103 CVR Specification 2019-05-06.docm|Word version of CVR specification|
|NIST 1500-103 CVR Specification 2019-05-06.pdf|PDF version of CVR specification|
|NIST 1500-103 CVR Specification 2019-02-08.pdf|Identical to the 05-06 document, needed so that links from Democracy Fund's RLA guides work|
|example_*.xml|Full listing of examples referenced in specification|
|NIST V1.0 - CastVoteRecords.xml|MagicDraw UML Model           |
|NIST_V0_cast_vote_records.json|JSON Schema                    |
|NIST_V0_cast_vote_records.xsd|XML Schema                      |
