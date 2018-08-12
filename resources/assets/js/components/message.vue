<template>
    <div>
    <li class="list-group-item " :class="className"><span class="badge badge-primary float-rigth">{{user}}:</span><slot></slot><small style="float: right;">{{time}}</small></li>


    </div>
</template>

<script>
    export default {
        props:[
            'color','user','time'
        ],
        computed:{
            className(){
                return 'list-group-item-'+this.color
            }
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
