<template>
    <div class="container">
        <ListDefault :elements-list="elements" />
    </div>
</template>

<script>
import ListDefault from "../partials/_ListDefault";
export default {
    components: {
        ListDefault
    },
    created(){
        this.findAll()
    },

    data(){
        return {
            elements:[]
        };
    }, 
    methods: {
        findAll: function(){
            fetch('http://127.0.0.1:8000/api/element/?format=json')
                .then(res => res.json())
                .then(res => this.elements = res)
        }
    },
}
</script>

<style>
    .box{
        border: 3px solid #CCC;
        margin: 8px 0 0 0;
    }
</style>