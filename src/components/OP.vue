<template>

  <div class="container">
    <v-contaoner>
      <h1>เพิ่มหัวข้อ/การบ้าน</h1>
      <v-select
        v-model="select"
        :items="items"
        label="หัวข้อ"
        solo
      ></v-select>
      <v-text-field v-model="name" label="รายการ" outlined></v-text-field>
      <v-btn color="success" class="mr-4" @click="validate()">เพิ่ม</v-btn>
      <v-contaoner class="">
        <h1>รายวิชาที่เพิ่ม</h1>
       
      </v-contaoner>
    </v-contaoner>
  </div>
</template>


<script>
export default {
  subject: "",
  work: "",
  data() {
    return {
      select:null,
      name:"",
      items: ["วิชา SE", " วิชา Web", "อื่นๆ"],
      selectedItem: 1,
      additems: [
        { text: "วิชา SE ออกแบบ Diagram" },
        { text: "วิชา SE ออกแบบ" },
        { text: "วิชา Web ออกแบบ UI" },
        { text: "วิชา Web Assignment1000" },
      ],
    };
  },
  props: ["input1"],
  methods: {
    validate() {
      this.$emit("Input", this.select, this.name);
       (this.select = ""), (this.name = "");
    },
  },
};
</script>

<style>
</style>
//รับข้อมูล