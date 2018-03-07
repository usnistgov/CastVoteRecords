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
`adjudicated`|To indicate that the ballot selection was adjudicated.
`generated-rules`|To indicate that the ballot selection was generated per contest rules.
`invalidated-rules`|To indicate that the ballot selection was invalidated by the generating device because of contest rules.
`needs-adjudication`|To indicate that the ballot selection was flagged by the generating device for adjudication.
`overvoted`|To indicate that the ballot selection was overvoted.
`undervoted`|To indicate that the ballot selection was undervoted.
`other`|Used when no other value in this enumeration applies to the ballot selection.
  ### <a name="_18_0_2_6340208_1472159006307_546162_4628"></a>*The **BallotStatus** Enumeration*
    
Name | Value
---- | -----
`adjudicated`|To indicate that the ballot has been adjudicated.
`counted`|To indicate that the ballot has been counted.
`invalid`|To indicate that the ballot is invalid (not a ballot).
`needs-adjudication`|To indicate that the ballot needs to be adjudicated.
`unreadable`|To indicate that the ballot was not entirely readable by the scanner.
`other`|Used when no other value in this enumeration applies to the ballot.
  ### <a name="_18_0_2_6340208_1488984734564_983877_4662"></a>*The **CastVoteRecordVersion** Enumeration*
    
Name | Value
---- | -----
`1.0`|
  ### <a name="_18_0_5_43401a7_1475850124791_123384_4291"></a>*The **ContestStatus** Enumeration*
    
Name | Value
---- | -----
`adjudicated`|The contest has been adjudicated.
`invalidated-rules`|Used to indicate that the contest has been invalidated by the generating device because of contest rules.
`overvoted`|Used to indicate that the contest was overvoted.
`undervoted`|Used to indicate that the contest was undervoted.
`other`|Used when no other value in this enumeration applies to the contest.
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
`fips`|Used to indicate that the identifier is a FIPS code.
`local-level`|Used to indicate that the identifier is from a local-level scheme, i.e., unique to a county or city.
`national-level`|Used to indicate that the identifier is from a national-level scheme other than FIPS or OCD-ID.
`ocd-id`|Used to indicate that the identifier is from the OCD-ID scheme.
`state-level`|Used to indicate that the identifier is from a state-level scheme, i.e., unique to a particular state.
`other`|Used when no other value in this enumeration applies to the identifier type.
  ### <a name="_17_0_2_4_f71035d_1431607637366_785815_2242"></a>*The **ReportingUnitType** Enumeration*
    
Name | Value
---- | -----
`combined-precinct`|Used to indicate a combined precinct.
`polling-place`|Used to indicate a polling place.
`precinct`|Used to indicate a precinct.
`split-precinct`|Used to indicate a split-precinct.
`vote-center`|Used to indicate a vote-center.
`other`|
  ### <a name="_18_0_5_43401a7_1483727563257_179426_4343"></a>*The **ReportType** Enumeration*
    
Name | Value
---- | -----
`adjudicated`|Used when the report contains adjudications.
`aggregated`|Used when the report is an aggregation of device reports.
`originating-device-export`|Used when the report is an export from a device such as a scanner.
`rcv-round`|Used when the report is the result of a ranked choice voting round.
  ### <a name="_18_0_2_6340208_1485894157707_572874_4551"></a>*The **VoteMarkStatus** Enumeration*
    
Name | Value
---- | -----
`adjudicated-countable`|Used to indicate that the vote mark was adjudicated and is tabulatable.
`adjudicated-invalidated`|Used to indicate that the vote mark was invalidated because of adjudication and is not tabulatable.
`generated-countable-rules`|Used to indicate that the vote mark was generated by the generating device per contest rules and is tabulatable.
`invalidated-rules`|Used to indicate that the vote mark was invalidated by the generating device because of contest rules and is not tabulatable.
`invalidated-marginal-mark`|Used to indicate that the vote mark contains a marginal mark by the voter and is not tabulatable.
`voter-countable`|Used to indicate that the vote mark was made by the voter and is recognized as valid and is tabulatable.
`other`|Used when no other value in the enumeration applies to the vote mark.
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

