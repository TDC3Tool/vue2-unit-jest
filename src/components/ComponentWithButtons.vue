<!--
 * @Author       : ADI
 * @Date         : 2021-04-24 12:28:13
 * @LastEditors  : ADI
 * @LastEditTime : 2021-04-24 12:28:33
-->
<template>
  <div>
    <button class="commit" @click="handleCommit">Commit</button>

    <button class="dispatch" @click="handleDispatch">Dispatch</button>

    <button class="namespaced-dispatch" @click="handleNamespacedDispatch">
      Namespaced Dispatch
    </button>
  </div>
</template>

<script>
export default {
  name: "ComponentWithButtons",

  methods: {
    handleCommit() {
      this.$store.commit("testMutation", { msg: "Test Commit" });
    },

    handleDispatch() {
      this.$store.dispatch("testAction", { msg: "Test Dispatch" });
    },

    handleNamespacedDispatch() {
      this.$store.dispatch("namespaced/very/deeply/testAction", {
        msg: "Test Namespaced Dispatch",
      });
    },
  },
};
</script>
