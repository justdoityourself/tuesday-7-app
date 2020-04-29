<template>
    <div>
        <div class=gvt style='--gg:4px;--gr:1fr 1fr 1fr;--gc:1fr 1fr 1fr;width:180px;height:180px;background:lightgrey;'>
          <template v-for="(item, index) in board">
            <div v-if='item.x' :key=index class=gvt style='--gr:1fr;--gc:1fr;background:blue;'>X</div>
            <div v-else-if='item.o' :key=index class=gvt style='--gr:1fr;--gc:1fr;background:green;'>O</div>
            <div @click=turn(item) v-else :key=index class=gvt style='--gr:1fr;--gc:1fr;background:red;'>?</div>
          </template>
        </div>

        <div>{{name}}</div>
        <v-text-field v-model="name" label="Jacob's Component"></v-text-field>
    </div>
</template>


<script>
export default {
  data: () => ({
    name:"Jacob",
    board:
    [
      {o:false,x:false},{o:false,x:false},{o:false,x:false},
      {o:false,x:false},{o:false,x:false},{o:false,x:false},
      {o:false,x:false},{o:false,x:false},{o:false,x:false}
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