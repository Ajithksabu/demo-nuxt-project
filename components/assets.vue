<template>
  <tbody class="divide-y divide-gray-200 bg-white">
    <tr>
      <td class="whitespace-nowrap py-4 pl-4 pr-3 text-sm sm:pl-6">
        <div class="font-medium text-gray-900">{{ assetType }}</div>
      </td>
      <td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
        <div class="text-gray-900">{{ assetCode }}</div>
      </td>
      <td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
        {{ issueDate }}
      </td>
      <td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
        <span
          class="
            inline-flex
            rounded-full
            bg-green-100
            px-2
            text-xs
            font-semibold
            leading-5
            text-green-800
          "
          >{{ status }}</span
        >
      </td>
      <td
        class="
          relative
          whitespace-nowrap
          py-4
          pl-3
          pr-4
          text-right text-sm
          font-medium
          sm:pr-6
        "
      >
        <a href="#" class="text-gray-600 hover:text-indigo-900"
          >Edit<span class="sr-only">, {{ assetCode }}</span></a
        >
      </td>
    </tr>
  </tbody>
</template>
<script>
export default {
  name: "Assets",
  props: {
    assetType: String,
    assetCode: String,
    issueDate: String,
    status: String,
  },
};
</script>