<template>
  <div>
    <GeneralDetails />
    <ContactDetails />
    <EmploymentDetails />
    <EducationalQualification />
    <PreviousWorkExperience />
    <CredentialDetails />
    <References />
  </div>
</template>

<script>
import GeneralDetails from "./employeeDetails/generalDetails.vue";
import ContactDetails from "./employeeDetails/contactDetails.vue";
import EmploymentDetails from "./employeeDetails/employmentDetails.vue";
import EducationalQualification from "./employeeDetails/educationalQualification.vue";
import PreviousWorkExperience from "./employeeDetails/previousWorkExperience.vue";
import CredentialDetails from "./employeeDetails/credentialDetails.vue";
import References from "./employeeDetails/references.vue";
export default {
  name: "EmployeesGeneralDetails",
  components: {
    GeneralDetails,
    ContactDetails,
    EmploymentDetails,
    EducationalQualification,
    PreviousWorkExperience,
    CredentialDetails,
    References,
  },
};
</script>