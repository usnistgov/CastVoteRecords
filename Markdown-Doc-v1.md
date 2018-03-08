# Table of Contents
- Table of Contents
  - Enumerations
    - *The **[BallotSelectionStatus](#_18_0_5_43401a7_1475850153090_186243_4311)** Enumeration*
    - *The **[BallotStatus](#_18_0_2_6340208_1472159006307_546162_4628)** Enumeration*
    - *The **[CastVoteRecordVersion](#_18_0_2_6340208_1488984734564_983877_4662)** Enumeration*
    - *The **[ContestStatus](#_18_0_5_43401a7_1475850124791_123384_4291)** Enumeration*
    - *The **[CVRComponentStatus](#_18_0_2_6340208_1493056057833_123746_4561)** Enumeration*
    - *The **[HashType](#_18_0_2_6340208_1485894679180_11599_4655)** Enumeration*
    - *The **[IdentifierType](#_17_0_2_4_f71035d_1425061188508_163854_2613)** Enumeration*
    - *The **[ReportingUnitType](#_17_0_2_4_f71035d_1431607637366_785815_2242)** Enumeration*
    - *The **[ReportType](#_18_0_5_43401a7_1483727563257_179426_4343)** Enumeration*
    - *The **[VoteMarkStatus](#_18_0_2_6340208_1485894157707_572874_4551)** Enumeration*
    - *The **[VoteVariation](#_18_0_5_43401a7_1483727021192_184103_4291)** Enumeration*
  - Classes
    - *The **[Annotation](#_18_0_5_43401a7_1475856712376_208252_4416)** Class*
    - *The **[BallotMeasureContest](#_17_0_2_4_78e0236_1389366932057_929676_2783)** Class*
    - *The **[BallotMeasureSelection](#_17_0_2_4_78e0236_1389372163799_981952_2926)** Class*
    - *The **[BallotSelection](#_17_0_2_4_78e0236_1389372124445_11077_2906)** Class*
    - *The **[BallotSelectionVote](#_18_0_5_43401a7_1474452890357_299022_4292)** Class*
    - *The **[Candidate](#_17_0_2_4_78e0236_1389366272694_544359_2440)** Class*
    - *The **[CandidateContest](#_17_0_2_4_78e0236_1389366970084_183781_2806)** Class*
    - *The **[CandidateSelection](#_17_0_2_4_d420315_1392145640524_831493_2562)** Class*
    - *The **[CastVoteRecord](#_17_0_2_4_78e0236_1389366224561_797289_2360)** Class*
    - *The **[CastVoteRecordReport](#_17_0_2_4_78e0236_1389366195564_913164_2300)** Class*
    - *The **[Code](#_17_0_2_4_f71035d_1430405712653_451634_2410)** Class*
    - *The **[Contest](#_17_0_2_4_78e0236_1389366251994_876831_2400)** Class*
    - *The **[ContestVote](#_18_0_2_6340208_1469203058990_306165_4565)** Class*
    - *The **[Election](#_17_0_2_4_f71035d_1426101822599_430942_2209)** Class*
    - *The **[File](#_18_0_2_6340208_1485284639717_497586_4548)** Class*
    - *The **[GpUnit](#_17_0_2_4_78e0236_1389366233346_42391_2380)** Class*
    - *The **[Hash](#_18_0_2_6340208_1485894593826_736413_4615)** Class*
    - *The **[Image](#_18_0_2_6340208_1485284639720_737438_4549)** Class*
    - *The **[ImageData](#_18_0_2_6340208_1485894533655_402033_4588)** Class*
    - *The **[InternationalizedText](#_17_0_2_4_f71035d_1428953680097_700602_2220)** Class*
    - *The **[LanguageString](#_17_0_2_4_f71035d_1428953680095_709464_2219)** Class*
    - *The **[MarkMetric](#_18_0_2_6340208_1488984835132_736302_4685)** Class*
    - *The **[Party](#_17_0_2_4_78e0236_1389366278128_412819_2460)** Class*
    - *The **[PartyContest](#_17_0_2_4_d420315_1393514218965_55008_3144)** Class*
    - *The **[PartySelection](#_17_0_2_4_f71035d_1426519980658_594892_2511)** Class*
    - *The **[ReportingDevice](#_17_0_2_4_78e0236_1389798013459_389380_4178)** Class*
    - *The **[RetentionContest](#_18_0_2_6340208_1425646217522_163181_4554)** Class*
    - *The **[s](#_18_0_5_43401a7_1470911339574_174030_4504)** Class*
    - *The **[Status](#_18_0_5_43401a7_1475850314395_25201_4338)** Class*
    - *The **[VoteMark](#_18_0_2_6340208_1485892992407_492157_4635)** Class*
    - *The **[WriteInBallotSelectionVote](#_18_0_2_6340208_1485892911278_166697_4594)** Class*
# Enumerations
### <a name="_18_0_5_43401a7_1475850153090_186243_4311"></a>*The **BallotSelectionStatus** Enumeration*
    
Name | Value
---- | -----
`adjudicated`|
`generated-rules`|
`invalidated-rules`|
`needs-adjudication`|
`overvoted`|
`undervoted`|
`other`|
  ### <a name="_18_0_2_6340208_1472159006307_546162_4628"></a>*The **BallotStatus** Enumeration*
    
Name | Value
---- | -----
`adjudicated`|
`counted`|
`invalid`|
`needs-adjudication`|
`unreadable`|
`other`|
  ### <a name="_18_0_2_6340208_1488984734564_983877_4662"></a>*The **CastVoteRecordVersion** Enumeration*
    
Name | Value
---- | -----
`1.0`|
  ### <a name="_18_0_5_43401a7_1475850124791_123384_4291"></a>*The **ContestStatus** Enumeration*
    
Name | Value
---- | -----
`adjudicated`|
`invalidated-rules`|
`overvoted`|
`undervoted`|
`other`|
  ### <a name="_18_0_2_6340208_1493056057833_123746_4561"></a>*The **CVRComponentStatus** Enumeration*
    
Name | Value
---- | -----
  ### <a name="_18_0_2_6340208_1485894679180_11599_4655"></a>*The **HashType** Enumeration*
    
Name | Value
---- | -----
`md6`|
`sha-512`|
`other`|
  ### <a name="_17_0_2_4_f71035d_1425061188508_163854_2613"></a>*The **IdentifierType** Enumeration*
    
Name | Value
---- | -----
`fips`|
`local-level`|
`national-level`|
`ocd-id`|
`state-level`|
`other`|
  ### <a name="_17_0_2_4_f71035d_1431607637366_785815_2242"></a>*The **ReportingUnitType** Enumeration*
    
Name | Value
---- | -----
`combined-precinct`|
`polling-place`|
`precinct`|
`split-precinct`|
`vote-center`|
`other`|
  ### <a name="_18_0_5_43401a7_1483727563257_179426_4343"></a>*The **ReportType** Enumeration*
    
Name | Value
---- | -----
`adjudicated`|
`aggregated`|
`originating-device-export`|
`rcv-round`|
  ### <a name="_18_0_2_6340208_1485894157707_572874_4551"></a>*The **VoteMarkStatus** Enumeration*
    
Name | Value
---- | -----
`adjudicated-countable`|
`adjudicated-invalidated`|
`generated-countable-rules`|
`invalidated-rules`|
`invalidated-marginal-mark`|
`voter-countable`|
`other`|
  ### <a name="_18_0_5_43401a7_1483727021192_184103_4291"></a>*The **VoteVariation** Enumeration*
    
Name | Value
---- | -----
`approval`|
`borda`|
`cumulative`|
`majority`|
`n-of-m`|
`one-of-m`|
`plurality`|
`proportional`|
`range`|
`rcv`|
`super-majority`|
`other`|
  # Classes
### <a name="_18_0_5_43401a7_1475856712376_208252_4416"></a>*The **Annotation** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Message`|0..*|`string`|
`Name`|0..*|`string`|
`PreviousStatus`|0..1|`CVRComponentStatus`|
`TimeStamp`|0..1|`dateTime`|
### <a name="_17_0_2_4_78e0236_1389366932057_929676_2783"></a>*The **BallotMeasureContest** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
### <a name="_17_0_2_4_78e0236_1389372163799_981952_2926"></a>*The **BallotMeasureSelection** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Selection`|1|`InternationalizedText`|
### <a name="_17_0_2_4_78e0236_1389372124445_11077_2906"></a>*The **BallotSelection** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
### <a name="_18_0_5_43401a7_1474452890357_299022_4292"></a>*The **BallotSelectionVote** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{BallotSelection}`|0..1|`BallotSelection`|
`{Annotation}`|0..*|`Annotation`|
`{VoteMark}`|0..*|`VoteMark`|
`OtherStatus`|0..1|`string`|
`Position`|0..1|`integer`|
`Status`|0..*|`BallotSelectionStatus`|
`TotalNumberVotes`|0..1|`integer`|
### <a name="_17_0_2_4_78e0236_1389366272694_544359_2440"></a>*The **Candidate** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Code`|0..1|`Code`|
`Name`|0..1|`InternationalizedText`|
`Party`|0..1|`Party`|
### <a name="_17_0_2_4_78e0236_1389366970084_183781_2806"></a>*The **CandidateContest** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`NumberElected`|0..1|`integer`|
`PrimaryParty`|0..1|`Party`|
`VotesAllowed`|0..1|`integer`|
### <a name="_17_0_2_4_d420315_1392145640524_831493_2562"></a>*The **CandidateSelection** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Candidate`|0..*|`Candidate`|
`IsWriteIn`|0..1|`boolean`|
### <a name="_17_0_2_4_78e0236_1389366224561_797289_2360"></a>*The **CastVoteRecord** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{ContestVote}`|0..*|`ContestVote`|
`{Party}`|0..*|`Party`|
`{Annotation}`|0..*|`Annotation`|
`{Election}`|0..1|`Election`|
`BallotIdentifier`|0..1|`string`|
`BallotImage`|0..*|`ImageData`|
`BallotStatus`|0..*|`BallotStatus`|
`BallotStyleId`|0..1|`string`|
`BatchId`|0..1|`string`|
`BatchSequenceNumber`|0..1|`integer`|
`Identifier`|0..1|`string`|
`NumWriteIns`|0..1|`integer`|
`OriginatingDevice`|0..1|`ReportingDevice`|
`OtherBallotStatus`|0..1|`string`|
`SequenceNumber`|0..1|`string`|
`SheetNumber`|0..1|`integer`|
`SmallestVotingUnit`|0..1|`GpUnit`|
### <a name="_17_0_2_4_78e0236_1389366195564_913164_2300"></a>*The **CastVoteRecordReport** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{CastVoteRecord}`|0..*|`CastVoteRecord`|
`{Election}`|0..*|`Election`|
`{GpUnit}`|0..*|`GpUnit`|
`GeneratedDate`|1|`dateTime`|
`Notes`|0..1|`RichText`|
`OtherReportType`|0..1|`string`|
`ReportGeneratingDevice`|1..*|`ReportingDevice`|
`ReportType`|0..*|`ReportType`|
`Signature`|0..1|`Signature`|
`Version`|1|`CastVoteRecordVersion`|

```
Placeholder for an optional digital signature, using the W3C digital signature standard.
```
### <a name="_17_0_2_4_f71035d_1430405712653_451634_2410"></a>*The **Code** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`label`|0..1|`string`|
`OtherType`|0..1|`string`|
`Type`|1|`IdentifierType`|
`Value`|1|`string`|
### <a name="_17_0_2_4_78e0236_1389366251994_876831_2400"></a>*The **Contest** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{BallotSelection}`|0..*|`BallotSelection`|
`Abbreviation`|0..1|`string`|
`Code`|0..*|`Code`|
`Name`|0..1|`string`|
`OtherVoteVariation`|0..1|`string`|
`VoteVariation`|0..1|`VoteVariation`|
### <a name="_18_0_2_6340208_1469203058990_306165_4565"></a>*The **ContestVote** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{Contest}`|1|`Contest`|
`{BallotSelectionVote}`|0..*|`BallotSelectionVote`|
`{Annotation}`|0..*|`Annotation`|
`OtherStatus`|0..1|`string`|
`Overvotes`|0..1|`integer`|
`Selections`|0..1|`integer`|
`Status`|0..*|`ContestStatus`|
`Undervotes`|0..1|`integer`|
### <a name="_17_0_2_4_f71035d_1426101822599_430942_2209"></a>*The **Election** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{Contest}`|0..*|`Contest`|
`{Candidate}`|0..*|`Candidate`|
`Code`|0..*|`Code`|
`ElectionScope`|0..1|`GpUnit`|
`Name`|0..1|`string`|
### <a name="_18_0_2_6340208_1485284639717_497586_4548"></a>*The **File** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Data`|1|`base64Binary`|
`fileName`|0..1|`string`|
`mimeType`|0..1|`string`|

```
Contains the base64 binary contents of the file.
```
### <a name="_17_0_2_4_78e0236_1389366233346_42391_2380"></a>*The **GpUnit** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{ReportingDevice}`|0..*|`ReportingDevice`|
`Code`|0..*|`Code`|
`Name`|0..1|`string`|
`OtherType`|0..1|`string`|
`Type`|1|`ReportingUnitType`|
### <a name="_18_0_2_6340208_1485894593826_736413_4615"></a>*The **Hash** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`OtherType`|0..1|`string`|
`Type`|1|`HashType`|
`Value`|1|`string`|
### <a name="_18_0_2_6340208_1485284639720_737438_4549"></a>*The **Image** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
### <a name="_18_0_2_6340208_1485894533655_402033_4588"></a>*The **ImageData** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{Image}`|0..1|`Image`|
`{Hash}`|0..1|`Hash`|
`Location`|0..1|`anyURI`|
`Signature`|0..1|`Signature`|

```
Either a signature for the embedded image, or a detached signature for the image available at the specified location.
```
### <a name="_17_0_2_4_f71035d_1428953680097_700602_2220"></a>*The **InternationalizedText** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`label`|0..1|`string`|
`Text`|1..*|`LanguageString`|
### <a name="_17_0_2_4_f71035d_1428953680095_709464_2219"></a>*The **LanguageString** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Content`|1|`string`|
`language`|1|`language`|

```

```
### <a name="_18_0_2_6340208_1488984835132_736302_4685"></a>*The **MarkMetric** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Type`|1|`string`|
`Value`|1|`string`|
### <a name="_17_0_2_4_78e0236_1389366278128_412819_2460"></a>*The **Party** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Abbreviation`|0..1|`string`|
`Code`|0..*|`Code`|
`Name`|0..1|`InternationalizedText`|
### <a name="_17_0_2_4_d420315_1393514218965_55008_3144"></a>*The **PartyContest** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
### <a name="_17_0_2_4_f71035d_1426519980658_594892_2511"></a>*The **PartySelection** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Party`|1..*|`Party`|
### <a name="_17_0_2_4_78e0236_1389798013459_389380_4178"></a>*The **ReportingDevice** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Application`|0..1|`string`|
`Manufacturer`|0..1|`string`|
`Model`|0..1|`string`|
`Notes`|0..*|`string`|
`SerialNumber`|0..1|`string`|
### <a name="_18_0_2_6340208_1425646217522_163181_4554"></a>*The **RetentionContest** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Candidate`||`Candidate`|
### <a name="_18_0_5_43401a7_1470911339574_174030_4504"></a>*The **s** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
### <a name="_18_0_5_43401a7_1475850314395_25201_4338"></a>*The **Status** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
### <a name="_18_0_2_6340208_1485892992407_492157_4635"></a>*The **VoteMark** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{Annotation}`|0..*|`Annotation`|
`{MarkMetric}`|0..*|`MarkMetric`|
`NumberVotes`|0..1|`integer`|
`OtherStatus`|0..1|`string`|
`Position`|0..1|`integer`|
`Rank`|0..1|`integer`|
`Status`|0..*|`VoteMarkStatus`|
### <a name="_18_0_2_6340208_1485892911278_166697_4594"></a>*The **WriteInBallotSelectionVote** Class*



Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Image`|0..1|`ImageData`|
`Text`|0..1|`string`|
