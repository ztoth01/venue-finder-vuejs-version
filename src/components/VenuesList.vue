<template>
   <div v-show="search" class="col-md-10 col-lg-8 mx-auto" id="result-inner">
        <div class="page-header">
            <h3 id="tables" class="my-2">Results for: {{ location }} </h3>
        </div>
        <div v-for="(venue, index) in venuesList" :key="index" class="card text-white bg-secondary mb-3" >
            <div class="card-header">
                <h3>{{ venue.venue.name }}</h3>
            </div>
            <div class="card-body">
                <h4 class="card-title">Additional inforamtion</h4>
                <p class="card-text">Additional information</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
    name: 'VenuesList',
    props:['venuesList','location','search']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>