<template>
    <div>
        <div>{{name}}</div>
        <v-text-field v-model="name" label="Andrew's Component"></v-text-field>
    </div>
</template>

<script>
export default {
  data: () => ({
    name:"Andrew"
  }),
}
</script>