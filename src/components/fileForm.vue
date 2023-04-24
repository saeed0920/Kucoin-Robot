<template>
  <div>
    <form class="form grid grid-rows-4 grid-cols-2 items-center mt-10">
      <label class="custom mt-4">
        <v-file-input
          class="w-full"
          label="No file chosen"
          bg-color="#101C46"
          color="#f7f7f7f7"
          density="compact"
        ></v-file-input>
      </label>
      <input class="bg-[#35B458D9]" type="button" value="Submit" />
      <label>Export Acount:</label>
      <input class="bg-[#6825AB]" type="button" value="Export" />
      <label>Manual Import:</label>
      <input class="bg-[#2552AB]" type="button" value="Import" />
      <label>Delete Selected Items:</label>
      <input class="bg-[#AB256D]" type="button" value="Delete" />
    </form>
  </div>
</template>
