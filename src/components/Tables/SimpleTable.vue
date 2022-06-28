<template>
  <div>
    <md-table v-model="users" :table-header-color="tableHeaderColor">
      <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="Author-name">{{ item.author_name }}</md-table-cell>
        <md-table-cell md-label="Research-name">{{ item.researchName }}</md-table-cell>
        <md-table-cell md-label="Institute">{{ item.institute }}</md-table-cell>
        <md-table-cell md-label="Details"><md-button>view</md-button></md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "simple-table",
  props: {
    tableHeaderColor: {
      type: String,
      default: ""
    }
  },
  data() {
    return {
      selected: [],
      users: [
        {
          author_name: "Mr Rice",
          researchName: "Transport",
          institute: "CUT",
          details: ""
        },
        {
          author_name: "Mrs Hooper",
          researchName: "Water",
          institute: "Curaçao",
          details: ""
        },
        {
          author_name: "Sage Rodriguez",
          researchName: "KIJ",
          institute: "Netherlands",
          details: ""
        },
        {
          author_name: "Philip Chaney",
          researchName: "CDF",
          institute: "Korea, South",
          details: ""
        },
        {
          author_name: "Doris Greene",
          researchName: "ABC",
          institute: "Malawi",
          details: ""
        },
        {
          author_name: "Mason Porter",
          researchName: "XYZ",
          institute: "Chile",
          details: ""
        }
      ]
    };
  }
};
</script>