Used to record annotations made by one or more adjudicators.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Message`|0..*|`string`|A message created by the annotator(s).
`Name`|0..*|`string`|Name(s) of the adjudicator(s).
`PreviousStatus`|0..1|`CVRComponentStatus`|The previous status (prior to the recording of the annotation) of the item being annotated, i.e., the CVR as a whole, a contest, a specific ballot selection, or a specific ballot mark.
`TimeStamp`|0..1|`dateTime`|The date and time of an annotation.
### <a name="_17_0_2_4_78e0236_1389366932057_929676_2783"></a>*The **BallotMeasureContest** Class*

Indentifies the type of contest as involving a ballot measures. Inherits attributes from the Contest class.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
### <a name="_17_0_2_4_78e0236_1389372163799_981952_2926"></a>*The **BallotMeasureSelection** Class*

Class for a type of ballot selection specific to ballot measures, e.g., "yes", "no".

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Selection`|1|`InternationalizedText`|The selection, i.e., 'yes', 'no'.
### <a name="_17_0_2_4_78e0236_1389372124445_11077_2906"></a>*The **BallotSelection** Class*

Abstract class for a ballot selection in a contest on the ballot corresponding to this CVR or a CVR in the collection of CVRs. Classes for specific types of ballot selections inherit the attributes and define their own.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
### <a name="_18_0_5_43401a7_1474452890357_299022_4292"></a>*The **BallotSelectionVote** Class*

Used to indicate a ballot selection or marginal mark. The ballot selection could have been: a) marked by the voter, including for a write-in, or b) marked (generated) by the scanner per contest rules, or c) marked through adjudication, or d) determined by the scanner as being a marginal mark.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{BallotSelection}`|0..1|`BallotSelection`|This will most typically have a multiplicity of 1, but can be multiple for contests that allow selecting multiple choices. The order of this association can be used to determine candidate preference for appropriate voting variations.
`{Annotation}`|0..*|`Annotation`|Used to record an annotation made by one or more individuals, e.g., adjudicating aspects of the ballot.
`{VoteMark}`|0..*|`VoteMark`|Contains further information about the mark made (e.g., by the voter) for the ballot selection.
`OtherStatus`|0..1|`string`|If Status is 'other', contains the ballot status.
`Position`|0..1|`integer`|The ordinal position of the selection as is appreared on the ballot.
`Status`|0..*|`BallotSelectionStatus`|The status of the ballot selection, e.g., 'marked-voter' for marked by the voter, taken from the BallotSelectionStatus enumeration.
`TotalNumberVotes`|0..1|`integer`|For cumulative or range voting variations, this attribute represents the total number of votes indicated across all marks.
### <a name="_17_0_2_4_78e0236_1389366272694_544359_2440"></a>*The **Candidate** Class*

Identifies a candidate in a contest on the ballot corresponding to the CVR.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Code`|0..1|`Code`|A code or identifier associated with the candidate.
`Name`|0..1|`InternationalizedText`|Candidate's name as listed on the ballot.
`Party`|0..1|`Party`|The party associated with the candidate.
### <a name="_17_0_2_4_78e0236_1389366970084_183781_2806"></a>*The **CandidateContest** Class*

Identifies the type of contest as involving one or more candidates. Inherits attributes from the Contest class.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`NumberElected`|0..1|`integer`|The number of candidates to be elected in the contest.
`PrimaryParty`|0..1|`Party`|The party associated with the contest, if a partisan primary.
`VotesAllowed`|0..1|`integer`|The number of votes allowed in the contest, e.g., 3 for a 'choose 3 of 5 candidates' contest.
### <a name="_17_0_2_4_d420315_1392145640524_831493_2562"></a>*The **CandidateSelection** Class*

