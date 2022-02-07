<template>
  <v-container>
    <v-card
      class="mx-auto"
      max-width="720"
      v-for="(item, index) in input1"
      :key="index"
      height="56"
    >
      <v-list-item-content>
        <center>
          <v-list-item-subtitle>
            {{ item.name }}
             <v-btn
         
          color="bg-danger mx-15"
          @click="deleteTodo(index)"
          >Delete
        </v-btn>
          </v-list-item-subtitle>
        </center>
        
        <br />
      </v-list-item-content>
      
    </v-card>
  </v-container>
</template>

<script>
export default {
  props: ["input1"],
  methods: {
    deleteTodo(index) {
      this.input1.splice(index, 1);
    },
  },
};
</script>

<style>
</style>
//Excel