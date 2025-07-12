<template>
<PageHeader :activeTab="activeTab" @setTab="(value) => setTab(value)" />

<RouterView />

</template>

<script>
import PageHeader from '@/components/PageHeader.vue';

export default {
  components: {
    PageHeader,
  },
    data() {
    return {
      activeTab: "home"
    };
  },
    methods: {
    setTab(tab) {
      this.activeTab = tab;
    }
  }
}

</script>

<style lang="less">




@keyframes flicker {
  from {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}


</style>
