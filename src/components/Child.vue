<template>
    <div>
        <input type="text" v-model="client.name" placeholder="Name">
        <input type="number" v-model="client.age" placeholder="Age">
        <div class="box">
            <strong>Child.vue</strong>
            <pre v-html="client"></pre>
        </div>
    </div>
</template>

<script>
  export default {
    name: 'Child',
    props: {
      client: {
        required: true,
        type: Object,
        default: () => ({})
      }
    }
  }
</script>
