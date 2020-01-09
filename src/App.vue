<template>
  <div class="container">
    <app-header/>
    <hr>
    <div class="row">
      <servers/>
      <app-server-details/>
    </div>
    <hr>
    <app-footer/>
  </div>
</template>

<script>
import Header from "@/components/Shared/Header/Header";
import Servers from "@/components/Server/Servers/Servers";
import ServerDetails from "@/components/Server/ServerDetails/ServerDetails";
import Footer from "@/components/Shared/Footer/Footer";

export default {
  name: 'app',
  components: {
    appHeader: Header,
    Servers,
    AppServerDetails: ServerDetails,
    AppFooter: Footer
  }
}
</script>

<style>

</style>
