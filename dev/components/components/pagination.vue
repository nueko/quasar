<template>
  <div>
    <div class="layout-padding">
      <div class="label bg-secondary text-white">
        Model <span class="right-detail"><em>{{page}}</em></span>
      </div>

      <p class="caption">
        You can also
        <span class="desktop-only">click</span>
        <span class="mobile-only">tap</span>
        on the Input box and type out another page number
        then hit &lt;ENTER&gt;
      </p>

      <q-pagination @change="onChange" @input="onInput" v-model="page" :max="17"></q-pagination>

      <p class="caption">Disabled State</p>
      <q-pagination v-model="page" :max="17" disable></q-pagination>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      page: 1
    }
  },
  methods: {
    onChange (val) {
      console.log('@change', JSON.stringify(val))
    },
    onInput (val) {
      console.log('@input', JSON.stringify(val))
    }
  }
}
</script>
