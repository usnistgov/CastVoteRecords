# Voting - Cast Vote Records(CVR) CDF Specification

This repository holds the NIST Special Publication 1500-103 Cast Vote Record (CVR) common data format specification and related information and other related information and supporting files. The CVR specification is available using either of the following Digital Object Identifiers (DOI):

1. https://doi.org/10.6028/NIST.SP.1500-103

2. https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.1500-103.pdf


Besides the PDF and Word versions of the specification located in this repository, there is an HTML version being developed at https://pages.nist.gov/CastVoteRecords.

The CVR specification supports 3 general use cases:

1. Interoperable exports of CVRs from devices such as scanners, DREs (direct record electronic), or other devices that create CVRs and perform contest rule post-processing. Resultant interoperable import into tabulators, such as election management systems (EMS), or import into auditing systems, or import into adjudication systems.

2. Interoperable exports of aggregated collections of CVRs from aggregating devices such as EMS.

3. Interoperable export of CVRs from adjudication devices.


Please contact [John Wack](mailto:john.wack@nist.gov) or [John Dziurlaj](mailto:john@hiltonroscoe.com) for questions and more information.

## Repo Structure

|Name     |Description                                         |
|---------|----------------------------------------------------|
|CastVoteRecords.png|Image of Cast Vote Records UML model          |
|CastVoteRecords_UML_Documentation_files|Images of UML classes|
|CastVoteRecords_UML_Documentation.md|UML Documentation        |
|NIST 1500-103 CVR Specification 2019-05-06.docm|Word version of CVR specification|
|**NIST 1500-103 CVR Specification 2019-05-06.pdf**|PDF version of CVR specification|
|NIST 1500-103 CVR Specification 2019-02-08.pdf|Identical to the 05-06 document, needed so that links from Democracy Fund's RLA guides work|
|NIST V1.0 - CastVoteRecords.xml|MagicDraw UML Model           |
|NIST_V0_cast_vote_records.json|CVR JSON schema                    |
|NIST_V0_cast_vote_records.xsd|CVR XML schema                      |
|example_*.xml|Full listing of examples referenced in specification|
