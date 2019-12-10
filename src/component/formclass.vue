<template>
  <div>
    <form>
      <div id="form-header">
        <slot name="form-header"></slot>
      </div>
      <div id="form-field">
        <slot name="form-field"></slot>
      </div>
      <div id="form-control">
        <slot name="form-control"></slot>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style>
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
