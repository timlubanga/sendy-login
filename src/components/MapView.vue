<template>
  <GoogleMap api-key="AIzaSyCwEcGBx0QtLenpuYSUtIny1kRpEY_8miA" style="width: 100%; height: 91vh" :center="center" :zoom="15">
    <Marker :options="{ position: center }" />
  </GoogleMap>
</template>

<script>
import { defineComponent,computed } from "vue";
import { GoogleMap, Marker } from "vue3-google-map";
import { useGeolocation } from '../useGeolocation';


export default defineComponent({
  components: { GoogleMap, Marker },
  setup() {
    const { coords } = useGeolocation()
    const center = computed(() => ({
      lat: coords.value.latitude,
      lng: coords.value.longitude
    }))
    return { center };
  },
  
 
  
});
</script>