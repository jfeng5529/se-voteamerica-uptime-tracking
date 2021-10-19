<template>
  <div>
    <md-table v-model="services" md-sort="name" md-sort-order="asc" md-card>
      <md-table-toolbar>
        <h1 class="md-title">Services</h1>
      </md-table-toolbar>

      <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="Description" md-sort-by="description">{{
          item.description
        }}</md-table-cell>
        <md-table-cell md-label="Status" md-sort-by="status">{{
          item.status
        }}</md-table-cell>
        <md-table-cell md-label="Status Changed At" md-sort-by="statusChangedAt">{{
          item.statusChangedAt
        }}</md-table-cell>
        <md-table-cell md-label="Uptime Day" md-sort-by="uptimeDay">{{
          item.uptimeDay
        }}</md-table-cell>
        <md-table-cell md-label="Uptime Week" md-sort-by="upTimeWeek">{{
          item.upTimeWeek
        }}</md-table-cell>
        <md-table-cell md-label="Uptime Month" md-sort-by="uptimeMonth">{{
          item.uptimeMonth
        }}</md-table-cell>
        <md-table-cell md-label="Uptime Quarter" md-sort-by="upTimeQuarter">{{
          item.upTimeQuarter
        }}</md-table-cell>
        <md-table-cell md-label="Links" md-sort-by="links">{{
          item.links
        }}</md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>
<script>
export default {
  name: "HomeTable",
  data() {
    return {
        services:[{
          id: 1,
          description: 'VT Polling Place Lookup, Voter Registration Status Verifier, Absentee Ballot Request, and Absentee Ballot Tracker',
          status: 'up',
          statusChangedAt: '06/10/2021 2:39 a.m.',
          uptimeDay: '99.00%',
          upTimeWeek: '100.00%',
          uptimeMonth: '100.00%',
          upTimeQuarter: '100.00%',
          links: "links"
        },
        {
          id: 2,
          description: 'IN Absentee Ballot Request',
          status: 'up',
          statusChangedAt: '06/20/2021 12:27 a.m.',
          uptimeDay: '100.00%',
          upTimeWeek: '100.00%',
          uptimeMonth: '100.00%',
          upTimeQuarter: '100.00%',
          links: "links"
        },
        {
          id: 3,
          description: 'IN Polling Place Lookup, Online Voter Registration, Voter Registration Status Verifier, and Absentee Ballot Tracker',
          status: 'up',
          statusChangedAt: '07/02/2021 5:46 a.m.',
          uptimeDay: '100.00%',
          upTimeWeek: '100.00%',
          uptimeMonth: '100.00%',
          upTimeQuarter: '100.00%',
          links: "links"
        },]
    };
  },
  async mounted() {
    //   const serviceInfo = await fetch("http://uptime.voteamerica.com/v1/uptime/proxies/");
    //   this.services = serviceInfo.results;
  },
};
</script>