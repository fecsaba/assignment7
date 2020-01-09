<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <app-server
                    v-for="server in servers"
                    :key="server"
                    :server="server"

            />
        </ul>
    </div>
</template>

<script>

    import Server from "@/components/Server/Server/Server";

    export default {
        data: function() {
            return {
                servers: [
                    { id : 1, status: 'Normal'},
                    { id : 2, status: 'Critical'},
                    { id : 3, status: 'Unknown'},
                    { id : 4, status: 'Critical'},
                    { id : 5, status: 'Normal'}
                ]
            }
        },
        props: {
        },
        components: {
            appServer: Server
        }
    };
</script>
