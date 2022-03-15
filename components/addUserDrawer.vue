<template>
  <div
    class="
      hidden
      z-10
      md:flex md:w-80 md:flex-col md:fixed md:inset-y-0 md:right-0
    "
  >
    <!-- Sidebar component, swap this element with another sidebar if you like -->
    <div class="flex-1 flex flex-col min-h-0 bg-gray-800">
      <button
        @click.prevent="handleDrawer"
        class="text-white flex justify-end mr-3 mt-3"
      >
        ❌
      </button>
      <p class="text-center text-white text-lg mb-5 font-bold">Add User</p>
      <form action="" class="mt-6" method="post" @submit.prevent="onSubmit">
        <div class="sm:col-span-4 mb-4">
          <label for="name" class="block mx-3 text-sm font-medium text-white">
            Name
          </label>
          <div class="mt-1 mx-3 flex rounded-md shadow-sm">
            <input
              type="text"
              v-model="name"
              autocomplete="Name"
              class="
                flex-1
                focus:ring-indigo-500 focus:border-indigo-500
                block
                w-full
                min-w-0
                sm:text-sm
                border-gray-300
                rounded-lg
                h-7
              "
            />
          </div>
        </div>
        <div class="sm:col-span-4 mb-4">
          <label for="email" class="block mx-3 text-sm font-medium text-white">
            Email
          </label>
          <div class="mt-1 mx-3 flex rounded-md shadow-sm">
            <input
              type="text"
              v-model="email"
              autocomplete="Email"
              class="
                flex-1
                focus:ring-indigo-500 focus:border-indigo-500
                block
                w-full
                min-w-0
                sm:text-sm
                border-gray-300
                rounded-lg
                h-7
              "
            />
          </div>
        </div>
        <div class="sm:col-span-4 mb-4">
          <label for="title" class="block mx-3 text-sm font-medium text-white">
            Title
          </label>
          <div class="mt-1 mx-3 flex rounded-md shadow-sm">
            <input
              type="text"
              v-model="title"
              autocomplete="Title"
              class="
                flex-1
                focus:ring-indigo-500 focus:border-indigo-500
                block
                w-full
                min-w-0
                sm:text-sm
                border-gray-300
                rounded-lg
                h-7
              "
            />
          </div>
        </div>
        <div class="sm:col-span-4 mb-4">
          <label
            for="subtitle"
            class="block mx-3 text-sm font-medium text-white"
          >
            Sub Title
          </label>
          <div class="mt-1 mx-3 flex rounded-md shadow-sm">
            <input
              type="text"
              v-model="subtitle"
              autocomplete="Sub Title"
              class="
                flex-1
                focus:ring-indigo-500 focus:border-indigo-500
                block
                w-full
                min-w-0
                sm:text-sm
                border-gray-300
                rounded-lg
                h-7
              "
            />
          </div>
        </div>
        <div class="sm:col-span-4 mb-4">
          <label for="status" class="block mx-3 text-sm font-medium text-white">
            Status
          </label>
          <div class="mt-1 mx-3 flex rounded-md shadow-sm">
            <input
              type="text"
              v-model="status"
              autocomplete="Status"
              class="
                flex-1
                focus:ring-indigo-500 focus:border-indigo-500
                block
                w-full
                min-w-0
                sm:text-sm
                border-gray-300
                rounded-lg
                h-7
              "
            />
          </div>
        </div>
        <div class="sm:col-span-4 mb-4">
          <label for="role" class="block mx-3 text-sm font-medium text-white">
            Role
          </label>
          <div class="mt-1 mx-3 flex rounded-md shadow-sm">
            <input
              type="text"
              v-model="role"
              autocomplete="Role"
              class="
                flex-1
                focus:ring-indigo-500 focus:border-indigo-500
                block
                w-full
                min-w-0
                sm:text-sm
                border-gray-300
                rounded-lg
                h-7
              "
            />
          </div>
        </div>
        <div class="sm:col-span-4 mb-4">
          <label for="img" class="block mx-3 text-sm font-medium text-white">
            Image Link
          </label>
          <div class="mt-1 mx-3 flex rounded-md shadow-sm">
            <input
              type="text"
              v-model="img"
              autocomplete="Image Link"
              class="
                flex-1
                focus:ring-indigo-500 focus:border-indigo-500
                block
                w-full
                min-w-0
                sm:text-sm
                border-gray-300
                rounded-lg
                h-7
              "
            />
          </div>
        </div>
        <button
          class="
            block
            text-center text-white
            bg-gray-800
            p-3
            duration-300
            rounded-sm
            hover:bg-black
            w-full
          "
        >
          Submit
        </button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "AddUserDrawer",
  data() {
    return {
      name: null,
      email: null,
      title: null,
      subtitle: null,
      status: null,
      role: null,
      img: null,
    };
  },
  methods: {
    handleDrawer() {
      this.$emit("close-drawer");
    },
    onSubmit(e) {
      this.$emit("add-user", {
        name: this.name,
        email: this.email,
        title: this.title,
        subtitle: this.subtitle,
        status: this.status,
        role: this.role,
        img: this.img,
      });
      this.$emit("close-drawer");
    },
  },
};
</script>