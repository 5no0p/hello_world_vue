<script setup>
import './style.css';
import { ref } from 'vue';

//data
const name = ref('Rachel');
const href = ref('https://www.scrimba.com');
const disabled = ref(true);
const attributes = {
  id: 'big_emoji',
  class: 'waving',
};
const coding_years = ref(5);
const getFormattedDate = (date) => {
  const options = { year: 'numeric', month: 'long', day: 'numeric' };
  return date.toLocaleDateString('en-UK', options);
};
const username = ref('rachelktyjohnson');
const event = ref('dblclick');
const blockLeave = () => {
  alert("You can't leave!");
};
</script>

<template>
  <span v-bind="attributes">👋🏻</span>
  <!--
  CHALLENGE: Bind the anchor tag's href attribute to the Scrimba profile of the username variable
  SYNTAX: v-bind:[attribute]="expression"
  SCRIMBA PROFILE URL: https://scrimba.com/@[username]
  -->
  <h1>Hi, my name is 
    <a :href="href + '/@' + username" target="_blank">{{ name }}</a>
  </h1>
  <a :href target="_blank">
    <button :disabled>Click to visit my favourite website! If you can...</button>
  </a>
  <h2 v-on:[event]="coding_years++">
    {{
        coding_years > 0
          ? `I have been coding for ${coding_years} years`
          : "I am a newbie!"
    }}
  </h2>
  <h3>Today is {{ getFormattedDate(new Date()) }}</h3>
</template>
