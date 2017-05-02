<template>
  <div class="wrapper">
    <div class="p-1">
      <h3 class="title">{{index+1}}. {{event.title}}</h3>
    </div>
    <div class="p-1">
      <p class="time">{{ Date.parse(new Date(event.date)) }}</p>
    </div>
    <div class="p-1">
      <p class="desc">{{event.desc}}</p>
    </div>
  </div>
</template>
<script>

export default {
  data () {
    return {
      i18n
    }
  },
  props: {
    event: {
      type: Object,
      required: true
    },
    index: {
      type: Number,
      required: true
    }
  }
}
</script>
