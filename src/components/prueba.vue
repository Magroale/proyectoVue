<template>

</template>

<script>
import axios from 'axios'

export default {
    
    name: 'HelloWorld',
    props: {
        msg: String
    },
    data() {
        return {
        }
    },
    methods: {
        fetchData() {
            axios.get('http://127.0.0.1:8000/home_page')
                .then(response => {
                    this.infoViajes = response.data;
                    console.log(this.data)
                })
                .catch(error => {
                    console.error('Error fetching data:', error);
                });
        },
    },
}
</script>
  
<style scoped></style>