<template>
    <div class="col-xs-12 col-sm-6">
        <p v-if="!server">Please select a server</p>
        <p v-else>{{ server.id }} selected, Status: {{ server.status }}</p>
        <button @click="changeStatus">Change status</button>
    </div>
</template>

<script>
    import {dataBus} from "@/main";

    export default {
        props: {

        },
        data: function () {
            return {
                server: null
            }
        },
        created() {
            dataBus.$on('serverSelection', (server) => {
                this.server = server
            })
        },
        methods: {
            changeStatus() {
                this.server.status = 'Normal'
            }
        }
    };
</script>
