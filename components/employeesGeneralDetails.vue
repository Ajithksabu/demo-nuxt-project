<template>
  <div>
    <GeneralDetails />
    <ContactDetails />
    <EmploymentDetails />
    <EducationalQualification />
    <PreviousWorkExperience />
    <CredentialDetails />
    <References />
    <div class="pt-5">
      <div class="flex justify-end">
        <button
          type="button"
          class="
            bg-white
            py-2
            px-4
            border border-gray-300
            rounded-md
            shadow-sm
            text-sm
            font-medium
            text-gray-700
            hover:bg-gray-50
            focus:outline-none
            focus:ring-2
            focus:ring-offset-2
            focus:ring-indigo-500
          "
        >
          Cancel
        </button>
        <button
          type="submit"
          class="
            ml-3
            mr-5
            inline-flex
            justify-center
            py-2
            px-4
            border border-transparent
            shadow-sm
            text-sm
            font-medium
            rounded-md
            text-white
            bg-indigo-600
            hover:bg-indigo-700
            focus:outline-none
            focus:ring-2
            focus:ring-offset-2
            focus:ring-indigo-500
          "
        >
          Save
        </button>
      </div>
    </div>
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