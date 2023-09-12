<template>
  <div class="sign-in">
    <div class="sign-in__info">
      <LogoBlock />
      <FormBlock />
      <CopyrightBlock />
    </div>

    <div class="sign-in__bg">
      <BackgroundBlock />
    </div>
  </div>
</template>

<script>
import FormBlock from "./components/FormBlock.vue";
import CopyrightBlock from "./components/CopyrightBlock.vue";
import LogoBlock from "./components/LogoBlock.vue";
import BackgroundBlock from "./components/BackgroundBlock.vue";

export default {
  components: {
    FormBlock,
    CopyrightBlock,
    LogoBlock,
    BackgroundBlock,
  },
};
</script>

<style lang="scss">
@import "/src/scss/style.scss";
.sign-in{
  display: flex;
  gap: 156px;
}
</style>
