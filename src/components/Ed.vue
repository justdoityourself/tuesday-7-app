<template>
    <div>
        <div>{{name}}</div>
        <v-text-field v-model="name" label="Ed's Component"></v-text-field>
    </div>
</template>

<script>
export default {
  data: () => ({
    name:"Ed"
  }),
}
</script>