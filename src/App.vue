<template>
  <div>
    <!-- <app-form>
      <div slot="form-header">
        <h3>Form for get the basic infomation.</h3>
      </div>
      <div slot="form-field">
        <input type="text" placeholder="Enter person full name" />
        <br />
        <input type="number" placeholder="Enter person Mobile number" />
        <br />
        <input type="email" placeholder="Enter person Email" />
        <br />
        <input type="password" placeholder="Enter the Password" />
        <br />
      </div>
      <div slot="form-control">
        <button v-on:click="handleSubmit">Submit</button>
      </div>
    </app-form>-->
    <component v-bind:is="components"></component>
    <button v-on:click="components ='main-form'">Main form</button>
    <button v-on:click="components ='app-form'">secondform</button>
  </div>
</template>

<script>
import formclass from "./component/formclass.vue";
import formmain from "./component/formmain.vue";
export default {
  components: {
    "app-form": formclass,
    "main-form": formmain
  },
  data() {
    return {
      components: "app-form"
    };
  },
  methods: {
    handleSubmit: function() {
      alert("hello");
    }
  }
};
</script>

<style>
input {
  margin: 5px;
  padding: 5px;
  text-align: center;
}
div {
  text-align: center;
}
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
