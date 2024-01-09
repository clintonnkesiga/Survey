<template>
  <div class="flex min-h-full flex-1 flex-col justify-center px-6 py-12 lg:px-8">
    <router-view></router-view>
  </div>
</template>

<script>

import {LockClosedIcon} from "@heroicons/vue/16/solid/index.js";

export default {
  components: {
    LockClosedIcon,
  },
}
</script>
