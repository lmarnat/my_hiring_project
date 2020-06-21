<template>
  <div>
    <icon :type="name"></icon>
  </div>

</template>

<script>
  import Icon from "./Icon";

  export default {
    name: "sr-icon",
    components: {
      Icon
    },
    data: function () {
      return {
        error: null,
      }
    },
    props: {
      capture: {
        default: false,
        type: Boolean
      },
      name: {
        type: String,
        required: true,
      },
    },
    methods: {
    },
    errorCaptured(error) {
      this.error = error;
      this.$emit('error', error);
    },
  }
</script>


<style scoped>
  .sr-red-color {
    color: red;
  }

  .sr-green-color {
    color: green;
  }

  .sr-blue-color {
    color: blue;
  }

  .sr-default-color {
    color: black;
  }

</style>

