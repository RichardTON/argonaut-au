-----------

**`GET /AllergyIntolerance?patient=[id]`**

Example:

[GET  https://fhir-open-api-dstu3.smarthealthit.org/AllergyIntolerance?patient=1137192](https://fhir-open-api-dstu3.smarthealthit.org/AllergyIntolerance?patient=1137192)

*Support:* Mandatory to support search by patient.

*Implementation Notes:* Search for all allergies for a patient. Fetches a bundle of all AllergyIntolerance resources for the specified patient [(how to search by reference)].

*Response Class:*

-   (Status 200): successful operation
-   (Status 400): invalid parameter
-   (Status 401/4xx): unauthorized request
-   (Status 403): insufficient scope


  [(how to search by reference)]: http://hl7.org/fhir/STU3/search.html#reference
  [(how to search by token)]: http://hl7.org/fhir/STU3/search.html#token
  [Composite Search Parameters]: http://hl7.org/fhir/search.html#combining
