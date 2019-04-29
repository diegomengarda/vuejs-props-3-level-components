<template>
    <div>
        <Child :client="client"></Child>
        <div class="box">
            <strong>Parent.vue</strong>
            <pre v-html="client"></pre>
        </div>
    </div>
</template>

<script>
  import Child from './Child'
  export default {
    name: 'HelloWorld',
    components: {
      Child
    },
    props: {
      client: {
        required: true,
        type: Object,
        default: () => ({})
      }
    }
  }
</script>
