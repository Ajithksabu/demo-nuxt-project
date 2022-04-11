<template>
  <div class="px-4 my-4 md:px-8">
    <div class="md:flex md:items-center">
      <div class="md:flex-auto"></div>
      <div class="mt-4 md:mt-0 md:ml-16 md:flex-none">
        <button
          type="button"
          class="
            inline-flex
            items-center
            justify-center
            rounded-md
            border border-transparent
            bg-gray-700
            px-4
            py-2
            text-sm
            font-medium
            text-white
            shadow-sm
            hover:bg-gray-400
            focus:outline-none
            focus:ring-2
            focus:ring-gray-700
            focus:ring-offset-2
            sm:w-auto
          "
          @click.prevent="openAssetsModal"
        >
          Add more
        </button>
      </div>
    </div>
    <div class="relative w-full text-gray-400 focus-within:text-gray-600">
      <div class="absolute inset-y-0 flex items-center pointer-events-none">
        <svg
          class="h-5 w-5 ml-2"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 20 20"
          fill="currentColor"
          aria-hidden="true"
        >
          <path
            fill-rule="evenodd"
            d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
            clip-rule="evenodd"
          />
        </svg>
      </div>
      <input
        id="search-field"
        class="
          block
          w-72
          border-2
          h-full
          rounded-lg
          px-10
          py-2
          border-gray-200
          text-gray-900
          placeholder-gray-500
          focus:outline-none focus:placeholder-gray-400
          sm:text-sm
        "
        placeholder="Search..."
        type="search"
        name="search"
      />
    </div>
    <div class="mt-8 flex flex-col">
      <div class="-my-2 -mx-4 overflow-x-auto sm:-mx-6 lg:-mx-8">
        <div class="inline-block min-w-full py-2 align-middle md:px-6 lg:px-8">
          <div
            class="
              overflow-hidden
              shadow
              ring-1 ring-black ring-opacity-5
              md:rounded-lg
            "
          >
            <table class="min-w-full divide-y divide-gray-300">
              <thead class="bg-gray-50">
                <tr>
                  <th
                    scope="col"
                    class="
                      py-3.5
                      pl-4
                      pr-3
                      text-left text-sm
                      font-semibold
                      text-gray-900
                      sm:pl-6
                    "
                  >
                    Asset type
                  </th>
                  <th
                    scope="col"
                    class="
                      px-3
                      py-3.5
                      text-left text-sm
                      font-semibold
                      text-gray-900
                    "
                  >
                    Asset code
                  </th>
                  <th
                    scope="col"
                    class="
                      px-3
                      py-3.5
                      text-left text-sm
                      font-semibold
                      text-gray-900
                    "
                  >
                    Issue date
                  </th>
                  <th
                    scope="col"
                    class="
                      px-3
                      py-3.5
                      text-left text-sm
                      font-semibold
                      text-gray-900
                    "
                  >
                    Status
                  </th>
                  <th scope="col" class="relative py-3.5 pl-3 pr-4 sm:pr-6">
                    <span class="sr-only">Edit</span>
                  </th>
                </tr>
              </thead>
              <Assets
                v-for="asset in assets"
                :key="asset.assetCode"
                :assetType="asset.assetType"
                :assetCode="asset.assetCode"
                :issueDate="asset.issueDate"
                :status="asset.status"
              />
            </table>
            <Pagination />
          </div>
        </div>
      </div>
    </div>
    <AddMoreAssets
      :open="openModal"
      title="Add assets"
      v-on:close="close"
      @save-data="saveToList"
    />
  </div>
</template>
<script>
import Assets from "./assets.vue";
import Pagination from "./pagination.vue";
import AddMoreAssets from "../components/modals/addMoreAssets.vue";
export default {
  name: "AssetsList",
  components: {
    Assets,
    Pagination,
    AddMoreAssets,
  },
  data() {
    return {
      assets: [
        {
          assetType: "Asset one",
          assetCode: "AS001",
          issueDate: "12-04-2022",
          status: "Active",
        },
        {
          assetType: "Asset two",
          assetCode: "AS002",
          issueDate: "13-04-2022",
          status: "Active",
        },
        {
          assetType: "Asset three",
          assetCode: "AS003",
          issueDate: "14-04-2022",
          status: "Active",
        },
        {
          assetType: "Asset four",
          assetCode: "AS004",
          issueDate: "15-04-2022",
          status: "Active",
        },
      ],
      openModal: false,
    };
  },
  methods: {
    openAssetsModal() {
      this.openModal = true;
    },
    close() {
      this.openModal = false;
    },
    saveToList(e) {
      this.assets.push(e);
      this.openModal = false;
    },
  },
};
</script>