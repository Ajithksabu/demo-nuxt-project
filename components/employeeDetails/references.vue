<template>
  <div class="grow items-center justify-center px-5">
    <form action="#" method="POST">
      <div>
        <div class="bg-white py-6 px-4 space-y-6 sm:p-6">
          <!-- <h3 class="text-lg leading-6 font-medium text-gray-900">
            Contact Details
          </h3> -->

          <div class="grid grid-cols-5 gap-4">
            <div>
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >Name</label
              >
              <input
                type="text"
                name="first-name"
                id="first-name"
                autocomplete="given-name"
                class="
                  mt-1
                  block
                  w-full
                  border border-gray-300
                  rounded-md
                  shadow-sm
                  py-2
                  px-3
                  focus:outline-none
                  focus:ring-indigo-500
                  focus:border-indigo-500
                  sm:text-sm
                "
              />
            </div>
            <div>
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >Reference type</label
              >
              <input
                type="text"
                name="first-name"
                id="first-name"
                autocomplete="given-name"
                class="
                  mt-1
                  block
                  w-full
                  border border-gray-300
                  rounded-md
                  shadow-sm
                  py-2
                  px-3
                  focus:outline-none
                  focus:ring-indigo-500
                  focus:border-indigo-500
                  sm:text-sm
                "
              />
            </div>
            <div>
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >Contact No.</label
              >
              <input
                type="email"
                name="first-name"
                id="first-name"
                autocomplete="given-name"
                class="
                  mt-1
                  block
                  w-full
                  border border-gray-300
                  rounded-md
                  shadow-sm
                  py-2
                  px-3
                  focus:outline-none
                  focus:ring-indigo-500
                  focus:border-indigo-500
                  sm:text-sm
                "
              />
            </div>
            <div>
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >Email</label
              >
              <input
                type="email"
                name="first-name"
                id="first-name"
                autocomplete="given-name"
                class="
                  mt-1
                  block
                  w-full
                  border border-gray-300
                  rounded-md
                  shadow-sm
                  py-2
                  px-3
                  focus:outline-none
                  focus:ring-indigo-500
                  focus:border-indigo-500
                  sm:text-sm
                "
              />
            </div>
            <div>
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
          </div>
        </div>
        <div class="pt-5 mb-4">
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
    </form>
  </div>
</template>

<script>
export default {
  name: "References",
};
</script>