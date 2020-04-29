<template>

    <div>
      
      <!--<p>Luke's</p>-->
      <!--<h3>Luke's</h3>-->
       <div class=gvt style='--gg:4px;--gr:1fr 1fr 1fr;--gc:1fr 1fr 1fr;width:180px;height:180px;background:black;'>
          <template v-for="(item, index) in board">
            <div v-if='item.x' :key=index class=gvt style='--gr:1fr;--gc:1fr;background:darkred ;'>X</div>
            <div v-else-if='item.o' :key=index class=gvt style='--gr:1fr;--gc:1fr;background:darkgreen;'>O</div>
            <div @click=turn(item) v-else :key=index class=gvt style='--gr:1fr;--gc:1fr;background:lightgrey;'>?</div>
          </template>
        </div>

        <div>{{name}}</div>
        <v-text-field v-model="name" label="Luke's Component"></v-text-field>
    </div>

</template>

<script>
export default {
  data: () => ({
    name:"Luke",
     board:
    [
      {o:false,x:false},{o:false,x:false},{o:false,x:false},
      {o:false,x:false},{o:false,x:false},{o:false,x:false},
      {o:false,x:false},{o:false,x:false},{o:false,x:false},
    ],
    x_or_o_turn:0,
    turn(item)
    {
      if(this.x_or_o_turn++ % 2)
        item.o = true;
      else
        item.x = true;
    }
  }),
}
</script>