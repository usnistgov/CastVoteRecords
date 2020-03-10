# National Institute of Standards and Technology (NIST) Special Publication 1500-103, Cast Vote Records Common Data Format Specification Version 1.0

**March 2020**

**The following is an excerpt from the SP 1500-103 specification. It contains the specification's executive summary and class documentation.**

The complete publication including JSON and XML schemas is available free of charge from:

<https://github.com/usnistgov/CastVoteRecords>

# Executive Summary

This document presents an interoperable, common data format specification for cast vote records (CVR), which are produced by vote-capture devices such as ballot scanners.  A CVR is an electronic record of a voter’s selections, with usually one CVR created per sheet (page) of a ballot.  Election results are produced by tabulating the collection of CVRs, and audits can be done by comparisons of the paper ballots or paper records of voter selections against the CVRs.

This specification supports three general use cases for CVRs:

- Interoperable exports of CVRs from devices such as scanners for import into tabulators, election management systems (EMS), or auditing systems.
- Interoperable exports of aggregated collections of CVRs from aggregating devices such as election management systems.
- Update of CVRs after adjudication.

The purpose of this specification is to provide an interoperable, non-proprietary data exchange format in JavaScript Object Notation (JSON) and eXtensible Markup Language (XML) for CVRs so as to promote greater transparency to voting records produced by vote-capture devices, and to facilitate the exchange of CVRs with other devices that operate upon CVRs regardless of device manufacturer.

The specification includes a UML (Unified Markup Language) model and references XML (eXtensible Markup Language) and JSON (JavaScript Object Notation) schemas that were created from the UML model.

There are many complex operations performed by voting devices when voters submit their paper ballots to be scanned.  These operations are mostly invisible to voters but are necessary to determine whether contest selections have been marked adequately and whether voter intent is reflected by what is marked on the ballot.  This specification includes the necessary detail to capture these operations so that CVRs can be better audited and adjudicated as necessary to include write-in candidates or other issues.

This specification is geared towards the following audiences:

- Election officials
- Voting equipment manufacturers
- Election analysts and auditors
- Election-affiliated organizations
- The public

# Table of Contents

