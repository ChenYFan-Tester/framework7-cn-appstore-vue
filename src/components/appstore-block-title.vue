<template>
    <div class="block-title appstore-block-title">
      <span v-if="title">{{title}}</span>
      <slot></slot>
    </div>
</template>

<script>
export default {
    props: {
        title: String,
    }
}
</script>

<style lang="less">
@import url("../css/_mixins.less");

.appstore-block-title {
  .hairline(top, var(--f7-block-strong-border-color));
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 10px;
  white-space: normal;
  --f7-block-title-font-size: 21px;
  --f7-block-title-font-weight: bold;
  --f7-block-title-line-height: 1.4;
  > .link {
    font-size: 17px;
    font-weight: normal;
    flex-shrink: 0;
  }
}
</style>