<template>
  <div id="app">
    <div class="container">
      <div class="jumbotron">
        <h2 class="text-center">Sr Icon Component</h2>
      </div>

      <table class="table table-borderless">
        <thead>
        <tr>
          <th>Name</th>
          <th>Class</th>
          <th>Result</th>
        </tr>
        </thead>
        <tbody>
        <tr>
          <td>sr-share</td>
          <td>none</td>
          <td>
            <sr-icon name="sr-share"/>
          </td>
        </tr>
        <tr>
          <td>sr-filter</td>
          <td>sr-red-color</td>
          <td>
            <sr-icon name="sr-filter" class="sr-red-color"/>
          </td>
        </tr>
        <tr>
          <td>sr-settings</td>
          <td>sr-green-color</td>
          <td>
            <sr-icon name="sr-settings" class="sr-green-color"/>
          </td>
        </tr>
        <tr>
          <td>sr-like</td>
          <td>sr-blue-color</td>
          <td>
            <sr-icon name="sr-like" class="sr-blue-color" @error="showErrorMessage($event)"/>
          </td>
        </tr>
        <tr>
          <td>sr-home</td>
          <td>sr-blue-color</td>
          <td>
            <sr-icon name="sr-home" class="sr-blue-color" @error="showErrorMessage($event)"/>
          </td>
        </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
  import SrIcon from "./components/SrIcon";

  export default {
    name: "App",
    components: {
      SrIcon
    },
    methods: {
      showErrorMessage(event) {
        alert(event)
      }
    }
  };
</script>

<style>

</style>