- Table of Contents
  - Enumerations
    - *The **[AllocationStatus](#_18_5_3_43701b0_1533322047899_321573_5682)** Enumeration*
    - *The **[CastVoteRecordVersion](#_18_0_2_6340208_1488984734564_983877_4662)** Enumeration*
    - *The **[ContestSelectionStatus](#_18_0_5_43401a7_1475850153090_186243_4311)** Enumeration*
    - *The **[ContestStatus](#_18_0_5_43401a7_1475850124791_123384_4291)** Enumeration*
    - *The **[CVRStatus](#_18_0_2_6340208_1472159006307_546162_4628)** Enumeration*
    - *The **[CVRType](#_18_0_2_6340208_1532543997676_592413_4694)** Enumeration*
    - *The **[HashType](#_18_0_2_6340208_1485894679180_11599_4655)** Enumeration*
    - *The **[IdentifierType](#_17_0_2_4_f71035d_1425061188508_163854_2613)** Enumeration*
    - *The **[IndicationStatus](#_19_0_43701b0_1541430872294_37549_5007)** Enumeration*
    - *The **[PositionStatus](#_18_0_2_6340208_1485894157707_572874_4551)** Enumeration*
    - *The **[ReportingUnitType](#_17_0_2_4_f71035d_1431607637366_785815_2242)** Enumeration*
    - *The **[ReportType](#_18_0_5_43401a7_1483727563257_179426_4343)** Enumeration*
    - *The **[VoteVariation](#_18_0_5_43401a7_1483727021192_184103_4291)** Enumeration*
  - Classes
    - *The **[Annotation](#_18_0_5_43401a7_1475856712376_208252_4416)** Class*
    - *The **[BallotMeasureContest](#_17_0_2_4_78e0236_1389366932057_929676_2783)** Class*
    - *The **[BallotMeasureSelection](#_17_0_2_4_78e0236_1389372163799_981952_2926)** Class*
    - *The **[Candidate](#_17_0_2_4_78e0236_1389366272694_544359_2440)** Class*
    - *The **[CandidateContest](#_17_0_2_4_78e0236_1389366970084_183781_2806)** Class*
    - *The **[CandidateSelection](#_17_0_2_4_d420315_1392145640524_831493_2562)** Class*
    - *The **[CastVoteRecordReport](#_17_0_2_4_78e0236_1389366195564_913164_2300)** Class*
    - *The **[Code](#_17_0_2_4_f71035d_1430405712653_451634_2410)** Class*
    - *The **[Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400)** Class*
    - *The **[ContestSelection](#_17_0_2_4_78e0236_1389372124445_11077_2906)** Class*
    - *The **[CVR](#_18_0_2_6340208_1532543460307_914551_4600)** Class*
    - *The **[CVRContest](#_18_0_2_6340208_1469203058990_306165_4565)** Class*
    - *The **[CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292)** Class*
    - *The **[CVRSnapshot](#_17_0_2_4_78e0236_1389366224561_797289_2360)** Class*
    - *The **[CVRWriteIn](#_18_0_2_6340208_1485892911278_166697_4594)** Class*
    - *The **[Election](#_17_0_2_4_f71035d_1426101822599_430942_2209)** Class*
    - *The **[File](#_18_0_2_6340208_1485284639717_497586_4548)** Class*
    - *The **[FractionalNumber](#_19_0_43701b0_1556049559972_974781_5102)** Class*
    - *The **[GpUnit](#_17_0_2_4_78e0236_1389366233346_42391_2380)** Class*
    - *The **[Hash](#_18_0_2_6340208_1485894593826_736413_4615)** Class*
    - *The **[Image](#_18_0_2_6340208_1485284639720_737438_4549)** Class*
    - *The **[ImageData](#_18_0_2_6340208_1485894533655_402033_4588)** Class*
    - *The **[Party](#_17_0_2_4_78e0236_1389366278128_412819_2460)** Class*
    - *The **[PartyContest](#_17_0_2_4_d420315_1393514218965_55008_3144)** Class*
    - *The **[PartySelection](#_17_0_2_4_f71035d_1426519980658_594892_2511)** Class*
    - *The **[ReportingDevice](#_17_0_2_4_78e0236_1389798013459_389380_4178)** Class*
    - *The **[RetentionContest](#_18_0_2_6340208_1425646217522_163181_4554)** Class*
    - *The **[SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635)** Class*

## Enumerations

### <a name="_18_5_3_43701b0_1533322047899_321573_5682"></a>*The **AllocationStatus** Enumeration*

![Image of AllocationStatus](CastVoteRecords_UML_Documentation_files/18_5_3_43701b0_1533322047923_796623_5683.png)

![Image of Alloca](Pics/media/18_5_3_43701b0_1533322047923_796623_5683.png)

![](Pics/media/_qw.png)

Used in [SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635)::[IsAllocable](#_18_0_2_6340208_1532546142492_921207_4764) to indicate whether the [SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635)::[NumberVotes](#_18_0_2_6340208_1485892992408_339917_4637) should be allocated to the underlying contest option counter.

Name | Value
---- | -----
`no`|To not allocate votes to the contest option's accumulator.
`unknown`|When the decision to allocate votes is unknown, such as when the adjudication is needed.
`yes`|To allocate votes to the contest option's accumulator.

### <a name="_18_0_2_6340208_1488984734564_983877_4662"></a>*The **CastVoteRecordVersion** Enumeration*

![Image of CastVoteRecordVersion](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1488984734567_410041_4663.png)

To identify the version of the CVR specification being used, i.e., version 1.0.0. This will need to be updated for different versions of the specification.

Name | Value
---- | -----
`1.0.0`|Fixed value for the version of this specification.

### <a name="_18_0_5_43401a7_1475850153090_186243_4311"></a>*The **ContestSelectionStatus** Enumeration*

![Image of ContestSelectionStatus](CastVoteRecords_UML_Documentation_files/_18_0_5_43401a7_1475850153092_221720_4312.png)

Used in [CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292)::[Status](#_18_0_5_43401a7_1475850275266_189599_4334) to identify the status of a contest selection in the CVR.

Name | Value
---- | -----
`generated-rules`|To indicate that the contest selection was generated per contest rules.
`invalidated-rules`|To indicate that the contest selection was invalidated by the generating device because of contest rules.
`needs-adjudication`|To indicate that the contest selection was flagged by the generating device for adjudication.
`other`|Used in conjunction with CVRContestSelection::OtherStatus when no other value in this enumeration applies.

### <a name="_18_0_5_43401a7_1475850124791_123384_4291"></a>*The **ContestStatus** Enumeration*

![Image of ContestStatus](CastVoteRecords_UML_Documentation_files/_18_0_5_43401a7_1475850124799_533420_4292.png)

Used in [CVRContest](#_18_0_2_6340208_1469203058990_306165_4565)::[Status](#_18_0_5_43401a7_1475850227700_908488_4330) to identify the status of a contest in which contest selection(s) were made.

Name | Value
---- | -----
`invalidated-rules`|To indicate that the contest has been invalidated by the generating device because of contest rules.
`not-indicated`|For a CVRContest with no SelectionPosition, i.e. to specify the position contains no marks or other indications.
`overvoted`|To indicate that the contest was overvoted.
`undervoted`|To indicate that the contest was undervoted.
`other`|Used in conjunction with CVRContest::OtherStatus when no other value in this enumeration applies.

### <a name="_18_0_2_6340208_1472159006307_546162_4628"></a>*The **CVRStatus** Enumeration*

![Image of CVRStatus](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1472159006313_115999_4629.png)

Used in [CVRSnapshot](#_17_0_2_4_78e0236_1389366224561_797289_2360)::[Status](#_18_0_2_6340208_1472158928951_402259_4603) to identify the status of the CVR.

Name | Value
---- | -----
`needs-adjudication`|To indicate that the CVR needs to be adjudicated.
`other`|Used in conjunction with CVRSnapshot::OtherStatus when no other value in this enumeration applies.

### <a name="_18_0_2_6340208_1532543997676_592413_4694"></a>*The **CVRType** Enumeration*

![Image of CVRType](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1532543997679_592668_4695.png)

Used in [CVRSnapshot](#_17_0_2_4_78e0236_1389366224561_797289_2360)::[Type](#_18_0_2_6340208_1532543968111_779654_4689) to indicate the type of snapshot.

Name | Value
---- | -----
`interpreted`|Has been adjudicated.
`modified`|After contest rules applied.
`original`|As scanned, no contest rules applied.


### <a name="_18_0_2_6340208_1485894679180_11599_4655"></a>*The **HashType** Enumeration*

![Image of HashType](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1485894679181_566848_4656.png)

Used in [Hash](#_18_0_2_6340208_1485894593826_736413_4615)::[Type](#_18_0_2_6340208_1485894641846_811323_4646) to indicate the type of hash being used for an image file.

Name | Value
---- | -----
`md6`|To indicate that the MD6 message digest algorithm is being used.
`sha-256`|To indicate that the SHA 256-bit signature is being used.
`sha-512`|To indicate that the SHA 512-bit (32-byte) signature is being used.
`other`|Used in conjunction with Hash::OtherType when no other value in this enumeration applies.

### <a name="_17_0_2_4_f71035d_1425061188508_163854_2613"></a>*The **IdentifierType** Enumeration*

![Image of IdentifierType](CastVoteRecords_UML_Documentation_files/_17_0_2_4_f71035d_1425061188510_56434_2614.png)

Used in [Code](#_17_0_2_4_f71035d_1430405712653_451634_2410)::[Type](#_17_0_2_4_f71035d_1430405763078_743585_2433) to indicate the type of code/identifier being used.

Name | Value
---- | -----
`fips`|To indicate that the identifier is a FIPS code.
`local-level`|To indicate that the identifier is from a local-level scheme, i.e., unique to a county or city.
`national-level`|To indicate that the identifier is from a national-level scheme other than FIPS or OCD-ID.
`ocd-id`|To indicate that the identifier is from the OCD-ID scheme.
`state-level`|To indicate that the identifier is from a state-level scheme, i.e., unique to a particular state.
`other`|Used in conjunction with Code::OtherType when no other value in this enumeration applies.

### <a name="_19_0_43701b0_1541430872294_37549_5007"></a>*The **IndicationStatus** Enumeration*

![Image of IndicationStatus](CastVoteRecords_UML_Documentation_files/_19_0_43701b0_1541430872330_109394_5014.png)

Used in [SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635)::[HasIndication](#_19_0_43701b0_1541095481007_618279_4996) to identify whether a selection indication is present.


Name | Value
---- | -----
`no`|There is no selection indication.
`unknown`|It is unknown whether there is a selection indication, e.g., used for ambiguous marks.
`yes`|There is a selection indication present.

### <a name="_18_0_2_6340208_1485894157707_572874_4551"></a>*The **PositionStatus** Enumeration*

![Image of PositionStatus](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1485894157711_931606_4552.png)

Used in [SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635)::[Status](#_18_0_2_6340208_1485892992408_985925_4639) to identify the status of a selection indication.

Name | Value
---- | -----
`adjudicated`|Used if the indication was adjudicated.
`generated-rules`|Used if the indication was generated by the creating device per contest rules.
`invalidated-rules`|Used if the indication was invalidated by the creating device because of contest rules.
`other`|Used in conjunction with SelectionPosition::OtherStatus when no other value in this enumeration applies.

### <a name="_17_0_2_4_f71035d_1431607637366_785815_2242"></a>*The **ReportingUnitType** Enumeration*

![Image of ReportingUnitType](CastVoteRecords_UML_Documentation_files/_17_0_2_4_f71035d_1431607637380_196295_2243.png)

Used in [GpUnit](#_17_0_2_4_78e0236_1389366233346_42391_2380)::[Type](#_17_0_2_4_78e0236_1389713376966_77071_2393) to indicate a type of political geography.

Name | Value
---- | -----
`combined-precinct`|To indicate a combined precinct.
`polling-place`|To indicate a polling place.
`precinct`|To indicate a precinct.
`split-precinct`|To indicate a split-precinct.
`vote-center`|To indicate a vote-center.
`other`|Used in conjunction with GpUnit::OtherType when no other value in this enumeration applies.

### <a name="_18_0_5_43401a7_1483727563257_179426_4343"></a>*The **ReportType** Enumeration*

![Image of ReportType](CastVoteRecords_UML_Documentation_files/_18_0_5_43401a7_1483727563261_758233_4344.png)

Used in [CastVoteRecordReport](#_17_0_2_4_78e0236_1389366195564_913164_2300)::[ReportType](#_18_0_5_43401a7_1483727759336_770912_4370) to indicate the type of the CVR report.

Name | Value
---- | -----
`adjudicated`|To indicate that the report contains adjudications.
`aggregated`|To indicate that the report is an aggregation of device reports.
`originating-device-export`|To indicate that the report is an export from a device such as a scanner.
`rcv-round`|To indicate that the report is the result of a ranked choice voting round.
`other`|Used in conjunction with CastVoteRecordReport::OtherReportType when no other value in this enumeration applies.

### <a name="_18_0_5_43401a7_1483727021192_184103_4291"></a>*The **VoteVariation** Enumeration*

![Image of VoteVariation](CastVoteRecords_UML_Documentation_files/_18_0_5_43401a7_1483727021198_32472_4292.png)

Used in [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400)::[VoteVariation](#_18_0_5_43401a7_1483727343854_246701_4334) to indicate the vote variation (vote method) used to tabulate the contest.

Name | Value
---- | -----
`approval`|To indicate approval voting.
`borda`|To indicate the borda count method.
`cumulative`|To indicate cumulative voting.
`majority`|To indicate majority voting.
`n-of-m`|To indicate the N of M voting method.
`plurality`|To indicate plurality voting.
`proportional`|To indicate proportional voting.
`range`|To indicate range voting.
`rcv`|To indicate Ranked Choice Voting (RCV).
`super-majority`|To indicate the super majority voting method.
`other`|Used in conjunction with Contest::OtherVoteVariation when no other value in this enumeration applies.

## Classes

### <a name="_18_0_5_43401a7_1475856712376_208252_4416"></a>*The **Annotation** Class*

![Image of Annotation](CastVoteRecords_UML_Documentation_files/_18_0_5_43401a7_1475856712378_788981_4417.png)

[Annotation](#_18_0_5_43401a7_1475856712376_208252_4416) is used to record annotations made by one or more adjudicators.
[CVRSnapshot](#_17_0_2_4_78e0236_1389366224561_797289_2360) includes Annotation.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_5_43401a7_1475856818925_753666_4441"></a>`AdjudicatorName`|0..*|`String`|The name(s) of the adjudicator(s).
<a name="_18_0_5_43401a7_1475856861979_461651_4445"></a>`Message`|0..*|`String`|A message created by the adjudicator(s).
<a name="_18_0_5_43401a7_1475856758084_638015_4437"></a>`TimeStamp`|0..1|`dateTime`|The date and time of the annotation.


### <a name="_17_0_2_4_78e0236_1389366932057_929676_2783"></a>*The **BallotMeasureContest** Class*

![Image of BallotMeasureContest](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1389798977982_80297_5351.png)

[BallotMeasureContest](#_17_0_2_4_78e0236_1389366932057_929676_2783) is a subclass of [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) and is used to identify the type of contest as involving one or more ballot measures. It inherits attributes from [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400).


### <a name="_17_0_2_4_78e0236_1389372163799_981952_2926"></a>*The **BallotMeasureSelection** Class*

![Image of BallotMeasureSelection](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1389798977982_930954_5339.png)

[BallotMeasureSelection](#_17_0_2_4_78e0236_1389372163799_981952_2926) is a subclass of [ContestSelection](#_17_0_2_4_78e0236_1389372124445_11077_2906) and is used for ballot measures. The voter's selected response to the contest selection (e.g., "yes" or "no") may be in English or other languages as utilized on the voter's ballot.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_17_0_2_4_78e0236_1389710917151_765889_2176"></a>`Selection`|1|`String`|The voter's selection, i.e., 'yes' or 'no', in English or in other languages as utilized on the voter's ballot.


### <a name="_17_0_2_4_78e0236_1389366272694_544359_2440"></a>*The **Candidate** Class*

![Image of Candidate](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1389798977982_557229_5346.png)

[Candidate](#_17_0_2_4_78e0236_1389366272694_544359_2440) identifies a candidate in a contest on the voter's ballot. [Election](#_17_0_2_4_f71035d_1426101822599_430942_2209) includes instances of [Candidate](#_17_0_2_4_78e0236_1389366272694_544359_2440) for each candidate in a contest; typically, only those candidates who received votes would be included.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_17_0_2_4_f71035d_1430405890311_465205_2454"></a>`Code`|0..*|`Code`|A code or identifier associated with the candidate.
<a name="_17_0_2_4_78e0236_1389710816659_20227_2170"></a>`Name`|0..1|`String`|Candidate's name as listed on the ballot.
<a name="_17_0_2_4_78e0236_1389366597377_433664_2698"></a>`{Party}`|0..1|`Party`|The party associated with the candidate.


### <a name="_17_0_2_4_78e0236_1389366970084_183781_2806"></a>*The **CandidateContest** Class*

![Image of CandidateContest](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1389798977982_347543_5358.png)

[CandidateContest](#_17_0_2_4_78e0236_1389366970084_183781_2806) is a subclass of [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) and is used to identify the type of contest as involving one or more candidates. It inherits attributes from [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400).

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_2_6340208_1472160807984_726708_4721"></a>`NumberElected`|0..1|`Integer`|The number of candidates to be elected in the contest.
<a name="_17_0_2_4_78e0236_1389735000217_728769_4016"></a>`{PrimaryParty}`|0..1|`Party`|The party associated with the contest, if a partisan primary.
<a name="_18_0_2_6340208_1472160823529_29923_4725"></a>`VotesAllowed`|0..1|`Integer`|The number of votes allowed in the contest, e.g., 3 for a 'choose 3 of 5 candidates' contest.


### <a name="_17_0_2_4_d420315_1392145640524_831493_2562"></a>*The **CandidateSelection** Class*

![Image of CandidateSelection](CastVoteRecords_UML_Documentation_files/_17_0_2_4_d420315_1392145640527_433768_2563.png)

[CandidateSelection](#_17_0_2_4_d420315_1392145640524_831493_2562) is a subclass of [ContestSelection](#_17_0_2_4_78e0236_1389372124445_11077_2906) and is used for candidates, including for write-in candidates.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_17_0_2_4_d420315_1392145686219_781480_2594"></a>`{Candidate}`|0..*|`Candidate`|The candidate associated with the contest selection. For contests involving a ticket of multiple candidates, an ordered list of candidates as they appeared on the ballot would be created.
<a name="_18_0_2_6340208_1477060857505_890997_4554"></a>`IsWriteIn`|0..1|`Boolean`|A flag to indicate if the candidate selection is associated with a write-in.


### <a name="_17_0_2_4_78e0236_1389366195564_913164_2300"></a>*The **CastVoteRecordReport** Class*

![Image of CastVoteRecordReport](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1389798977982_73815_5340.png)

The root class/element; attributes pertain to the status and format of the report and when created.

[CastVoteRecordReport](#_17_0_2_4_78e0236_1389366195564_913164_2300) includes multiple instances of [CVR](#_18_0_2_6340208_1532543460307_914551_4600), one per [CVR](#_18_0_2_6340208_1532543460307_914551_4600) or sheet of a multi-page cast vote record. [CastVoteRecordReport](#_17_0_2_4_78e0236_1389366195564_913164_2300) also includes multiple instances of [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400), typically only for those contests that were voted so as to reduce file size. The [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) instances are later referenced by other classes to link them to contest options that were voted and the indication(s)/mark(s) made.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_5_43401a7_1469813329803_508626_4301"></a>`{CVR}`|0..*|`CVR`|Used to include instances of [CVR](#_18_0_2_6340208_1532543460307_914551_4600) classes, one per cast vote record in the report.
<a name="_18_0_2_6340208_1488998728442_776822_4559"></a>`{Election}`|1..*|`Election`|Used to include the election(s) associated with the CVRs.
<a name="_17_0_2_4_78e0236_1389733247429_431211_3338"></a>`GeneratedDate`|1|`dateTime`|Identifies the time that the election report was created.
<a name="_18_0_2_6340208_1488999116122_796953_4633"></a>`{GpUnit}`|1..*|`GpUnit`|Used to include the political geography, i.e., location, for where the cast vote record report was created and for linking cast vote records to their corresponding precinct or split (or otherwise smallest unit).
<a name="_17_0_2_4_f71035d_1400594737789_912202_2453"></a>`Notes`|0..1|`String`|Notes that can be added as appropriate, presumably by an adjudicator.
<a name="_18_0_2_6340208_1532543674900_374654_4626"></a>`{Party}`|0..*|`Party`|The party associated with the ballot sheet for a partisan primary.
<a name="_18_0_5_43401a7_1484155960667_232191_4295"></a>`{ReportGeneratingDevice}`|1..*|`ReportingDevice`|Identifies the device used to create the CVR report.
<a name="_18_0_2_6340208_1538322120049_840860_4675"></a>`{ReportingDevice}`|1..*|`ReportingDevice`|The device creating the report. The reporting device need not necessarily be the creating device, i.e., for an aggregated report, the reporting device could be an EMS used to aggregate and tabulate cast vote records.
<a name="_18_0_5_43401a7_1483727759336_770912_4370"></a>`ReportType`|0..*|`ReportType`|The type of report, using the [ReportType](#_18_0_5_43401a7_1483727563257_179426_4343) enumeration.
<a name="_18_0_5_43401a7_1483727799922_278659_4374"></a>`OtherReportType`|0..1|`String`|If [ReportType](#_18_0_5_43401a7_1483727759336_770912_4370) is 'other', this contains the report type.
<a name="_18_0_2_6340208_1488984515169_690457_4657"></a>`Version`|1|`CastVoteRecordVersion`|The version of the CVR specification being used (1.0).


### <a name="_17_0_2_4_f71035d_1430405712653_451634_2410"></a>*The **Code** Class*

![Image of Code](CastVoteRecords_UML_Documentation_files/_17_0_2_4_f71035d_1430405712661_66241_2411.png)

[Code](#_17_0_2_4_f71035d_1430405712653_451634_2410) is used in [Election](#_17_0_2_4_f71035d_1426101822599_430942_2209), [GpUnit](#_17_0_2_4_78e0236_1389366233346_42391_2380), [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400), [Candidate](#_17_0_2_4_78e0236_1389366272694_544359_2440), and [Party](#_17_0_2_4_78e0236_1389366278128_412819_2460) to identify an associated code as well as the type of code.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_17_0_2_4_f71035d_1441215385623_864674_2521"></a>`Label`|0..1|`String`|A label associated with the code, used as needed.
<a name="_17_0_2_4_f71035d_1430405763078_743585_2433"></a>`Type`|1|`IdentifierType`|Used to indicate the type of code, from the [IdentifierType](#_17_0_2_4_f71035d_1425061188508_163854_2613) enumeration.
<a name="_17_0_2_4_f71035d_1430405732252_109247_2429"></a>`OtherType`|0..1|`String`|If [Type](#_17_0_2_4_f71035d_1430405763078_743585_2433) is 'other', the type of code.
<a name="_17_0_2_4_f71035d_1430405785820_123111_2437"></a>`Value`|1|`String`|The value of the code, i.e., the identifier.


### <a name="_17_0_2_4_78e0236_1389366251994_876831_2400"></a>*The **Contest** Class*

![Image of Contest](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1389798977982_293750_5341.png)

[Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) represents a contest on the ballot. [CastVoteRecordReport](#_17_0_2_4_78e0236_1389366195564_913164_2300) initially includes an instance of [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) for each contest on the ballot.  Other classes can subsequently reference the instances as necessary to link together items on the cast vote record, such as a contest, its voted contest selection(s), and the mark(s) associated with the selection(s).

[Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) has three subclasses, each used for a specific type of contest:   These subclasses inherit Contest's attributes.

 *  [PartyContest](#_17_0_2_4_d420315_1393514218965_55008_3144) \- used for straight party contests,
 *  [BallotMeasureContest](#_17_0_2_4_78e0236_1389366932057_929676_2783) \- used for contests, and
 *  [CandidateContest](#_17_0_2_4_78e0236_1389366970084_183781_2806) \- used for candidate contests.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_17_0_5_1_43401a7_1395831571231_804795_3632"></a>`Abbreviation`|0..1|`String`|An abbreviation associated with the contest.
<a name="_17_0_2_4_f71035d_1430412090176_814999_2249"></a>`Code`|0..*|`Code`|A code or identifier used for this contest.
<a name="_17_0_2_4_78e0236_1389366541302_23458_2637"></a>`{ContestSelection}`|1..*|`ContestSelection`|Identifies the contest selections in the contest.
<a name="_17_0_2_4_78e0236_1389712460582_306281_2220"></a>`Name`|0..1|`String`|Title or name of the contest, e.g., "Governor" or "Question on Legalization of Gambling".
<a name="_18_0_5_43401a7_1483727343854_246701_4334"></a>`VoteVariation`|0..1|`VoteVariation`|The vote variation for this contest, from the [VoteVariation](#_18_0_5_43401a7_1483727021192_184103_4291) enumeration.
<a name="_18_0_5_43401a7_1483727376096_587155_4338"></a>`OtherVoteVariation`|0..1|`String`|If [VoteVariation](#_18_0_5_43401a7_1483727343854_246701_4334) is 'other', the vote variation for this contest.


### <a name="_17_0_2_4_78e0236_1389372124445_11077_2906"></a>*The **ContestSelection** Class*

![Image of ContestSelection](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1389798977982_125024_5356.png)

[ContestSelection](#_17_0_2_4_78e0236_1389372124445_11077_2906) represents a contest selection in a contest.  [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) can include an instance of [ContestSelection](#_17_0_2_4_78e0236_1389372124445_11077_2906) for each contest selection in the contest or, as desired, all contest selections.  

ContestSelection has three subclasses, each used for a specific type of contest selection:

 *  [BallotMeasureSelection](#_17_0_2_4_78e0236_1389372163799_981952_2926) \- used for ballot measures,
 *  [CandidateSelection](#_17_0_2_4_d420315_1392145640524_831493_2562) \- used for candidate selections, and
 *  [PartySelection](#_17_0_2_4_f71035d_1426519980658_594892_2511) \- used for straight party selections.

Instances of [CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292) subsequently link to the contest selections as needed so as to tie together the contest, the contest selection, and the mark(s) made for the contest selection.

[ContestSelection](#_17_0_2_4_78e0236_1389372124445_11077_2906) contains one attribute, [Code](#_18_5_3_43701b0_1534269642876_463463_5873), that can be used to identify the contest selection and thereby eliminate the need to identify it using the subclasses.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_5_3_43701b0_1534269642876_463463_5873"></a>`Code`|0..*|`Code`|Code used to identify the contest selection.


### <a name="_18_0_2_6340208_1532543460307_914551_4600"></a>*The **CVR** Class*

![Image of CVR](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1532543460312_263838_4601.png)

[CVR](#_18_0_2_6340208_1532543460307_914551_4600) constitutes a cast vote record, generated by a ballot scanning device, containing indications of contests and contest options chosen by the voter, as well as other information for auditing and annotation purposes. Each sheet of a multi-page paper ballot is represented by an individual [CVR](#_18_0_2_6340208_1532543460307_914551_4600), e.g., if all sheets of a 5-sheet ballot are scanned, 5 CVRs will be created. [CastVoteRecordReport](#_17_0_2_4_78e0236_1389366195564_913164_2300) includes multiple instances of [CVR](#_18_0_2_6340208_1532543460307_914551_4600) as applicable.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_2_6340208_1469207550920_513772_4736"></a>`BallotAuditId`|0..1|`String`|A unique identifier for this CVR, used to link the CVR with the corresponding audit record, e.g., a paper ballot. This identifier may be impressed on the corresponding audit record as it is scanned, or otherwise associated with the corresponding ballot.
<a name="_18_0_2_6340208_1477335811070_110072_4695"></a>`BallotImage`|0..*|`ImageData`|An image of the ballot sheet created by the scanning device.
<a name="_18_0_2_6340208_1485889604690_46103_4553"></a>`BallotPrePrintedId`|0..1|`String`|A unique identifier for the ballot (or sheet of a multi-sheet ballot) that this CVR represents, used if ballots are pre-marked with unique identifiers. If provided, this number would be the same on all CVRs that represent individual sheets from the same multi-sheet ballot. This identifier is not the same as one that may be impressed on the corresponding ballot as it is scanned or otherwise associated with the corresponding ballot; see the [BallotAuditId](#_18_0_2_6340208_1469207550920_513772_4736) attribute.
<a name="_18_0_2_6340208_1485889507713_842254_4548"></a>`BallotSheetId`|0..1|`String`|A unique number for the ballot (or sheet of a multi-sheet ballot) that this CVR represents, used if ballots are pre-marked with unique numbers. If provided, this number would be the same on all CVRs that represent individual sheets from the same multi-sheet ballot. This number is not the same as one that may be impressed on the corresponding ballot as it is scanned or otherwise associated with the corresponding ballot; see the [BallotAuditId](#_18_0_2_6340208_1469207550920_513772_4736) attribute.
<a name="_18_0_2_6340208_1477336326894_57154_4725"></a>`BallotStyleId`|0..1|`String`|An identifier of the ballot style associated with the corresponding ballot.
<a name="_18_0_2_6340208_1491322891923_301659_4571"></a>`{BallotStyleUnit}`|0..1|`GpUnit`|Identifies the smallest unit of geography associated with the corresponding ballot, typically a precinct or split-precinct.
<a name="_18_0_2_6340208_1485284914250_330502_4620"></a>`BatchId`|0..1|`String`|The identifier for the batch that includes this CVR.
<a name="_18_0_2_6340208_1491322213394_604125_4555"></a>`BatchSequenceId`|0..1|`Integer`|The sequence number of the corresponding paper ballot within a batch.
<a name="_18_5_3_43701b0_1533931125455_124502_5709"></a>`{CreatingDevice}`|0..1|`ReportingDevice`|Identifies the device that created the CVR.
<a name="_19_0_43701b0_1541096043878_35148_5034"></a>`{CurrentSnapshot}`|1|`CVRSnapshot`|Identifies the snapshot that is currently tabulatable.
<a name="_18_0_2_6340208_1532543700707_228349_4655"></a>`{CVRSnapshot}`|1..*|`CVRSnapshot`|Identifies the repeatable portion of the CVR that links to contest selections and related information.
<a name="_18_0_2_6340208_1489002073957_902699_4732"></a>`{Election}`|1|`Election`|Used to identify an election with which the CVR is associated.
<a name="_17_0_2_4_f71035d_1426788475880_621446_2579"></a>`{Party}`|0..*|`Party`|Identifies the party associated with a CVR, typically for partisan primaries.
<a name="_18_0_2_6340208_1485285067563_572486_4624"></a>`UniqueId`|0..1|`String`|The sequence number for this CVR. This represents the ordinal number that this CVR was processed by the tabulating device.


### <a name="_18_0_2_6340208_1469203058990_306165_4565"></a>*The **CVRContest** Class*

![Image of CVRContest](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1469203058998_13088_4566.png)

[CVRContest](#_18_0_2_6340208_1469203058990_306165_4565) class is included by [CVRSnapshot](#_17_0_2_4_78e0236_1389366224561_797289_2360) for each contest on the ballot that was voted, that is, whose contest options contain indications that may constitute a vote. [CVRContest](#_18_0_2_6340208_1469203058990_306165_4565) includes [CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292) for each contest option in the contest containing an indication or write-in.

[CVRSnapshot](#_17_0_2_4_78e0236_1389366224561_797289_2360) can also include [CVRContest](#_18_0_2_6340208_1469203058990_306165_4565) for every contest on the ballot regardless of whether any of the contest options contain an indication, for cases where the CVR must include all contests that appeared on the ballot.

[CVRContest](#_18_0_2_6340208_1469203058990_306165_4565) attributes are for including summary information about the contest.

Overvotes plus Undervotes plus TotalVotes must equal the number of votes allowable in the contest, e.g., in a "chose 3 of 5" contest in which the voter chooses only 2, then Overvotes = 0, Undervotes = 1, and TotalVotes = 2, which adds up to the number of votes allowable = 3.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_2_6340208_1469203119527_802583_4612"></a>`{Contest}`|1|`Contest`|Used to link to an instance of [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) specific to the contest at hand, for the purpose of specifying information about the contest such as its contest identifier.
<a name="_18_0_5_43401a7_1474453069356_745132_4326"></a>`{CVRContestSelection}`|0..*|`CVRContestSelection`|Used to include information about a contest selection in the contest, including the associated indication(s).
<a name="_18_0_2_6340208_1491331465665_822585_4606"></a>`Overvotes`|0..1|`Integer`|The number of votes lost due to overvoting.
<a name="_18_0_2_6340208_1491409925893_814149_4553"></a>`Selections`|0..1|`Integer`|Used to indicate the number of possible contest selections in the contest.
<a name="_18_0_5_43401a7_1475850227700_908488_4330"></a>`Status`|0..*|`ContestStatus`|The status of the contest, e.g., overvoted, undervoted, from the [ContestStatus](#_18_0_5_43401a7_1475850124791_123384_4291) enumeration. If no values apply, use 'other' and include a user-defined status in [OtherStatus](#_18_0_5_43401a7_1475856016959_840864_4388).
<a name="_18_0_5_43401a7_1475856016959_840864_4388"></a>`OtherStatus`|0..1|`String`|Used when [Status](#_18_0_5_43401a7_1475850227700_908488_4330) is 'other' to include a user-defined status.
<a name="_18_0_2_6340208_1491331452091_318387_4602"></a>`Undervotes`|0..1|`Integer`|The number of votes lost due to undervoting.
<a name="_18_5_3_43701b0_1534266820963_828170_5833"></a>`WriteIns`|0..1|`Integer`|The total number of write-ins in the contest.


### <a name="_18_0_5_43401a7_1474452890357_299022_4292"></a>*The **CVRContestSelection** Class*

![Image of CVRContestSelection](CastVoteRecords_UML_Documentation_files/_18_0_5_43401a7_1474452890365_842519_4293.png)

[CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292) is used to link a contest option containing an indication with information about the indication, such as whether a mark constitutes a countable vote, or whether a mark is determined to be marginal, etc. [CVRContest](#_18_0_2_6340208_1469203058990_306165_4565) includes an instance of [CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292) when an indication for the selection is present, and [CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292) then includes [SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635) for each indication present. To tie the indication to the specific contest selection, [CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292) links to an instance of [ContestSelection](#_17_0_2_4_78e0236_1389372124445_11077_2906) that has previously been included by [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400).

Since multiple indications per contest option are possible for some voting methods, [CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292) can include multiple instances of [SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635), one per indication. [CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292) can also be used for the purpose of including, in the CVR, all contest options in the contest regardless of whether indications are present. In this case, CVRContestSelection would not include [SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635) if no indication is present but would link to the appropriate instance of [ContestSelection](#_17_0_2_4_78e0236_1389372124445_11077_2906).


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_2_6340208_1469203113749_298974_4591"></a>`{ContestSelection}`|0..1|`ContestSelection`|Used to link to an instance of a contest selection that was previously included by [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400).
<a name="_18_0_5_43401a7_1484322103253_625422_4289"></a>`OptionPosition`|0..1|`Integer`|Used to include the ordinal position of the contest option as it appeared on the ballot.
<a name="_18_0_5_43401a7_1525884900274_453930_4291"></a>`Rank`|0..1|`Integer`|For the RCV voting variation, the rank chosen by the voter, for when a contest selection can represent a ranking.
<a name="_18_0_2_6340208_1485892992410_316802_4653"></a>`{SelectionPosition}`|1..*|`SelectionPosition`|Used to include further information about the indication/mark associated with the contest selection. Depending on the voting method, multiple indications/marks per selection may be possible.
<a name="_18_0_5_43401a7_1475850275266_189599_4334"></a>`Status`|0..*|`ContestSelectionStatus`|Contains the status of the contest selection, e.g., 'needs-adjudication' for a contest requiring adjudication, using values from the [ContestSelectionStatus](#_18_0_5_43401a7_1475850153090_186243_4311) enumeration. If no values apply, use 'other' and include a user-defined status in [OtherStatus](#_18_0_5_43401a7_1475855963037_920235_4384).
<a name="_18_0_5_43401a7_1475855963037_920235_4384"></a>`OtherStatus`|0..1|`String`|Used when [Status](#_18_0_5_43401a7_1475850275266_189599_4334) is 'other' to include a user-defined status.
<a name="_19_0_43701b0_1556050052423_495068_5158"></a>`TotalFractionalVotes`|0..1|`FractionalNumber`|For cumulative or range and other similar voting variations, contains the total proper fractional number of votes across all indications/marks.
<a name="_18_0_2_6340208_1488988324514_948852_4757"></a>`TotalNumberVotes`|0..1|`Integer`|For cumulative or range and other similar voting variations, contains the total number of votes across all indications/marks.


### <a name="_17_0_2_4_78e0236_1389366224561_797289_2360"></a>*The **CVRSnapshot** Class*

![Image of CVRSnapshot](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1389799207465_976765_6435.png)

[CVRSnapshot](#_17_0_2_4_78e0236_1389366224561_797289_2360) contains a version of the contest selections for a CVR; there can be multiple versions of [CVRSnapshot](#_17_0_2_4_78e0236_1389366224561_797289_2360) within the same CVR. Type specifies the type of the snapshot, i.e., whether interpreted by the scanner according to contest rules, modified as a result of adjudication, or the original, that is, the version initially scanned before contest rules are applied. [CVR](#_18_0_2_6340208_1532543460307_914551_4600) includes [CVRSnapshot](#_17_0_2_4_78e0236_1389366224561_797289_2360).

Other attributes are repeated in each [CVRSnapshot](#_17_0_2_4_78e0236_1389366224561_797289_2360) because they may differ across snapshots, e.g., the contests could be different as well as other status.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_5_43401a7_1475856929390_368624_4454"></a>`{Annotation}`|0..*|`Annotation`|Used to include an annotation associated with the CVR snapshot.
<a name="_18_0_2_6340208_1469203129639_870971_4633"></a>`{CVRContest}`|0..*|`CVRContest`|Identifies the contests in the CVR.
<a name="_18_0_2_6340208_1472158928951_402259_4603"></a>`Status`|0..*|`CVRStatus`|The status of the CVR.
<a name="_18_0_5_43401a7_1475856170152_824205_4392"></a>`OtherStatus`|0..1|`String`|When [Status](#_18_0_2_6340208_1472158928951_402259_4603) is 'other', contains the ballot status.
<a name="_18_0_2_6340208_1532543968111_779654_4689"></a>`Type`|1|`CVRType`|The type of the snapshot, e.g., original.


### <a name="_18_0_2_6340208_1485892911278_166697_4594"></a>*The **CVRWriteIn** Class*

![Image of CVRWriteIn](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1485892911283_45277_4605.png)

[CVRWriteIn](#_18_0_2_6340208_1485892911278_166697_4594) is used when the contest selection is a write-in. It has attributes for the image or text of the write-in.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_2_6340208_1485892911278_481541_4596"></a>`Text`|0..1|`String`|Used for the text of the write-in, typically present when the CVR has been created by electronic ballot marking equipment.
<a name="_18_0_2_6340208_1485892911278_517000_4595"></a>`WriteInImage`|0..1|`ImageData`|Used for an image of the write-in, typically made by a scanner when scanning a paper ballot.


### <a name="_17_0_2_4_f71035d_1426101822599_430942_2209"></a>*The **Election** Class*

![Image of Election](CastVoteRecords_UML_Documentation_files/_17_0_2_4_f71035d_1426101822601_995748_2210.png)

[Election](#_17_0_2_4_f71035d_1426101822599_430942_2209) defines instances of the [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) and [Candidate](#_17_0_2_4_78e0236_1389366272694_544359_2440) classes so that they can be later referenced in CVR classes. [Election](#_17_0_2_4_f71035d_1426101822599_430942_2209) includes an instance of [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) for each contest in the election and includes an instance of [Candidate](#_17_0_2_4_78e0236_1389366272694_544359_2440) for each candidate. This is done to utilize file sizes more efficiently; otherwise each CVR would need to define these instances separately and much duplication would occur.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_17_0_2_4_f71035d_1426788786008_599642_2643"></a>`{Candidate}`|0..*|`Candidate`|Used to establish a collection of candidate definitions that will be referenced by the CVRs. The contests in each CVR will reference the candidate definitions.
<a name="_17_0_2_4_f71035d_1430411992333_911417_2240"></a>`Code`|0..*|`Code`|Used for a code associated with the election, e.g., a precinct identifier if the election scope is a precinct.
<a name="_17_0_2_4_f71035d_1426788714136_545781_2616"></a>`{Contest}`|1..*|`Contest`|Used for establishing a collection of contest definitions that will be referenced by the CVRs.
<a name="_18_2_43401a7_1450723692857_875635_4654"></a>`{ElectionScope}`|1|`GpUnit`|Used to identify the election scope, i.e., the political geography corresponding to the election.
<a name="_17_0_2_4_f71035d_1426101865703_367602_2232"></a>`Name`|0..1|`String`|A text string identifying the election.


### <a name="_18_0_2_6340208_1485284639717_497586_4548"></a>*The **File** Class*

![Image of File](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1485284639742_53322_4561.png)

Used to hold the contents of a file or identify a file created by the scanning device. The file generally would contain an image of the scanned ballot or an image of a write-in entered by a voter onto the scanned ballot. SubClass [Image](#_18_0_2_6340208_1485284639720_737438_4549) is used if the file contains an image.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_2_6340208_1485284639723_485833_4550"></a>`Data`|1|`base64Binary`|Contains the base64 binary contents of the file.
<a name="_18_0_2_6340208_1485284639724_125436_4551"></a>`FileName`|0..1|`String`|Contains the name of the file or an identifier of the file.
<a name="_18_0_2_6340208_1485284639724_875893_4552"></a>`MimeType`|0..1|`String`|The mime type of the file, e.g., image/jpeg.


### <a name="_19_0_43701b0_1556049559972_974781_5102"></a>*The **FractionalNumber** Class*

![Image of FractionalNumber](CastVoteRecords_UML_Documentation_files/_19_0_43701b0_1556049559993_299889_5103.png)

A proper fractional value, represented using fractional or decimal notation.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_19_0_43701b0_1556049825598_445953_5155"></a>`pattern`||`String`|Pattern describing the allowed values for a [FractionalNumber](#_19_0_43701b0_1556049559972_974781_5102).


### <a name="_17_0_2_4_78e0236_1389366233346_42391_2380"></a>*The **GpUnit** Class*

![Image of GpUnit](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1390579885871_183088_2445.png)

Used for identifying a geographical unit for various purposes, including:

 *  The reporting unit of the report generation device, e.g., a precinct location of a scanner that generates the collection of CVRs,
 *  The geographical scope of the election, or the unit of geography associated with an individual CVR.

[CastVoteRecordReport](#_17_0_2_4_78e0236_1389366195564_913164_2300) includes instances of [GpUnit](#_17_0_2_4_78e0236_1389366233346_42391_2380) as needed. [Election](#_17_0_2_4_f71035d_1426101822599_430942_2209) references [GpUnit](#_17_0_2_4_78e0236_1389366233346_42391_2380) as [ElectionScope](#_18_2_43401a7_1450723692857_875635_4654), for the geographical scope of the election.  [CVR](#_18_0_2_6340208_1532543460307_914551_4600) CastVoteRecordReport includes instances of GpUnit as needed. Election references GpUnit as ElectionScope, for the geographical scope of the election.  CVR references GpUnit as BallotStyleUnit to link a CVR to the smallest political subdivision that uses the same ballot style as was used for the voter’s ballot.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_17_0_2_4_f71035d_1430412120441_638024_2251"></a>`Code`|0..*|`Code`|A code associated with the geographical unit.
<a name="_17_0_2_4_d420315_1393450176252_314086_2868"></a>`Name`|0..1|`String`|Name of the geographical unit.
<a name="_18_0_2_6340208_1489681733700_296781_4553"></a>`{ReportingDevice}`|0..*|`ReportingDevice`|The collection of cast vote records associated with the reporting unit and the reporting device.
<a name="_17_0_2_4_78e0236_1389713376966_77071_2393"></a>`Type`|1|`ReportingUnitType`|Contains the type of geographical unit, e.g., precinct, split-precinct, vote center, using values from the [ReportingUnitType](#_17_0_2_4_f71035d_1431607637366_785815_2242) enumeration. If no values apply, use 'other' and include a user-defined type in [OtherType](#_17_0_2_4_f71035d_1426007519161_685921_2510).
<a name="_17_0_2_4_f71035d_1426007519161_685921_2510"></a>`OtherType`|0..1|`String`|Used when [Type](#_17_0_2_4_78e0236_1389713376966_77071_2393) is 'other' to include a user-defined type.


### <a name="_18_0_2_6340208_1485894593826_736413_4615"></a>*The **Hash** Class*

![Image of Hash](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1485894619632_889587_4622.png)

[Hash](#_18_0_2_6340208_1485894593826_736413_4615) is used to specify a hash associated with a file such as an image file of a scanned ballot.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_2_6340208_1485894641846_811323_4646"></a>`Type`|1|`HashType`|The type of the hash, from the [HashType](#_18_0_2_6340208_1485894679180_11599_4655) enumeration.
<a name="_18_0_2_6340208_1485894652084_23532_4650"></a>`OtherType`|0..1|`String`|If [Type](#_18_0_2_6340208_1485894641846_811323_4646) is 'other', the type of the hash.
<a name="_18_0_2_6340208_1485894623486_698989_4642"></a>`Value`|1|`String`|The hash value, encoded as a string.


### <a name="_18_0_2_6340208_1485284639720_737438_4549"></a>*The **Image** Class*

![Image of Image](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1485284639744_493211_4562.png)

Used by [File](#_18_0_2_6340208_1485284639717_497586_4548) for a file containing an image, e.g., an image of a write-in on a paper ballot.


### <a name="_18_0_2_6340208_1485894533655_402033_4588"></a>*The **ImageData** Class*

![Image of ImageData](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1485894533656_423599_4589.png)

[ImageData](#_18_0_2_6340208_1485894533655_402033_4588) is used to specify an image file such as for a write-in or the entire ballot.  It works with several other classes, as follows:

 *  [File](#_18_0_2_6340208_1485284639717_497586_4548) with SubClass [Image](#_18_0_2_6340208_1485284639720_737438_4549) – to contain either a filename for an external file or the file contents, and
 *  [Hash](#_18_0_2_6340208_1485894593826_736413_4615) – to contain cryptographic hash function data for the file.


Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_2_6340208_1485894809122_512616_4712"></a>`{Hash}`|0..1|`Hash`|A hash value for the image data, used for verification comparisons against subsequent copies of the image.
<a name="_18_0_2_6340208_1485894784931_504817_4685"></a>`{Image}`|0..1|`Image`|The image of an individual ballot sheet created by the scanner, could possibly include both sides of a two-sided ballot sheet depending on the scanner's configuration.
<a name="_18_0_2_6340208_1485894593835_110320_4618"></a>`Location`|0..1|`anyURI`|A pointer to the location of the image file.


### <a name="_17_0_2_4_78e0236_1389366278128_412819_2460"></a>*The **Party** Class*

![Image of Party](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1389798977982_989674_5350.png)

[Party](#_17_0_2_4_78e0236_1389366278128_412819_2460) is used for describing information about a political party associated with the voter's ballot. [CVR](#_18_0_2_6340208_1532543460307_914551_4600) includes instances of [Party](#_17_0_2_4_78e0236_1389366278128_412819_2460) as needed, e.g., for a [CVR](#_18_0_2_6340208_1532543460307_914551_4600) corresponding to a ballot in a partisan primary, and [CandidateContest](#_17_0_2_4_78e0236_1389366970084_183781_2806) references Party as needed to link a candidate to their political party.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_17_0_2_4_78e0236_1389734813018_766516_3987"></a>`Abbreviation`|0..1|`String`|Short name for the party, e.g., "DEM".
<a name="_17_0_2_4_f71035d_1430412372015_749476_2263"></a>`Code`|0..*|`Code`|A code associated with the party.
<a name="_17_0_2_4_78e0236_1389710882517_230322_2174"></a>`Name`|0..1|`String`|Official full name of the party, e.g., "Republican".


### <a name="_17_0_2_4_d420315_1393514218965_55008_3144"></a>*The **PartyContest** Class*

![Image of PartyContest](CastVoteRecords_UML_Documentation_files/_17_0_2_4_d420315_1393514218978_361648_3145.png)

[PartyContest](#_17_0_2_4_d420315_1393514218965_55008_3144) is a subclass of [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400) and is used to identify the type of contest as involving a straight party selection. It inherits attributes from [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400).


### <a name="_17_0_2_4_f71035d_1426519980658_594892_2511"></a>*The **PartySelection** Class*

![Image of PartySelection](CastVoteRecords_UML_Documentation_files/_17_0_2_4_f71035d_1426519980661_572615_2512.png)

[PartySelection](#_17_0_2_4_f71035d_1426519980658_594892_2511) is a subclass of [ContestSelection](#_17_0_2_4_78e0236_1389372124445_11077_2906) and is used typically for a contest selection in a straight-party contest.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_17_0_2_4_f71035d_1426520590194_384550_2564"></a>`{Party}`|1..*|`Party`|The party associated with the contest selection.


### <a name="_17_0_2_4_78e0236_1389798013459_389380_4178"></a>*The **ReportingDevice** Class*

![Image of ReportingDevice](CastVoteRecords_UML_Documentation_files/_17_0_2_4_78e0236_1389798977982_371820_5343.png)

[ReportingDevice](#_17_0_2_4_78e0236_1389798013459_389380_4178) is used to specify a voting device as the “political geography” at hand. [CastVoteRecordReport](#_17_0_2_4_78e0236_1389366195564_913164_2300) refers to it as [ReportGeneratingDevice](#_18_0_5_43401a7_1484155960667_232191_4295) and uses it to specify the device that created the CVR report. [CVR](#_18_0_2_6340208_1532543460307_914551_4600) refers to it as [CreatingDevice](#_18_5_3_43701b0_1533931125455_124502_5709) to specify the device that created the CVRs.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_5_43401a7_1484156729348_915950_4329"></a>`Application`|0..1|`String`|The application associated with the reporting device.
<a name="_19_0_43701b0_1545400619649_205122_5079"></a>`Code`|0..*|`Code`|A code associated with the reporting device.
<a name="_17_0_2_4_f71035d_1401286171326_648907_2273"></a>`Manufacturer`|0..1|`String`|Manufacturer of the reporting device.
<a name="_18_0_2_6340208_1488984847640_305895_4706"></a>`MarkMetricType`|0..1|`String`|The type of metric being used to determine quality. The type must be specific enough that the attached value can be accurately verified later, e.g., 'Acme Mark Density' may be a sufficiently specific type.
<a name="_17_0_2_4_f71035d_1401286117587_806540_2269"></a>`Model`|0..1|`String`|Manufacturer's model of the reporting device.
<a name="_18_0_5_43401a7_1484156092074_357957_4321"></a>`Notes`|0..*|`String`|Additional explanatory notes as applicable.
<a name="_17_0_2_4_d420315_1393446014406_394266_2688"></a>`SerialNumber`|0..1|`String`|Serial number or other identification that can uniquely identify the reporting device.


### <a name="_18_0_2_6340208_1425646217522_163181_4554"></a>*The **RetentionContest** Class*

![Image of RetentionContest](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1425646217525_713812_4555.png)

[RetentionContest](#_18_0_2_6340208_1425646217522_163181_4554) is a subclass of [BallotMeasureContest](#_17_0_2_4_78e0236_1389366932057_929676_2783) and is used to identify the type of contest as involving a retention, such as for a judicial retention. While it is similar to [BallotMeasureContest](#_17_0_2_4_78e0236_1389366932057_929676_2783), it contains a link to [Candidate](#_17_0_2_4_78e0236_1389366272694_544359_2440) that [BallotMeasureContest](#_17_0_2_4_78e0236_1389366932057_929676_2783) does not. [RetentionContest](#_18_0_2_6340208_1425646217522_163181_4554) inherits attributes from [Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400).

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_18_0_2_6340208_1425646466278_708197_4616"></a>`{Candidate}`||`Candidate`|Identifies the candidate in the retention contest.


### <a name="_18_0_2_6340208_1485892992407_492157_4635"></a>*The **SelectionPosition** Class*

![Image of SelectionPosition](CastVoteRecords_UML_Documentation_files/_18_0_2_6340208_1485892992418_910967_4658.png)

[CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292) includes [SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635) to specify a voter's indication/mark in a contest option, and thus, a potential vote. The number of potential SelectionPositions that could be included by [CVRContestSelection](#_18_0_5_43401a7_1474452890357_299022_4292) is the same as the number of ovals next to a particular option. There will be usually 1 instance of [SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635) for plurality voting, but there could be multiple instances for RCV, approval, cumulative, or other vote variations in which a voter can select multiple options per candidate.

[MarkMetricValue](#_18_0_2_6340208_1488984862414_760136_4710) specifies the measurement of a mark on a paper ballot. The measurement is assigned by the scanner for measurements of mark density or quality and would be used by the scanner to indicate whether the mark is a valid voter mark representing a vote or is marginal.

[SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635) contains additional information about the mark to specify whether the indication/mark is allocable, as well as information needed for certain voting methods.

[SelectionPosition](#_18_0_2_6340208_1485892992407_492157_4635) includes [CVRWriteIn](#_18_0_2_6340208_1485892911278_166697_4594), whose attributes are used to include information about the write-in including the text of the write-in or an image of the write-in.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
<a name="_19_0_43701b0_1541096140220_743803_5066"></a>`Code`|0..*|`Code`|Code used to identify the contest selection position.
<a name="_19_0_43701b0_1541096285019_709577_5079"></a>`{CVRWriteIn}`|0..1|`CVRWriteIn`|Used to store information regarding a write-in vote.
<a name="_19_0_43701b0_1556130739145_967916_5093"></a>`FractionalVotes`|0..1|`FractionalNumber`|The proper fractional number of votes represented by the position.
<a name="_19_0_43701b0_1541095481007_618279_4996"></a>`HasIndication`|1|`IndicationStatus`|Whether there is a selection indication present.
<a name="_18_0_2_6340208_1532546142492_921207_4764"></a>`IsAllocable`|0..1|`AllocationStatus`|Whether this indication should be allocated to the contest option's accumulator.
<a name="_19_0_43701b0_1543438269888_294947_5070"></a>`IsGenerated`|0..1|`Boolean`|Whether or not the indication was generated, rather than directly made by the voter.
<a name="_18_0_2_6340208_1488984862414_760136_4710"></a>`MarkMetricValue`|0..*|`String`|The value of the mark metric, represented as a string.
<a name="_18_0_2_6340208_1485892992408_339917_4637"></a>`NumberVotes`|1|`Integer`|The number of votes represented by the position, usually 1 but may be more depending on the voting method.
<a name="_18_0_2_6340208_1485892992408_897036_4641"></a>`Position`|0..1|`Integer`|The ordinal position of the selection position within the contest option.
<a name="_18_0_2_6340208_1485892992407_101557_4636"></a>`Rank`|0..1|`Integer`|For the RCV voting variation, the rank chosen by the voter, for when a position can represent a ranking.
<a name="_18_0_2_6340208_1485892992408_985925_4639"></a>`Status`|0..*|`PositionStatus`|Status of the position, e.g., "generated-rules" for generated by the machine, from the [PositionStatus](#_18_0_2_6340208_1485894157707_572874_4551) enumeration. If no values apply, use 'other' and include a user-defined status in OtherStatus.
<a name="_18_0_2_6340208_1485892992408_385738_4640"></a>`OtherStatus`|0..1|`String`|Used when [Status](#_18_0_2_6340208_1485892992408_985925_4639) is 'other' to include a user-defined status.
