<template>
  <div
    class="fixed z-10 inset-0 overflow-y-auto"
    aria-labelledby="modal-title"
    role="dialog"
    aria-modal="true"
    v-bind:class="{ hidden: open === false, block: open === true }"
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
              <form action="post" @submit.prevent="submitAssets">
                <label
                  for="first-name"
                  class="block text-sm font-medium text-gray-500"
                  >Asset type</label
                >
                <select
                  v-model="assets.assetType"
                  class="
                    mt-1
                    block
                    w-full
                    border border-gray-300
                    rounded-md
                    shadow-sm
                    py-2
                    px-3
                    focus:outline-none focus:ring-gray-500 focus:border-gary-500
                    sm:text-sm
                  "
                >
                  <option
                    v-for="option in typeOptions"
                    :key="option.value"
                    :value="option.text"
                  >
                    {{ option.text }}
                  </option>
                </select>
                <input
                  type="text"
                  v-model="assets.assetCode"
                  class="
                    mt-4
                    block
                    w-full
                    border border-gray-300
                    rounded-md
                    shadow-sm
                    py-2
                    px-3
                    focus:outline-none focus:ring-gray-500 focus:border-gary-500
                    sm:text-sm
                  "
                  placeholder="Asset code"
                />
                <input
                  type="text"
                  v-model="assets.issueDate"
                  class="
                    mt-4
                    block
                    w-full
                    border border-gray-300
                    rounded-md
                    shadow-sm
                    py-2
                    px-3
                    focus:outline-none focus:ring-gray-500 focus:border-gary-500
                    sm:text-sm
                  "
                  onfocus="(this.type='date')"
                  onblur="if(!this.value)this.type='text'"
                  placeholder="Issue date"
                />
                <label
                  for="first-name"
                  class="block text-sm font-medium text-gray-500 mt-4"
                  >Status</label
                >
                <select
                  v-model="assets.status"
                  class="
                    mt-1
                    block
                    w-full
                    border border-gray-300
                    rounded-md
                    shadow-sm
                    py-2
                    px-3
                    focus:outline-none focus:ring-gray-500 focus:border-gary-500
                    sm:text-sm
                  "
                >
                  <option
                    v-for="option in statusOptions"
                    :key="option.value"
                    :value="option.text"
                  >
                    {{ option.text }}
                  </option>
                </select>
                <div class="mt-5 sm:mt-4 sm:flex sm:flex-row-reverse">
                  <button
                    type="submit"
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
  name: "AddMoreAssets",
  props: {
    open: Boolean,
    title: String,
  },
  data() {
    return {
      assets: {
        assetType: "",
        assetCode: "",
        issueDate: "",
        status: {
          type: Boolean,
        },
      },
      typeOptions: [
        { value: "asset1", text: "Asset one" },
        { value: "asset2", text: "Asset two" },
        { value: "asset3", text: "Asset three" },
        { value: "asset4", text: "Asset four" },
      ],
      statusOptions: [
        { value: true, text: "Active" },
        { value: false, text: "Inactive" },
      ],
    };
  },
  methods: {
    closeModal() {
      this.$emit("close");
    },
    submitAssets() {
      this.$emit("save-data", this.assets);
    },
  },
};
</script>