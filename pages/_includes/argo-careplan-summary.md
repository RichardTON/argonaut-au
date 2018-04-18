﻿#### Complete Summary of the Mandatory Requirements

1.  A narrative summary in `CarePlan.text`
    -   [CarePlan.text.status] is either “generated” or “additional”

1.  One reference to a patient in `CarePlan.subject`
1.  One status in `CarePlan.status`
    -   CarePlan.status is bound to [CarePlanStatus](http://hl7.org/fhir/ValueSet-care-plan-status.html) Value set
1.  A category in `Careplan.category` which must have:
    -   a fixed `Careplan.category.coding.system` = [http://argonaut.hl7.org]
    -   a fixed 'Careplan.category.coding.code' = “assess-plan”



  [CarePlan.text.status]: http://hl7.org/fhir/ValueSet-narrative-status.html
  [CarePlanStatus]: http://hl7.org/fhir/ValueSet-care-plan-status.html
  [http://argonaut.hl7.org]: ValueSet-argo-codesystem.html
