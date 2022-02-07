<template>

  <div>
    
    <OP @Input="validate"></OP>
    <IP :input1="input1"></IP>
    </div>
    
</template>

<script>
import IP from "../components/IP.vue"
import OP from "../components/OP.vue";
export default {
  data: () => ({
    input1: [],
  }),
components :{ OP, IP,  },
input1: "Input",
  methods: {
    validate(select, name) {
      this.input1.push({
        name: select + " : " + name,
      });
    },
  },
};
</script>

<style>

</style>