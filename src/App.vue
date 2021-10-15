<template>
  <div style="display:flex">
    <Sheet style="margin-left:20px">
      <h3>Memo to myself</h3>
      <p>Always prepare for PLFs in time!</p>
      <img src="info.svg" width="80px" />
    </Sheet>
    <Sheet style="margin-left:20px">
      <p>INSY, SEW and Webtechnologies are our favorite subjects!</p>
      <span style="font-style: italic">Starkschwitz Fiedler, Jan Schreck</span>
      <p>Wish i was there!</p>
      <span style="font-style: italic">E. Wahn</span>
    </Sheet>
  </div>
</template>

<script>
import Sheet from '@/components/Sheet.vue';
export default {
  components: {
    Sheet,
  },
};
</script>

<style lang="scss" scoped></style>
