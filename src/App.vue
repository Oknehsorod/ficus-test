<template>
  <div id="app">
    <table>
      <thead>
        <tr>
          <th v-for="field in fields">{{ field }}</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="record in records">
          <td v-for="cell in record">{{ cell }}</td>
        </tr>
      </tbody>
    </table>
    <div class="action-buttons">
      <button>Download CSV</button>
      <button>Download PDF</button>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  data() {
    return {
      fields: ['Column 1', 'Column 2', 'Column 3', 'Column 4', 'Column 5'],
      records: [
        ['1.1', '1.2', '1.3', '1.4', '1.5'],
        ['2.1', '2.2', '2.3', '2.4', '2.5'],
        ['3.1', '3.2', '3.3', '3.4', '3.5'],
        ['4.1', '4.2', '4.3', '4.4', '4.5'],
        ['5.1', '5.2', '5.3', '5.4', '5.5'],
        ['6.1', '6.2', '6.3', '6.4', '6.5'],
        ['7.1', '7.2', '7.3', '7.4', '7.5'],
        ['8.1', '8.2', '8.3', '8.4', '8.5']
      ]
    };
  }
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  padding: 0 20px 0 20px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.action-buttons {
  display: flex;
  margin-top: 20px;
}
</style>