Class for a type of ballot selection specific to selecting a candidate in a contest for an office.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Candidate`|0..*|`Candidate`|The candidate associated with this ballot selection.
`IsWriteIn`|0..1|`boolean`|A flag to indicate if the candidate selection is associated with a write-in.
### <a name="_17_0_2_4_78e0236_1389366224561_797289_2360"></a>*The **CastVoteRecord** Class*

Represents a CVR generated by a scanner or other vote capture device, containing indications of the contests and ballot selections selected because of the voter’s ballot choices, as well as other information for auditing and annotation. Each sheet of a multi-page paper ballot is represented by an individual CVR, e.g., if all sheets of a 5-sheet ballot are scanned, 5 CVRs will be generated.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{ContestVote}`|0..*|`ContestVote`|
`{Party}`|0..*|`Party`|
`{Annotation}`|0..*|`Annotation`|
`{Election}`|0..1|`Election`|
`BallotIdentifier`|0..1|`string`|An identifier for the ballot that this CVR represents. If provided, this number must be the same on all CVRs that represent individual sheets from the same multi-sheet ballot.
`BallotImage`|0..*|`ImageData`|An ordered list of pointers to image files of the scanner ballots.
`BallotStatus`|0..*|`BallotStatus`|The status of the CVR, e.g., adjudicated, counted, etc.
`BallotStyleId`|0..1|`string`|An identifier of the ballot style of the ballot associated with this CVR.
`BatchId`|0..1|`string`|The identifier for the batch that includes this CVR.
`BatchSequenceNumber`|0..1|`integer`|The sequence number of the corresponding paper ballot within a batch.
`Identifier`|0..1|`string`|An optional, unique identifier for this CVR, used to link the CVR with the corresponding paper ballot, e.g., would contain the same value that the scanner stamped on the paper ballot when scanned.
`NumWriteIns`|0..1|`integer`|The total number of write-ins in all contests of the CVR.
`OriginatingDevice`|0..1|`ReportingDevice`|The device that generated the cast vote records.
`OtherBallotStatus`|0..1|`string`|When BallotStatus is 'other', contains the ballot status.
`SequenceNumber`|0..1|`string`|The sequence number for this CVR. This represents the ordinal number that this CVR was processed in by the tabulating device.
`SheetNumber`|0..1|`integer`|Indicates the sheet number of the multi-sheet ballot being represented.
`SmallestVotingUnit`|0..1|`GpUnit`|The smallest piece of geography associated with a voter's ballot or cast vote record at the smallest or lowest level (typically a precinct or split-precinct).
### <a name="_17_0_2_4_78e0236_1389366195564_913164_2300"></a>*The **CastVoteRecordReport** Class*

The root class/element; attributes pertain to the status and format of the report and when generated.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{CastVoteRecord}`|0..*|`CastVoteRecord`|
`{Election}`|0..*|`Election`|
`{GpUnit}`|0..*|`GpUnit`|
`GeneratedDate`|1|`dateTime`|Identifies the time that the election report was generated.
`Notes`|0..1|`RichText`|Notes that can be added as appropriate, presumably by an adjudicator.
`OtherReportType`|0..1|`string`|If ReportType is 'other', this contains the report type.
`ReportGeneratingDevice`|1..*|`ReportingDevice`|Identification of the device that has generated this CVR report.
`ReportType`|0..*|`ReportType`|The type of report, using the ReportType enumeration.
`Signature`|0..1|`Signature`|Placeholder for an optional digital signature, using the W3C digital signature standard.
`Version`|1|`CastVoteRecordVersion`|The version of the CVR specification being used (1.0).

```
Placeholder for an optional digital signature, using the W3C digital signature standard.
```
### <a name="_17_0_2_4_f71035d_1430405712653_451634_2410"></a>*The **Code** Class*

Used in Election, GpUnit, Contest, Candidate, Party, to identify an associated code and the type of code.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`label`|0..1|`string`|A label associated with the code, used as needed.
`OtherType`|0..1|`string`|If Type is 'other', the type of code.
`Type`|1|`IdentifierType`|Used to indicate the type of code, from the IdentifierType enumeration.
`Value`|1|`string`|The value of the code, i.e., the identifier.
### <a name="_17_0_2_4_78e0236_1389366251994_876831_2400"></a>*The **Contest** Class*

Abstract class for a contest on the ballot that corresponds to this CVR. Classes for specific types of contests inherit the attributes and define their own.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{BallotSelection}`|0..*|`BallotSelection`|
`Abbreviation`|0..1|`string`|An abbreviation associated with the contest.
`Code`|0..*|`Code`|A code or identified used for this contest.
`Name`|0..1|`string`|Title or name of the contest, e.g., "Governor" or "Question on Legalization of Gambling".
`OtherVoteVariation`|0..1|`string`|If VoteVariation is 'other', the vote variation for this contest.
`VoteVariation`|0..1|`VoteVariation`|The vote variation for this contest.
### <a name="_18_0_2_6340208_1469203058990_306165_4565"></a>*The **ContestVote** Class*

