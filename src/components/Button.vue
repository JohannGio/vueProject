<template>
  <button @click="onClick()" class="bg-blue-400 active:bg-blue-200 rounded-xl p-2">{{title}}</button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    title: {
      type: String,
    },
  },
  methods: {
    onClick() {
      console.log('')
    }
  }
}</script>