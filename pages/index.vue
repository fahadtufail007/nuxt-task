<template>
  <div  class="main-container">
    <div id='container' class="mobile-view_container">
      <headers></headers>
      <topText></topText>
      <headerButton></headerButton>
      <div class="border-bottom"></div>
      <bottomTabs></bottomTabs>
    </div>
  </div>
</template>

<script>
  import Header from '../components/header.vue'
  import Button from '../components/button.vue'
  import TopText from '../components/topText.vue'
  import BottomTabs from '../components/bottomTabs.vue'
    export default {
      name: 'container',
      components: {
        'headers': Header,
        'headerButton': Button,
        'topText': TopText,
        'bottomTabs': BottomTabs
      }
    }
</script>

<style lang="scss" scoped>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.main-container {
  @apply min-h-screen flex justify-center items-center mx-auto;
}
.mobile-view_container {
  background-color: rgb(217, 236, 236);
  @apply h-screen w-96 flex justify-between flex-col;
}

.border-bottom {
  border-top: 2px solid rgb(230, 227, 227);
  @apply mt-7;
}

.tab {
  @apply bg-white flex justify-center mt-7;
}

/* Style the buttons inside the tab */
.tab button {
  color: rgb(68, 172, 172);
  border: 1px solid rgb(221, 220, 220);
  @apply bg-white cursor-pointer px-2 py-2.5 text-sm font-medium ;
}

/* Change background color of buttons on hover */
.tab button:hover {
  background-color: rgb(84, 230, 230);
  @apply text-white;
}

/* Create an active/current tablink class */
.tab button.active {
  background-color: rgb(84, 230, 230);
  @apply text-white;
}

/* Style the tab content */
.tabcontent {
  @apply hidden border-t-0 relative;
}

.btn-left-radius {
  @apply rounded-bl-xl rounded-tl-xl;
}

.btn-right-radius {
  @apply rounded-br-xl rounded-tr-xl;
}

.tab-heading {
  @apply text-center text-base text-black font-medium mt-0.5 font-sans;
}

.tab1-first-img {
  @apply w-7/12 bg-no-repeat	bg-contain z-50;
}

.image-container {
  @apply flex justify-end	mt-7 mr-5;
}

.one-bg-container {
  background-color: rgb(250, 250, 250);
  border-top-right-radius: 200px;
  border-bottom-right-radius: 200px;
  @apply h-44	w-44 flex justify-center items-center	absolute top-40;
}

.text-style {
  color: rgb(101, 98, 124);
  @apply text-9xl font-medium;
}

.two-text-style {
  color: rgb(101, 98, 124);
  @apply text-9xl font-medium ml-7;
}

.third-text-style {
  @apply text-9xl font-medium ml-7 -mt-40;
  color: rgb(101, 98, 124);
}

.fist-container {
  @apply flex items-center;
}

.num-one-text {
  @apply z-50 text-black text-base font-sans leading-5	;
}

.text-container {
  @apply z-50 ml-36	mt-7;
}

.second-container {
  clip-path: polygon(51% 1%, 76% 6%, 100% 0, 100% 91%, 82% 98%, 48% 99%, 20% 95%, 0 98%, 0 0, 21% 5%);
  background-color: rgb(232, 248, 253);
  @apply mt-10 p-5;
}

.second-text_container {
  @apply flex items-center;
}

.erstellen-text {
  @apply text-base font-sans text-black;
}

.erstellen-text1 {
  @apply mt-16 text-base font-sans text-black;
}

.second-image-container {
  @apply flex justify-center ml-10;
}

.third-image-container {
  @apply flex justify-center -mt-44; 
}

.third-container {
  clip-path: circle(44.7% at 23% 49%);
  background-color: rgb(250, 250, 250);
  @apply h-80 w-80 -mt-10 flex justify-center items-center;
}

.third-main-container {
  @apply flex items-center;
}

.third-text_container {
  @apply flex absolute;
}

.erstellen-dein-text {
  @apply -mt-10 text-base font-sans text-black w-9/12 text-center -mt-32;
}
.erstellen-dein-text1 {
  @apply -mt-12 text-base font-sans text-black;
}

</style>
