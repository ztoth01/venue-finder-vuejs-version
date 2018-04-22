<template>
   <div class="bs-component">
        <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
            <a class="navbar-brand" href="#">{{ msg }}</a>
        </nav>
    </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      msg: 'Venue Finder'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