Identifies a contest in which a ballot selection was made and associates the ballot selection(s). Overvotes plus Undervotes plus TotalVotes must equal the number of votes allowable in the contest, e.g., in a "chose 3 of 5" contest in which the voter chooses only 2, then Overvotes = 0, Undervotes = 1, and TotalVotes = 2, which adds up to the number of votes allowable = 3.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{Contest}`|1|`Contest`|
`{BallotSelectionVote}`|0..*|`BallotSelectionVote`|
`{Annotation}`|0..*|`Annotation`|Used for an annotation that applies to the contest.
`OtherStatus`|0..1|`string`|If Status is 'other', the status of the contest
`Overvotes`|0..1|`integer`|The number of votes lost due to overvoting.
`Selections`|0..1|`integer`|??? Ask Sam.
`Status`|0..*|`ContestStatus`|The status of the contest, e.g., overvoted, undervoted, from the ContestStatus enumeration.
`Undervotes`|0..1|`integer`|The number of votes lost due to undervoting.
### <a name="_17_0_2_4_f71035d_1426101822599_430942_2209"></a>*The **Election** Class*

Serves to organize the CVRs per an election, e.g., for a device, a precinct, etc., and defines the contests, ballot selections, and candidates referenced in the CVRs.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{Contest}`|0..*|`Contest`|Used for establishing a collection of contests that will be referenced by the CVRs.
`{Candidate}`|0..*|`Candidate`|Used to establish a collection of candidates, used for linking candidates to contests.
`Code`|0..*|`Code`|Used for a code associated with the election, e.g., a precinct identifier if the election scope is a precinct.
`ElectionScope`|0..1|`GpUnit`|Identifies the election scope, i.e., the political geography corresponding to the election.
`Name`|0..1|`string`|A text string identifying the election.
### <a name="_18_0_2_6340208_1485284639717_497586_4548"></a>*The **File** Class*

Used to hold the contents of a file, generally an image of a paper ballot or a write-in entered on to a paper ballot.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Data`|1|`base64Binary`|Contains the base64 binary contents of the file.
`fileName`|0..1|`string`|Contains the name of the file or an identifier of the file.
`mimeType`|0..1|`string`|The mime type of the file, e.g., image/jpeg.

```
Contains the base64 binary contents of the file.
```
### <a name="_17_0_2_4_78e0236_1389366233346_42391_2380"></a>*The **GpUnit** Class*

Used for identifying the geographical location, i.e., the reporting unit for the report generation device, which could be the precinct location of a scanner that generates a collection of CVRs.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{ReportingDevice}`|0..*|`ReportingDevice`|The collection of cast vote records associated with the reporting unit and the reporting device.
`Code`|0..*|`Code`|A code associated with the reporting unit.
`Name`|0..1|`string`|Name of the reporting unit.
`OtherType`|0..1|`string`|If Type is 'other', contains the reporting unit type.
`Type`|1|`ReportingUnitType`|Type of reporting unit, e.g., precinct, split-precinct, vote center, etc.
### <a name="_18_0_2_6340208_1485894593826_736413_4615"></a>*The **Hash** Class*

Contains a hash associated with the file.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`OtherType`|0..1|`string`|If Type is 'other', the type of the hash.
`Type`|1|`HashType`|The type of the hash, from the HashType enumeration.
`Value`|1|`string`|The hash value, encoded as a string.
### <a name="_18_0_2_6340208_1485284639720_737438_4549"></a>*The **Image** Class*

Used for a file containing an image, e.g., an image of a write-in on a paper ballot. .

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
### <a name="_18_0_2_6340208_1485894533655_402033_4588"></a>*The **ImageData** Class*

