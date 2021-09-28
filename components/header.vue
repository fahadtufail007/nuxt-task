<template>
  <div>
    <div class="header-border"></div>
    <div class="header">
      <div class="login_text">Login</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'header'
  }
</script>

<style lang="scss" scoped>

  .header {
    box-shadow: 0px 4px 5px -2px rgba(100, 100, 100, 0.43);
    @apply bg-white p-8 rounded-lg rounded-bl-xl rounded-br-xl flex justify-end;
  }
  .header-border {
    background-color: linear-gradient(to right, #009999 26%, #207cb9 61%);
    @apply w-full h-4;
  }
  .login_text {
    color: rgb(68, 172, 172);
    @apply text-base font-medium not-italic font-sans cursor-pointer;
  }

</style>
