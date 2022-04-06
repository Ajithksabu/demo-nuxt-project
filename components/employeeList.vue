<template>
  <div class="px-4 sm:px-6 lg:px-8">
    <div class="sm:flex sm:items-center">
      <div class="sm:flex-auto"></div>
      <div class="mt-4 sm:mt-0 sm:ml-16 sm:flex-none">
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
          @click.prevent="addEmployee"
        >
          Add employee
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
                    Name
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
                    Title
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
                    Role
                  </th>
                  <th scope="col" class="relative py-3.5 pl-3 pr-4 sm:pr-6">
                    <span class="sr-only">Edit</span>
                  </th>
                </tr>
              </thead>
              <Employee
                v-for="user in users"
                :key="user.name"
                :email="user.email"
                :name="user.name"
                :role="user.role"
                :status="user.status"
                :subtitle="user.subtitle"
                :title="user.title"
                :img="user.img"
              />
            </table>
            <Pagination />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Employee from "./employee.vue";
import Pagination from "./pagination.vue";
export default {
  name: "EmployeeList",
  components: {
    Employee,
    Pagination,
  },
  data() {
    return {
      users: [
        {
          name: "Sanjay",
          email: "sanjay@strebentechnik.com",
          title: "Frontend Developer",
          subtitle: "Optimization",
          role: "Member",
          status: "Active",
          img: "https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTZ8fGZhY2V8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60",
        },
        {
          name: "Arun",
          email: "arun@strebentechnik.com",
          title: "Frontend Developer",
          subtitle: "Optimization",
          role: "Member",
          status: "Active",
          img: "https://images.unsplash.com/photo-1544348817-5f2cf14b88c8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjV8fGZhY2V8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60",
        },
        {
          name: "Baghath",
          email: "baghath@strebentechnik.com",
          title: "Frontend Developer",
          subtitle: "Optimization",
          role: "Member",
          status: "Active",
          img: "https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MzN8fGZhY2V8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60",
        },
        {
          name: "Ajith",
          email: "ajith@strebentechnik.com",
          title: "Frontend Developer",
          subtitle: "Optimization",
          role: "Member",
          status: "Active",
          img: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8ZmFjZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60",
        },
      ],
      openDrawer: false,
    };
  },
  methods: {
    addEmployee() {
      this.$router.push("/employees");
    },
  },
};
</script>