Used for an image file, contains information about the file.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{Image}`|0..1|`Image`|
`{Hash}`|0..1|`Hash`|
`Location`|0..1|`anyURI`|A pointer to the location of the image file.
`Signature`|0..1|`Signature`|Either a signature for the embedded image, or a detached signature for the image available at the specified location.

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

MarkMetric represents some generic measurement of a mark when the scanner can assign it, such as for mark density or quality. The type of the metric being used is determined by the 'Type' attribute of a MarkMetric instance.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Type`|1|`string`|The specific type of metric being used to determine quality. The supplied type must be specific enough that the attached value can be accurately verified later. For example, 'Acme Mark Density' may be a sufficiently specific type. However, if different machines determine the metric using a different algorithm, then it would be necessary to be more specific: 'Acme ImageCast Precinct Mark Density'
`Value`|1|`string`|The string value of the metric specified by Type
### <a name="_17_0_2_4_78e0236_1389366278128_412819_2460"></a>*The **Party** Class*

Class for describing information about a political party associated with the CVR.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Abbreviation`|0..1|`string`|Short name for the party, e.g., "DEM".
`Code`|0..*|`Code`|
`Name`|0..1|`InternationalizedText`|Official full name of the party, e.g., "Republican".
### <a name="_17_0_2_4_d420315_1393514218965_55008_3144"></a>*The **PartyContest** Class*

Identifies the type of contest as involving a straight party selection. Inherits attributes from the Contest class.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
### <a name="_17_0_2_4_f71035d_1426519980658_594892_2511"></a>*The **PartySelection** Class*

For a ballot selection specific to a party selection, i.e., for a ballot selection in a straight-party contest.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Party`|1..*|`Party`|The party associated with the ballot selection.
### <a name="_17_0_2_4_78e0236_1389798013459_389380_4178"></a>*The **ReportingDevice** Class*

Used for identifying the device that has generated the CVRs. CastVoteRecordReport refers to this class as ReportGeneratingDevice.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Application`|0..1|`string`|The application associated with the reporting device.
`Manufacturer`|0..1|`string`|Manufacturer of the reporting device.
`Model`|0..1|`string`|Manufacturer's model of the reporting device.
`Notes`|0..*|`string`|Additional explanatory notes as applicable.
`SerialNumber`|0..1|`string`|Serial number or other identification that can uniquely identify the reporting device.
### <a name="_18_0_2_6340208_1425646217522_163181_4554"></a>*The **RetentionContest** Class*

Identifies the type of contest as involving a retention, such as for a judicial retention. Similar to a ballot measure contest and inherits attributes from Contest.

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

Contains additional information about a (voter's) mark in a ballot selection. The number of potential VoteMarks that should be associated with a BallotSelection is (for paper ballots) the same as the number of ovals next to a particular choice. There will be usually 1 instance of VoteMark for plurality voting, but there could be multiple instances for RCV, approval, cumulative, or other vote variations in which a voter can select multiple candidates.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`{Annotation}`|0..*|`Annotation`|
`{MarkMetric}`|0..*|`MarkMetric`|
`NumberVotes`|0..1|`integer`|Used for an annotation that applies to the ballot selection.
`OtherStatus`|0..1|`string`|If Status is 'other', the status of the ballot selection.
`Position`|0..1|`integer`|The ordinal position of the mark within the ballot selection.
`Rank`|0..1|`integer`|For the RCV voting variation, the rank chosen by the voter.
`Status`|0..*|`VoteMarkStatus`|Status of the mark, e.g., marked-voter for marked by the voter, from the VoteMarkStatus enumeration.
### <a name="_18_0_2_6340208_1485892911278_166697_4594"></a>*The **WriteInBallotSelectionVote** Class*

Used when the ballot selection is for a write-in. WriteInBallotSelectionVote is a subclass of BallotSelectionVote and has additional attributes for the image and text of the write-in.

Attribute | Multiplicity | Type | Attribute Description
--------- | ------------ | ---- | ---------------------
`Image`|0..1|`ImageData`|Used for the image of the write-in from paper ballot in base64 binary encoding and/or a file identifier for the file containing the image of the write-in.
`Text`|0..1|`string`|Used for the text of the write-in. If the CVR is produced from a handwritten write-in on a paper ballot, the text would be added via adjudication.
