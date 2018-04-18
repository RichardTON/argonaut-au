


This profile sets minimum expectations for the [Observation] resource to record, search and fetch smoking status data associated with a patient. It identifies which core elements, extensions, vocabularies and value sets **SHALL** be present in the resource when using this profile.

**Example Usage Scenarios:**

The following are example usage scenarios for the Argonaut SmokingStatus
profile:

- Query for Smoking Status of a particular patient
- Record Smoking Status of a particular patient  

##### Mandatory Data Elements and Terminology


The following data-elements are mandatory (i.e data MUST be present). These are presented below in a simple human-readable explanation.  Profile specific guidance and examples are provided as well.  The [**Formal Profile Definition**](#profile) below provides the  formal summary, definitions, and  terminology requirements.  

**Each Observation must have:**

1.  a status
1.  a fixed code for smoking observation
1.  a patient
1.  a date representing when the smoking status was recorded
1.  a result value code for smoking status


**Profile specific implementation guidance:**

* Smoking observation LOINC = 72166-2 *Tobacco smoking status NHIS*


#### Examples

   - [Some Day Smoker](Observation-some-day-smoker.html)

   [Observation]: http://hl7.org/fhir/observation.html
