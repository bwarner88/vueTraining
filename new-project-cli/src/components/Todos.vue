<template>
  <v-container fluid style="width:50%;">
    <v-textarea label="Text" 
                value="Enter Item Here" 
                style="height:50px;margin-bottom:25px;"
                v-model="inputVal"
                ></v-textarea>
    
    <div class="my-2">
      <v-btn color="error" 
             dark 
             large 
             style="margin-left:40%;margin-top:70px;"
             @click="addTodo"
             >Submit</v-btn>
    </div>

    <v-card
    class="mx-auto"
    max-width="344"
    outlined
    v-for="(todo, i) in todoArray" v-bind:key="i"
   
  >

    <v-list-item three-line  >
      <v-list-item-content>
        <div class="overline mb-4">Item# {{ i }}</div>
        <v-list-item-title class="headline mb-1">{{ todo }}</v-list-item-title>
      </v-list-item-content>
    </v-list-item>

    <v-card-actions>
      <v-btn text>Completed</v-btn>
      <v-btn text>Delete</v-btn>
    </v-card-actions>
  </v-card>
  </v-container>

  
</template>

<script>
export default {
    data () {
        return {
            todoArray: [],
            inputVal: null,
        }
    },
    methods: {
        addTodo() {
            this.todoArray.push(this.inputVal);
        }
    }
}
</script>