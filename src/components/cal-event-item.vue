<template>
  <div class="wrapper">
    <div class="p-1">
      <h3 class="title">{{index+1}}. {{event.title}}</h3>
    </div>
    <div class="p-1">
      <p class="time"><small>Starts: </small>{{dateTimeFormatter(Date.parse(new Date(event.date)),i18n[locale].fullFormat)}}</p>
    </div>
    <div class="p-1">
      <p class="desc">{{event.desc}}</p>
    </div>
  </div>
</template>
<script>
import i18n from '../i18n.js'
import { dateTimeFormatter } from '../tools.js'

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
    },
    locale: {
      type: String,
      required: true
    }
  },
  methods: {
    dateTimeFormatter
  }
}
</script>
