<template>
  <div>
    <div>
      <div class="deine-job-text">Deine Job</div>
      <div class="deine-job-text">Website</div>
    </div>
    <img class="image-styling" src="../assets/testmobileimg.svg" />
  </div>
</template>

<script>
  export default {
    name: 'CenterHeader'
  }
</script>

<style lang="scss" scoped>

  .deine-job-text {
    @apply text-black text-center	not-italic font-sans mt-1.5 font-medium text-4xl	;
  }

  .image-styling {
    @apply w-full bg-contain bg-no-repeat;
  }

</style>
