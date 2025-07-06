<template>
<PageHeader :activeTab="activeTab" @setTab="(value) => setTab(value)" />

<PageHome v-if="activeTab === 'home'" />

<PageRules v-if="activeTab === 'rules'" />

<PageContacts v-if="activeTab === 'contacts'" />


</template>

<script>
import SvgLogo from '@/components/icons/SvgLogo.vue';
import PageHeader from '@/components/PageHeader.vue';
import PageHome from '@/components/page/PageHome.vue';
import PageRules from '@/components/page/PageRules.vue';
import PageContacts from '@/components/page/PageContacts.vue';

export default {
  components: {
    PageHome,
    PageRules,
    PageHeader,
    PageContacts,
    SvgLogo,

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
