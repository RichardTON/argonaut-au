-----------

**`GET [base]/Observation?patient=[id]&code=72166-2`**

Example:

[GET https://fhir-open-api-dstu3.smarthealthit.org/Observation?patient=1032702&code=72166-2](https://fhir-open-api-dstu3.smarthealthit.org/Observation?patient=1032702&code=72166-2)

*Support:* Mandatory to support search by patient and LOINC = '72166-2'.

*Implementation Notes:*  Search based on smoking status LOINC code. Fetches a bundle of all Observation resources with Observation.code of Tobacco Smoking Status for the specified patient [(how to search by reference)] and [(how to search by token)].

*Response Class:*

-   (Status 200): successful operation
-   (Status 400): invalid parameter
-   (Status 401/4xx): unauthorized request
-   (Status 403): insufficient scope


  [(how to search by reference)]: http://hl7.org/fhir/STU3/search.html#reference
  [(how to search by token)]: http://hl7.org/fhir/STU3/search.html#token
  [Composite Search Parameters]: http://hl7.org/fhir/search.html#combining
  [(how to search by date)]: http://hl7.org/fhir/STU3/search.html#date
  [(how to search by string)]: http://hl7.org/fhir/STU3/search.html#string
