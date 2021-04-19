<template>
  <div id="app">
    
    <SmartNavbar />

    <main>
      <router-view/>
    </main>
  </div>
</template>

<script>
import SmartNavbar from '@/components/SmartNavbar'

export default {
  name: 'App',
  components: {
    SmartNavbar,
  }
}
</script>

