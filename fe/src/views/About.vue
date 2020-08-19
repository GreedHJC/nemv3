<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12" md="6">
        <v-textarea
          name="input-7-1"
          label="Default style"
          v-model="ta"
        ></v-textarea>
      </v-col>
    </v-row>
    <v-layout row warp>
    <v-flex xs12 sm6 md4 v-for="x in 4" v-bind:key="x">
      <v-card class="mx-auto" max-width="600">
        <v-img src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg" height="200px"></v-img>

        <v-card-title primary-title>
          <div>
            <v-chip>{{x}}</v-chip>
            <div class="headline">Top western road trips</div>
            <span class="grey--text">1000</span>
          </div>
        </v-card-title>

        <v-card-actions>
          <v-btn text>Share</v-btn>
          <v-btn color="purple" text> Explore </v-btn>
          <v-spacer></v-spacer>
          <v-btn icon @click="show = !show">
            <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-expand-transition>
          <div v-show="show">
            <v-divider></v-divider>
            <v-card-text v-show="show">
              I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
            </v-card-text>
          </div>
        </v-expand-transition>
      </v-card>
    </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'about',
  data () {
    return {
      ta: 'debug',
      show: false
    }
  },
  mounted () {
    const a = { a: 1, b: 2 }
    this.ta = JSON.stringify(a)
    console.log('page start')
  }
}
</script>
