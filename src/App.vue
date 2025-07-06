<template>
<PageHeader />

<AppHome />


</template>

<script>
import SvgLogo from '@/components/icons/SvgLogo.vue';
import PageHeader from '@/components/PageHeader.vue';
import AppHome from '@/components/AppHome.vue';


export default {
  components: {
    AppHome,
    PageHeader,
    SvgLogo,

  },
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
