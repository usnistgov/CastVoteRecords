# mCDF Profile for Contest Selection Capture

This profile of the NIST Cast Vote Records Common Data Format 1.0 is designed to support the capture of contest option selections encoded onto paper vote records using various machine readable symbologies. This profile includes only the CVR classes and properties required to convey the following:

-	The election associated with the ballot
-	The ballot style associated with the ballot
-	The election authority who created the ballot style
-	The contest option selections made, including any write-ins
-	An optional link to the ballot definition associated with the ballot style

This profile uses the [Micro Common Data Format](https://github.com/usnistgov/mcdf) (or mCDF)

## Repo Structure

| Name                                                      | Description                                    |
|-----------------------------------------------------------|------------------------------------------------|
| imgs/                                                     | Images for mCDF CSC Prototype instructions     |
| mapping_csc_mcdf_to_bd.xml                                | Mapping to BD XML Example                      |
| mapping_csc_mcdf_to_cvr.xml                               | Mapping to CVR XML Example                     |
| mCDF Profile for Contest Selection Capture Descriptor.xml | mCDF Profile using NIST HL7v2 Profiling Format |
| mCDF Profile for Contest Selection Capture.docx           | CSC Profile Document                           |
| mCDF Profile for Contest Selection Capture.svg            | UML Model of Contest Selection Capture Profile |
| [mCDF Prototype Instructions.md](./mCDF%20Prototype%20Instructions.md)                            | Instructions for running mCDF Prototype        |
| mCDF Prototype.pdf                                        | mCDF Prototype                                 |
| README.md                                                 | This document                                  |
