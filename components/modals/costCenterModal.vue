<template>
  <div
    class="fixed z-10 inset-0 overflow-y-auto"
    aria-labelledby="modal-title"
    role="dialog"
    aria-modal="true"
    v-bind:class="{
      hidden: openCostCenterModal === false,
      block: openCostCenterModal === true,
    }"
  >
    <div
      class="
        flex
        items-end
        justify-center
        min-h-screen
        pt-4
        px-4
        pb-20
        text-center
        sm:block sm:p-0
      "
    >
      <div
        class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity"
        aria-hidden="true"
      ></div>
      <span
        class="hidden sm:inline-block sm:align-middle sm:h-screen"
        aria-hidden="true"
        >&#8203;</span
      >
      <div
        class="
          relative
          inline-block
          align-bottom
          bg-white
          rounded-lg
          px-4
          pt-5
          pb-4
          text-left
          overflow-hidden
          shadow-xl
          transform
          transition-all
          sm:my-8 sm:align-middle sm:max-w-lg sm:w-full sm:p-6
        "
      >
        <div>
          <div class="mt-3 text-center sm:mt-0 sm:ml-4 sm:text-left">
            <h3
              class="text-lg leading-6 font-medium text-gray-900"
              id="modal-title"
            >
              {{ title }}
            </h3>
            <div class="mt-4">
              <form action="post">
                <div class="grid grid-cols-3 gap-2">
                  <select
                    id="country"
                    name="country"
                    autocomplete="country-name"
                    class="
                      inline
                      bg-white
                      w-25
                      px-2
                      h-8
                      mt-8
                      mr-4
                      border border-gray-300
                      rounded-md
                      shadow-sm
                      text-sm
                      leading-4
                      font-medium
                      text-gray-700
                      hover:bg-gray-50
                      focus:outline-none
                      focus:ring-2
                      focus:ring-offset-2
                      focus:ring-gray-500
                    "
                  >
                    <option disabled selected>Division</option>
                    <option>Appraisal</option>
                    <option>Change status</option>
                    <option>Staff exit</option>
                  </select>
                  <input
                    type="text"
                    name="first-name"
                    id="first-name"
                    autocomplete="given-name"
                    class="
                      inline
                      bg-white
                      w-25
                      px-2
                      h-8
                      mt-8
                      items-center
                      self-center
                      mr-4
                      border border-gray-300
                      rounded-md
                      shadow-sm
                      text-sm
                      leading-4
                      font-medium
                      text-gray-700
                      hover:bg-gray-50
                      focus:outline-none
                      focus:ring-2
                      focus:ring-offset-2
                      focus:ring-gray-500
                    "
                    placeholder="% Allocation"
                  />
                  <button
                    type="button"
                    class="
                      inline
                      bg-white
                      w-20
                      h-6
                      mt-8
                      border border-gray-300
                      rounded-md
                      shadow-sm
                      text-sm
                      leading-4
                      font-medium
                      text-gray-700
                      hover:bg-gray-50
                      focus:outline-none
                      focus:ring-2
                      focus:ring-offset-2
                      focus:ring-gray-500
                    "
                  >
                    Add more
                  </button>
                </div>
                <div class="mt-5 sm:mt-4 sm:flex sm:flex-row-reverse">
                  <button
                    type="button"
                    class="
                      w-full
                      inline-flex
                      justify-center
                      rounded-md
                      border border-transparent
                      shadow-sm
                      px-4
                      py-2
                      bg-red-600
                      text-base
                      font-medium
                      text-white
                      hover:bg-red-700
                      focus:outline-none
                      focus:ring-2
                      focus:ring-offset-2
                      focus:ring-red-500
                      sm:ml-3 sm:w-auto sm:text-sm
                    "
                  >
                    Save
                  </button>
                  <button
                    type="button"
                    class="
                      mt-3
                      w-full
                      inline-flex
                      justify-center
                      rounded-md
                      border border-gray-300
                      shadow-sm
                      px-4
                      py-2
                      bg-white
                      text-base
                      font-medium
                      text-gray-700
                      hover:bg-gray-50
                      focus:outline-none
                      focus:ring-2
                      focus:ring-offset-2
                      focus:ring-indigo-500
                      sm:mt-0 sm:w-auto sm:text-sm
                    "
                    @click.prevent="closeModal"
                  >
                    Cancel
                  </button>
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CostCenterModal",
  props: {
    openCostCenterModal: Boolean,
    title: String,
  },
  methods: {
    closeModal() {
      this.$emit("close-cost-center-modal");
    },
  },
};
</script>