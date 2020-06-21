<template>
  <i :class="type"></i>
</template>

<script>
  let availableName = [
    'sr-share',
    'sr-settings',
    'sr-like',
    'sr-filter'
  ]

  export default {
    name: "icon",
    data: function () {
      return {
      }
    },
    props: {
      type: {
        type: String,
        required: true,
      },
    },
    created() {
      if (!availableName.includes(this.type)) {
        throw new Error("Icon "+ this.type + " not found in securating-icons.otf")
      }
    },
  }
</script>

<style scoped>
  @font-face {
    font-family: 'securating-icons';
    src: url("../assets/fonts/securating-icons.otf") format('opentype');
    font-weight: normal;
    font-style: normal;
    font-display: block;
  }

  i {
    font-family: securating-icons, sans-serif !important;
    font-style: normal;
    font-weight: normal;
    font-variant: normal;
  }

  .sr-like:before {
    content: "\6c";
  }

  .sr-filter:before {
    content: "\66";
  }

  .sr-share:before {
    content: "\73";
  }

  .sr-settings:before {
    content: "\74";
  }
</style>
