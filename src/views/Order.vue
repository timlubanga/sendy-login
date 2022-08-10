<template>
  <div class="home">
    <MapView/>
    <MakeOrder/>
  </div>
</template>

<script>
// @ is an alias to /src
import MapView from '@/components/MapView.vue'
import MakeOrder from '@/components/MakeOrder.vue'

export default {
  name: 'OrdersView',
  components: {
    MapView,
    MakeOrder
  }
}
</script>
