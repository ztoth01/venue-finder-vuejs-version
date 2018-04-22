<template>
    <div v-show="error" class="alert alert-dismissible alert-danger mt-4 text-center">
        <p>Opps! No venues can be found at this location</p>
    </div>
</template>

<script>
export default {
    name: 'AlertMessage',
    props:['error'],
    data () {
        return {
          
        }
    }
}
</script>