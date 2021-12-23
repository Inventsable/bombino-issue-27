<template>
  <div id="app">
    <Menus refresh debug />
    <Panel>
      <Button block @click="testScript">Test script</Button>
    </Panel>
  </div>
</template>

<script>
import { evalScript } from "brutalism";
export default {
  methods: {
    async testScript() {
      let result = await evalScript("testJSX()");
      console.log("RESULT:", result);
    },
  },
};
</script>