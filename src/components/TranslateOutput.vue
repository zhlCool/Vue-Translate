<template>
  <div id="translateOutput" style="font-size:30px;color:#0EBC58;">
      <h2>{{translatedText}}</h2>
  </div>
</template>
<script>
export default {
  name: 'translateOutput',
  props:[
      "translatedText"
  ]
}
</script>

<style>
</style>
