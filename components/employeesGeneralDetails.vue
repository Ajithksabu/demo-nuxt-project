<template>
  <div id="accordion-collapse" data-accordion="collapse" class="mt-4">
    <h2 id="accordion-collapse-heading-1">
      <button
        type="button"
        class="
          flex
          justify-between
          items-center
          p-5
          w-full
          font-medium
          text-left text-gray-500
          rounded-t-lg
          border border-b-0 border-gray-200
          hover:bg-gray-100
        "
        @click.prevent="handleAccordion(1)"
        data-accordion-target="#accordion-collapse-body-1"
        aria-expanded="true"
        aria-controls="accordion-collapse-body-1"
      >
        <span>General details</span>
        <svg
          data-accordion-icon
          class="w-6 h-6 shrink-0"
          :class="{ 'rotate-180': accordionNo === 1 }"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </button>
    </h2>
    <div
      id="accordion-collapse-body-1"
      class="border border-x-1 border-gray-200"
      :class="{ hidden: accordionNo !== 1 }"
      aria-labelledby="accordion-collapse-heading-1"
    >
      <GeneralDetails />
    </div>
    <h2 id="accordion-collapse-heading-2">
      <button
        type="button"
        class="
          flex
          justify-between
          items-center
          p-5
          w-full
          font-medium
          text-left text-gray-500
          border border-b-0 border-gray-200
          hover:bg-gray-100
        "
        @click.prevent="handleAccordion(2)"
        data-accordion-target="#accordion-collapse-body-2"
        aria-expanded="false"
        aria-controls="accordion-collapse-body-2"
      >
        <span>Contact details</span>
        <svg
          data-accordion-icon
          class="w-6 h-6 shrink-0"
          :class="{ 'rotate-180': accordionNo === 2 }"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </button>
    </h2>
    <div
      id="accordion-collapse-body-1"
      class="border border-x-1 border-gray-200"
      :class="{ hidden: accordionNo !== 2 }"
      aria-labelledby="accordion-collapse-heading-1"
    >
      <ContactDetails />
    </div>
    <h2 id="accordion-collapse-heading-3">
      <button
        type="button"
        class="
          flex
          justify-between
          items-center
          p-5
          w-full
          font-medium
          rounded-b-lg
          text-left text-gray-500
          border border-gray-200
          hover:bg-gray-100
        "
        @click.prevent="handleAccordion(3)"
        data-accordion-target="#accordion-collapse-body-3"
        aria-expanded="false"
        aria-controls="accordion-collapse-body-3"
      >
        <span>Employment details</span>
        <svg
          data-accordion-icon
          class="w-6 h-6 shrink-0"
          :class="{ 'rotate-180': accordionNo === 3 }"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </button>
    </h2>
    <div
      id="accordion-collapse-body-1"
      class="border border-x-1 border-gray-200"
      :class="{ hidden: accordionNo !== 3 }"
      aria-labelledby="accordion-collapse-heading-1"
    >
      <EmploymentDetails />
    </div>
    <h2 id="accordion-collapse-heading-3">
      <button
        type="button"
        class="
          flex
          justify-between
          items-center
          p-5
          w-full
          font-medium
          rounded-b-lg
          text-left text-gray-500
          border border-gray-200
          hover:bg-gray-100
        "
        @click.prevent="handleAccordion(4)"
        data-accordion-target="#accordion-collapse-body-3"
        aria-expanded="false"
        aria-controls="accordion-collapse-body-3"
      >
        <span>Educational qualifications</span>
        <svg
          data-accordion-icon
          class="w-6 h-6 shrink-0"
          :class="{ 'rotate-180': accordionNo === 4 }"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </button>
    </h2>
    <div
      id="accordion-collapse-body-1"
      class="border border-x-1 border-gray-200"
      :class="{ hidden: accordionNo !== 4 }"
      aria-labelledby="accordion-collapse-heading-1"
    >
      <EducationalQualification />
    </div>
    <h2 id="accordion-collapse-heading-3">
      <button
        type="button"
        class="
          flex
          justify-between
          items-center
          p-5
          w-full
          font-medium
          rounded-b-lg
          text-left text-gray-500
          border border-gray-200
          hover:bg-gray-100
        "
        @click.prevent="handleAccordion(5)"
        data-accordion-target="#accordion-collapse-body-3"
        aria-expanded="false"
        aria-controls="accordion-collapse-body-3"
      >
        <span>Previous work experience</span>
        <svg
          data-accordion-icon
          class="w-6 h-6 shrink-0"
          :class="{ 'rotate-180': accordionNo === 5 }"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </button>
    </h2>
    <div
      id="accordion-collapse-body-1"
      class="border border-x-1 border-gray-200"
      :class="{ hidden: accordionNo !== 5 }"
      aria-labelledby="accordion-collapse-heading-1"
    >
      <PreviousWorkExperience />
    </div>
    <h2 id="accordion-collapse-heading-3">
      <button
        type="button"
        class="
          flex
          justify-between
          items-center
          p-5
          w-full
          font-medium
          rounded-b-lg
          text-left text-gray-500
          border border-gray-200
          hover:bg-gray-100
        "
        @click.prevent="handleAccordion(6)"
        data-accordion-target="#accordion-collapse-body-3"
        aria-expanded="false"
        aria-controls="accordion-collapse-body-3"
      >
        <span>Credential details</span>
        <svg
          data-accordion-icon
          class="w-6 h-6 shrink-0"
          :class="{ 'rotate-180': accordionNo === 6 }"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </button>
    </h2>
    <div
      id="accordion-collapse-body-1"
      class="border border-x-1 border-gray-200"
      :class="{ hidden: accordionNo !== 6 }"
      aria-labelledby="accordion-collapse-heading-1"
    >
      <CredentialDetails />
    </div>
    <h2 id="accordion-collapse-heading-3">
      <button
        type="button"
        class="
          flex
          justify-between
          items-center
          p-5
          w-full
          font-medium
          rounded-b-lg
          text-left text-gray-500
          border border-gray-200
          hover:bg-gray-100
        "
        @click.prevent="handleAccordion(7)"
        data-accordion-target="#accordion-collapse-body-3"
        aria-expanded="false"
        aria-controls="accordion-collapse-body-3"
      >
        <span>References</span>
        <svg
          data-accordion-icon
          class="w-6 h-6 shrink-0"
          :class="{ 'rotate-180': accordionNo === 7 }"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </button>
    </h2>
    <div
      id="accordion-collapse-body-1"
      class="border border-x-1 border-gray-200"
      :class="{ hidden: accordionNo !== 7 }"
      aria-labelledby="accordion-collapse-heading-1"
    >
      <References />
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
  data() {
    return {
      accordionNo: 1,
    };
  },
  methods: {
    handleAccordion(accordionValue) {
      if (this.accordionNo === accordionValue) {
        this.accordionNo = 0;
      } else {
        this.accordionNo = accordionValue;
      }
    },
  },
};
</script>