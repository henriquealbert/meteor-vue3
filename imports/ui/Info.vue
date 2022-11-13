<script setup>
import { autorun } from 'vue-meteor-tracker'
import { LinksCollection } from '/imports/api/links'

const links = autorun(() => LinksCollection.find({}).fetch()).result
</script>

<template>
  <h2>Learn Meteor!</h2>
  <ul>
    <li v-for="link of links" :key="link._id">
      <a :href="link.url" target="_blank">{{ link.title }}</a>
    </li>
  </ul>
</template>
