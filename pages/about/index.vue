<template>
  <!-- This example requires Tailwind CSS v2.0+ -->
  <div class="bg-white">
    <Sidebar />
    <div class="max-w-7xl mx-auto py-16 px-4 sm:py-24 sm:px-6 lg:px-8">
      <div class="text-center">
        <p
          class="
            mt-1
            text-xl
            font-extrabold
            text-gray-900
            sm:text-3xl sm:tracking-tight
            lg:text-4xl
          "
        >
          ABOUT THE CSS GROUP
        </p>
        <p class="max-w-xl text-left mt-5 mx-auto text-l text-gray-500">
          The Consolidated Shipping Services (CSS) Group is a global leader in
          international transport & logistics. Constantly adapting to its
          customers’ changing needs, the company has enriched its expertise to
          become a tier-one logistics and freight forwarding partner in the GCC,
          with integrated logistic networks in Africa, Middle East, Europe and
          the Americas. The Group delivers value to offering fast, quality, and
          delivery services via a network of partners. Consolidated Shipping
          Services Group’s scalable, direct-service technology platforms through
          its team of skilled salespeople support network operations, designed
          to optimize delivery efficiency and effectiveness.
        </p>
      </div>
    </div>
  </div>
</template>
<script>
import Sidebar from "../../components/sidebar.vue";
export default {
  components: {
    Sidebar,
  },
};
</script>