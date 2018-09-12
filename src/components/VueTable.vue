<template>
  <div>
    <p>Hello <strong>{{this.titleCase(name)}} (DOB: {{dob}} Age: {{calcAge}})</strong>, how are you doing today?</p>
    <button @click="sayHello()"> > Show Hello Badge < </button>
  </div>
</template>

<script>
  export default {
    props: {
      name: String,
      dob: String
    },
    methods: {
      calculateAge(dateString) {
        return ~~((Date.now() - new Date(dateString)) / 31557600000);
      },
      titleCase(str) {
        return str
          .toLowerCase()
          .split(" ")
          .map(function(word) {
            return word.charAt(0).toUpperCase() + word.slice(1);
          })
          .join(" ");
      },
      sayHello() {
        alert("Hello My Name Is " + this.name);
      }
    },
    computed: {
      calcAge() {
        return this.calculateAge(this.dob);
      }
    }
  };
</script>

<style scoped>
</style>
