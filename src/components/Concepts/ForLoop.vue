<template>
    <div>
        <template v-for="(item, index) in names">
            <div :key=index>{{item}}</div>

            <!--
                <div>Jake</div>
                <div>Luke</div>
                <div>Eddy</div>
                <div>Andrew</div>
                -->
        </template>
    </div>
</template>

<script>
export default {
  data: () => ({
    names:
    [
      "Jake",
      "Luke",
      "Eddy",
      "Andrew",
    ],
  }),
}
</script>