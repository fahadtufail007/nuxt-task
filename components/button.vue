<template>
  <div class="footer">
    <div class="button">
      <a class="button-text" href="#">kostenlos Registrieren</a>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'button'
  }
</script>

<style lang="scss" scoped>

 .footer {
    box-shadow: 0px -4px 4px -1px rgba(128, 125, 125, 0.43);
    @apply bg-white p-4 rounded-bl-xl rounded-br-xl;
  }
  .button {
    background: linear-gradient(to right, #009999 26%, #207cb9 61%);
    @apply p-2.5 rounded-lg flex justify-center items-center cursor-pointer;
  }
  .button-text {
    @apply no-underline text-white text-sm font-medium not-italic	font-sans;
  }

</style>
