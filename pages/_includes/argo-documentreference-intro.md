﻿#### U.S. Argonaut DocumentReference Profile


##### Scope and Usage

This profile sets minimum expectations  for searching and fetching patient documents using the [DocumentReference Resource]. It is inspired by ITI-68 in [IHE MHD] specification.  It identifies the mandatory core elements, extensions, vocabularies and value sets which **SHALL** be present in the DocumentReference resource when using this profile.

**Example Usage Scenarios:**

The following are example usage scenarios for the Argonaut AllergyIntolerance
profile:

-   Query for all documents belonging to a Patient
-   Query for clinical summary information about a patient (access a patient's Continuity of Care Document (CCD))

##### Mandatory Data Elements and Terminology


The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation.  Profile specific guidance and examples are provided as well.  The [**Formal Profile Definition**](#profile) below provides the  formal summary, definitions, and  terminology requirements.  

**Each DocumentReference must have:**

1.  a patient
1.  a code describing the type of document
1.  when the reference was created
1.  a status
1.  an https address where the document can be retrieved
1.  a code identifying the specific details about the format of the document — over and above the content's MIME type

In addition it should have ( if available) :

1.  an identifier
1.  a document creation date
1.  the patient encounter date that is being referenced


**Profile specific implementation guidance:**

For a C-CDA Clinical Summary of Care (CCD):

-   The document type code is the LOINC code  [34133-9](http://s.details.loinc.org/LOINC/34133-9.html?sections=Comprehensive) *Summary of episode note*.
-   The format code is `urn:hl7-org:sdwg:ccda-structuredBody:2.1`
-   The https address may refer to a FHIR Binary Resource (i.e. [base]/Binary/[id]) address on the server
-   The https address may have a parameter that identifies the patient (e.g. GET [url]?patient=[id]). Argonaut servers SHOULD not require this parameter, but for IHE compatibility reasons SHALL allow it to be provided, and SHALL check that it is correct if it is provided.

#### Examples

   - [DocumentReference-episode-summary](DocumentReference-episode-summary.html) Retrieve a URL for an episode summary note (CCD).

[DocumentReference Resource]: http://hl7.org/fhir/documentreference.html
[IHE MHD]: http://ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_Suppl_MHD.pdf
