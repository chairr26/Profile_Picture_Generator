<template>
  <div class="container mt-5">
    <b-form @submit.prevent="onSubmit">

      <b-form-group id="input-group-2" label="Any word:" label-for="input-2">
        <b-form-input id="input-2" v-model="form.name" placeholder="Enter name" required></b-form-input>
      </b-form-group>

      <b-button type="submit" variant="primary">Make your avatar</b-button>
    </b-form>
    <b-card class="mt-3 hasil" header="Here is your avatar">
      <b-img thumbnail rounded="circle" :src="'https://robohash.org/'+this.newname"></b-img>
    </b-card>
  </div>
</template>

<script>

export default {
    name: 'ContentView',
    data() {
      return {
        form: {
          name: '',
        },
        newname : 'chairrul la umang'
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        this.newname = this.form.name.toLowerCase().trim()
        console.log(this.newname);
      }
    }
  }
</script>

<style>
.hasil {
  text-align: center;
}
</style>
