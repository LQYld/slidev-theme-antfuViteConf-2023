<template>
  <div class="background-grow transition-all duration-600 ease-in-out green-neon-light opacity-50" :class="currentIllumiation" />
</template>
<script setup>
  import { computed } from "vue"
  const defaultIllumiation = `illumiation-right-up`;
  const illumiationMap = {
    [`right-up`]: `illumiation-right-up`,
    [`right-middle`]: `illumiation-right-middle`,
    [`right-down`]: `illumiation-right-down`,
    [`left-down`]: `illumiation-left-down`,
    [`left-middle`]: `illumiation-left-middle`,
    [`left-up`]: `illumiation-left-up`,
    [`top-up`]: `illumiation-top-up`,
    [`top-down`]: `illumiation-top-down`,
  }
  const currentIllumiation = computed(() => {
    const currentPage = $slidev.nav.currentPage
    return illumiationMap[$slidev?.configs?.themeConfig?.position?.[currentPage]] || defaultIllumiation
  })
</script>
<style>
.green-neon-light{
  position: fixed;
  background-image: linear-gradient(to right , rgb(207 200 89 / 1 ) 0% , rgb(77 189 127 / 1 ) 50% , rgb(77 189 172 / 1 ) 100%);
}

.illumiation-right-up{
  top: 30%;
  left: 80%;
  width: 520px;
  height: 520px;
  transform: translate(-50%, -50%) rotate(-45deg);
  filter: blur(140px);
}

.illumiation-left-down{
  top: 90%;
  left: 0%;
  width: 520px;
  height: 520px;
  transform: translate(-50%, -50%) rotate(-45deg);
  filter: blur(140px);
}

.illumiation-left-middle{
  top: 50%;
  left: -10%;
  width: 520px;
  height: 520px;
  transform: translate(-50%, -50%) rotate(-45deg);
  filter: blur(140px);
}

.illumiation-left-up{
  top: 0%;
  left: 0%;
  width: 520px;
  height: 520px;
  transform: translate(-50%, -50%) rotate(-45deg);
  filter: blur(140px);
}

.illumiation-top-down{
  top: 130%;
  left: 50%;
  width: 780px;
  height: 780px;
  transform: translate(-50%, -50%) rotate(-45deg);
  filter: blur(210px);
}

.illumiation-right-middle{
  top: 50%;
  right: -10%;
  width: 520px;
  height: 520px;
  transform: translate(50%, -50%) rotate(-45deg);
  filter: blur(140px);
}

.illumiation-right-down{
  top: 90%;
  right: 0%;
  width: 520px;
  height: 520px;
  transform: translate(50%, -50%) rotate(-45deg);
  filter: blur(140px);
}

.illumiation-top-up{
  top: 35%;
  left: 50%;
  width: 312px;
  height: 312px;
  transform: translate(-50%, -50%) rotate(-45deg);
  filter: blur(84px);
}

</style>