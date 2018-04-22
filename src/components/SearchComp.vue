<template>
  <div class="search card card-body mt-5 col-md-10 col-lg-8 mx-auto">
        <h1>Find recommended venues</h1>
        <p class="lead">Enter the place you're interested in</p>
        <input type="text" v-model="searchInput" class="form-control" :class="{'is-invalid' : error}"  @focus="inputFocus" placeholder="Location">
        <span v-if="error" class="warning d-block invalid-feedback mt-2">Please make sure you enter a location</span>
        <br>
        <button class="btn btn-success" @click="getLocation">Search</button>
        <br>
        <div id="api-response"></div>
    </div>
</template>

<script>
export default {
    name: 'SearchComp',
    data () {
        return {
            searchInput: '',
            error: false
        }
    },
    methods:{
        getLocation(e){
            if(this.searchInput === ""){
                this.error = true;
            }else{
                this.$emit('search', this.searchInput);
            }
            e.target.value = "";
        },
        inputFocus(e){
            this.error = false;
            e.target.value = "";
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
