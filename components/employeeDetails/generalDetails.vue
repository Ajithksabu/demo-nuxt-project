<template>
  <div class="grow items-center justify-center px-5">
    <form action="#" method="POST">
      <div class="shadow sm:rounded-md sm:overflow-hidden">
        <div class="bg-white py-6 px-4 space-y-6 sm:p-6">
          <!-- <h3 class="text-lg leading-6 font-medium text-gray-900">
            General Details
          </h3> -->

          <div class="grid grid-cols-4 gap-4">
            <div>
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >First name</label
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
                >Last name</label
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
                for="gender"
                class="block text-sm font-medium text-gray-700"
                >Gender</label
              >
              <select
                id="country"
                name="country"
                autocomplete="country-name"
                class="
                  mt-1
                  block
                  w-full
                  bg-white
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
              >
                <option>Select</option>
                <option>Female</option>
                <option>Male</option>
                <option>Others</option>
              </select>
            </div>
            <div>
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >Date of birth</label
              >
              <input
                type="date"
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
                for="gender"
                class="block text-sm font-medium text-gray-700"
                >Blood group</label
              >
              <select
                id="country"
                name="country"
                autocomplete="country-name"
                class="
                  mt-1
                  block
                  w-full
                  bg-white
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
              >
                <option>Select</option>
                <option>O+</option>
                <option>A+</option>
                <option>B+</option>
                <option>O-</option>
                <option>A-</option>
                <option>B-</option>
                <option>AB-</option>
                <option>AB+</option>
              </select>
            </div>
            <div>
              <label
                for="gender"
                class="block text-sm font-medium text-gray-700"
                >Martial status</label
              >
              <select
                id="country"
                name="country"
                autocomplete="country-name"
                class="
                  mt-1
                  block
                  w-full
                  bg-white
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
              >
                <option>Select</option>
                <option>Married</option>
                <option>Single</option>
              </select>
            </div>
            <div>
              <label
                for="first-name"
                class="block text-sm font-medium text-gray-700"
                >Nationality</label
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
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "GeneralDetails",
};
</script>