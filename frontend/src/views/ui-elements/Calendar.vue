<template>
  <div id="calendar">
    <page-title-bar></page-title-bar>
    <div class="row">
      <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12">
        <app-card customClasses="grid-b-space" :heading="$t('message.calendar')"
          class="predifined-btn-style">
          <div>
            <b-row>
              <b-col md="auto">
                <b-calendar v-model="value" @context="onContext" locale="en-US"></b-calendar>
              </b-col>
            </b-row>
          </div>
        </app-card>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
  	name: "calendar",
    data() {
      return {
        value: '',
        context: null
      }
    },
    methods: {
      onContext(ctx) {
        this.context = ctx
      }
    }
  }
</script>