<template>
    <div>
        <div>{{name}}</div>
        <v-text-field v-model="name" label="Jacob's Component"></v-text-field>
    </div>
</template>

<script>
export default {
  data: () => ({
    name:"Jacob"
  }),
}
</script>