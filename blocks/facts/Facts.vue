<template>
  <h5>Some Interesting Sushi Factss :</h5>
  <h6 v-for="fact in facts">{{ fact }}</h6>
</template>
<script>
import { toRefs } from "vue";
export default {
  name: "Facts",
  props: {
    factProp: Object,
  },
  setup(props) {
    const { factProp } = toRefs(props);
    return { facts: factProp.value.facts };
  },
};
</script>
