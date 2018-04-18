-----------

`GET /MedicationStatement?patient={id}`

**Example:**

[GET http://fhirtest.uhn.ca/baseDstu3/MedicationStatement?patient=14676](http://fhirtest.uhn.ca/baseDstu3/MedicationStatement?patient=14676)

*Support:* Mandatory for client to support search by patient.  Optional for server to support.

*Implementation Notes:*  Used when the server application represents the medication using either an inline code or a contained Medication resource. This searches for all MedicationStatement resources for a patient and returns a Bundle of all MedicationStatement resources for the specified patient.  [(how to search by reference)].

*Response Class:*

-   (Status 200): successful operation
-   (Status 400): invalid parameter
-   (Status 401/4xx): unauthorized request
-   (Status 403): insufficient scope

-----------

`GET /MedicationStatement?patient={id}&_include=MedicationStatement:medication`

**Example:**

[GET http://fhirtest.uhn.ca/baseDstu3/MedicationStatement?patient=14676&_include=MedicationStatement:medication](http://fhirtest.uhn.ca/baseDstu3/MedicationStatement?patient=14676&_include=MedicationStatement:medication)


*Support:* Mandatory for client to support search by patient using the include parameter.  Optional for server to support.

*Implementation Notes:*  Used when the server application represents the medication with an external reference to  a Medication resource. This searches for all MedicationStatement resources for a patient and returns a Bundle of all MedicationStatement and Medication resources for the specified patient.  [(how to search by reference)].

*Response Class:*

-   (Status 200): successful operation
-   (Status 400): invalid parameter
-   (Status 401/4xx): unauthorized request
-   (Status 403): insufficient scope

-------

  [(how to search by reference)]: http://hl7.org/fhir/STU3/search.html#reference
  [(how to search by token)]: http://hl7.org/fhir/STU3/search.html#token
  [Composite Search Parameters]: http://hl7.org/fhir/search.html#combining
  [(how to search by date)]: http://hl7.org/fhir/STU3/search.html#date
