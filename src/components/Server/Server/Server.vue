<template>
    <div class="Server">
        <li class="list-group-item"
            @click="serverSelected">
            Server #{{ server.id }} - status: {{ server.status }}

        </li>
    </div>
</template>

<script>
    import {dataBus} from "@/main";

    export default {
        props: ['server'],
        data: function () {

        },

        methods: {
            serverSelected() {
                dataBus.$emit('serverSelection', this.server)
            }
        }
    };
</script>
