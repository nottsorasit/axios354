<template >
  <div class="contrainer">
      <div class="navbar"> <h1 align="center">jsonplaceholder</h1></div>
    <div class="row">
      <div class="col" v-for="item in httpdata" :key="item">
          <br>
        <b-card style="width:200px;" >
          userId = {{ item.userId }}<br>
          id = {{ item.id }}<br>
          title = "{{ item.title }}" <br>
          completed = {{item.completed}}
        </b-card>
        
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return { httpdata: "" };
  },
  mounted() {
    axios({
      method: "GET",
      url: "http://jsonplaceholder.typicode.com/todos",
    }).then((result) => {
      this.httpdata = result.data;
    });
  },
};
</script>

 <style>
 .col{
     background-color: rgba(123, 253, 90, 0.685);
     
 }
 .navbar{
     background-color: rgba(16, 223, 50, 0.973);
     color: seashell;

 }
 

</style>