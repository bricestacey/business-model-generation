<template>
  <div class="h-screen p-10">
    <div class="shadow-lg  bg-white flex flex-col h-full border-2 border-grey-500">
      <div class="flex min-h-3/4">
        <div id="partners" class="flex-1 border-r-4 border-green-500 flex flex-col">
          <div :class="headingClass">Key Partners</div>
          <textarea :class="fooClass" v-model="partners"></textarea>
        </div>
        <div class="flex-1 flex flex-col">
          <div id="activities" class="flex-1 flex flex-col border-b-4 border-green-500">
            <div :class="headingClass">Key Activities</div>
          <textarea :class="fooClass" v-model="activities"></textarea>
          </div>
          <div id="resources" class="flex-1 flex flex-col">
            <div :class="headingClass">Key Resources</div>
          <textarea :class="fooClass" v-model="resources"></textarea>
          </div>
        </div>
        <div id="propositions" class="flex-1 border-l-4 border-yellow-500 flex flex-col">
          <div :class="headingClass">Value Propositions</div>
          <textarea :class="fooClass" v-model="propositions"></textarea>
        </div>
        <div class="flex flex-col flex-1 border-l-4 border-blue-500">
          <div id="relationships" class="flex flex-col flex-1 border-b-4 border-blue-500">
            <div :class="headingClass">Customer Relationships</div>
          <textarea :class="fooClass" v-model="relationships"></textarea>
          </div>
          <div id="channels" class="flex flex-col flex-1">
            <div :class="headingClass">Channels</div>
          <textarea :class="fooClass" v-model="channels"></textarea>
          </div>
        </div>
        <div id="segments" class="flex flex-col flex-1 border-l-4 border-black">
          <div :class="headingClass">Customer Segments</div>
          <textarea :class="fooClass" v-model="segments"></textarea>
        </div>
      </div>

      <div class="flex flex-1 min-h-1/4">
        <div id="cost" class="flex-1 border-t-4 border-yellow-500 flex flex-col">
          <div :class="headingClass">Cost Structure</div>
          <textarea :class="fooClass" v-model="cost"></textarea>
        </div>
        <div id="revenue" class="flex-1 border-t-4 border-l-4 border-orange-500 flex flex-col">
          <div :class="headingClass">Revenue Streams</div>
          <textarea :class="fooClass" v-model="revenue"></textarea>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import EditText from "./components/EditText.vue";

export default {
  name: 'app',
  data: function() {
    return {
      partners: "",
      activities: "",
      resources: "",
      propositions: "",
      relationships: "",
      channels: "",
      segments: "",
      cost: "",
      revenue: ""
    };
  },
  components: {
    EditText
  },
  computed: {
    headingClass() { return "font-semibold text-lg ml-2 mt-2" },
    fooClass() { return "flex-foo p-2" }
  },
  mounted: function() {
    if (localStorage.partners) {
      this.partners = localStorage.partners;
    }
    if (localStorage.activities) {
      this.activities = localStorage.activities;
    }
    if (localStorage.resources) {
      this.resources = localStorage.resources;
    }
    if (localStorage.propositions) {
      this.propositions = localStorage.propositions;
    }
    if (localStorage.relationships) {
      this.relationships = localStorage.relationships;
    }
    if (localStorage.channels) {
      this.channels = localStorage.channels;
    }
    if (localStorage.segments) {
      this.segments = localStorage.segments;
    }
    if (localStorage.cost) {
      this.cost = localStorage.cost;
    }
    if (localStorage.revenue) {
      this.revenue = localStorage.revenue;
    }
  },
  watch: {
    partners: function(value) {
      localStorage.partners = value;
    },
    activities: function(value) {
      localStorage.activities = value;
    },
    resources: function(value) {
      localStorage.resources = value;
    },
    propositions: function(value) {
      localStorage.propositions = value;
    },
    relationships: function(value) {
      localStorage.relationships = value;
    },
    channels: function(value) {
      localStorage.channels = value;
    },
    segments: function(value) {
      localStorage.segments = value;
    },
    cost: function(value) {
      localStorage.cost = value;
    },
    revenue: function(value) {
      localStorage.revenue = value;
    },
  }


    
}
</script>

<style>

body {
  background: #EEE;
}

textarea {
  outline: 0;
}

</style>
