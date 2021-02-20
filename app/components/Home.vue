<template>
    <Page>
      <ActionBar title="My App"></ActionBar>

        <StackLayout>
          <ActivityIndicator class="loader" busy="true" @busyChange="busy = false" />
          <Button text="Home" @tap="$navigateTo(this)" />
          <Button text="Elements" @tap="$navigateTo(ElementsUI)" />
        </StackLayout>
    </Page>
</template>

<script>
import ElementsUI from "~/pages/ElementsUI";

export default {
  data() {
    return {
      ElementsUI,
      busy: false,
      isEditing: false,
    }
  },
  computed: {
    message() {
      return "Blank {N}-Vue app";
    }
  }
};
</script>

<style scoped lang="scss">
    @import '~@nativescript/theme/scss/variables/blue';
    $accent: #0f9;

    .loader {
      vertical-align: top;
      horizontal-align: center;
      color: $accent;
      background: transparent;
    }

    .info {
        font-size: 30px;
        horizontal-align: center;
        vertical-align: center;
    }
</style>
