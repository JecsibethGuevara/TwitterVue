<template>
  <ButtonStd buttonText="hi"> </ButtonStd>
</template>

<script>
import ButtonStd from "src/components/ButtonStd.vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
  components: { ButtonStd },
});
</script>
