<!-- Using tailwind -->
<template>
  <header class="text-2xl flex-row flex items-center justify-between">
    <h1>{{title}}</h1>
    <Button title="Click"/>
  </header>
</template>


<script>
import Button from './Button'

  export default {
    name: 'Header',
    props: {
      title: {
        type: String,
        default: 'Hello'
      },
    },
    components: {
      Button
    }
  }
</script>
