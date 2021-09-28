<template>
  <div>
    <div class="tab">
      <button class="tablinks btn-left-radius active" @click="openCity($event, 'London')">Arbeitnehmer</button>
      <button class="tablinks" @click="openCity($event, 'Paris')">Arbeitgeber</button>
      <button class="tablinks btn-right-radius" @click="openCity($event, 'Tokyo')">Temporarburo</button>
    </div>

    <div id="London" class="tabcontent" style="display: block">

      <div class="tab-heading">Drei einfache Schritte</div>
      <div class="tab-heading">Zu deinem neuen job</div>
      <div class="image-container">
        <img class="tab1-first-img" src="../assets/tab1firstimg.png" />
      </div>
      <div class="fist-container">
        <div class="one-bg-container">
          <div class="text-style">1.</div>
        </div>
        <div class="text-container">
          <div class="num-one-text">Erstellen dein Lebenslauf</div>
          <!-- <div class="num-one-text">Unternehmensprofil</div> -->
        </div>
      </div>
      <div class="second-container">
        <div class="second-text_container">
          <div class="two-text-style">2.</div>
          <div class="erstellen-text">Erstellen dein Lebenslauf</div>
        </div>

        <div class="second-image-container">
          <img class="tab1-first-img" src="../assets/tab1secondimg.svg" />
        </div>
      </div>
      <div class="third-main-container">
        <div class="third-container"> </div>
        <div class="third-text_container">
          <div class="third-text-style">3.</div>
          <div>
            <div class="erstellen-dein-text"> Mit rur einem Klickbewerben </div>
          </div>
        </div>
      </div>
      <div class="third-image-container">
        <img class="tab1-first-img" src="../assets/tab1thirdimg.svg" />
      </div>

    </div>

    <div id="Paris" class="tabcontent">


      <div class="tab-heading">Drei einfache Schritte</div>
      <div class="tab-heading">Zu deinem neuen Mitarbeiter</div>
      <div class="image-container">
        <img class="tab1-first-img" src="../assets/tab1firstimg.png" />
      </div>
      <div class="fist-container">
        <div class="one-bg-container">
          <div class="text-style">1.</div>
        </div>
        <div class="text-container">
          <div class="num-one-text">Erstellen dein</div>
          <div class="num-one-text">Unternehmensprofil</div>
          <!-- <div class="num-one-text">Unternehmensprofil</div> -->
        </div>
      </div>
      <div class="second-container">
        <div class="second-text_container">
          <div class="two-text-style">2.</div>
          <div class="erstellen-text">Erstellen ein Jobinserat</div>
        </div>

        <div class="second-image-container">
          <img class="tab1-first-img" src="../assets/2tab2.svg" />
        </div>
      </div>
      <div class="third-main-container">
        <div class="third-container"> </div>
        <div class="third-text_container">
          <div class="third-text-style">3.</div>
          <div>
            <!-- <div class="erstellen-dein-text">bewerben </div> -->
            <div class="erstellen-dein-text">Wahle deinen neuen Mitarbeiter aus</div>
          </div>
        </div>
      </div>
      <div class="third-image-container">
        <img class="tab1-first-img" src="../assets/2tab1.svg" />
      </div>

    </div>

    <div id="Tokyo" class="tabcontent">


      <div class="tab-heading">Drei einfache Schritte zur</div>
      <div class="tab-heading">Vermittlung neuer Mitarbeiter</div>
      <div class="image-container">
        <img class="tab1-first-img" src="../assets/tab1firstimg.png" />
      </div>
      <div class="fist-container">
        <div class="one-bg-container">
          <div class="text-style">1.</div>
        </div>
        <div class="text-container">
          <div class="num-one-text">Erstellen dein Unternehmensprofil</div>
          <!-- <div class="num-one-text">Unternehmensprofil</div> -->
        </div>
      </div>
      <div class="second-container">
        <div class="second-text_container">
          <div class="two-text-style">2.</div>
          <div>
            <div class="erstellen-text1">Erhalte Vermittlungs</div>
          <div class="erstellen-text">angebot von Arbeitgeber</div>
          </div>
        </div>

        <div class="second-image-container">
          <img class="tab1-first-img" src="../assets/lastTab2.svg" />
        </div>
      </div>
      <div class="third-main-container">
        <div class="third-container"> </div>
        <div class="third-text_container">
          <div class="third-text-style">3.</div>
          <div>
            <div class="erstellen-dein-text">Vermittlung nach Provision oder Stundenlohn</div>
          </div>
        </div>
      </div>
      <div class="third-image-container">
        <img class="tab1-first-img" src="../assets/lastTab1.svg" />
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    name: 'bottomTab',
    methods: {
      openCity: function(evt, cityName) {
        var i, tabcontent, tablinks;
        tabcontent = document.getElementsByClassName("tabcontent");
        for (i = 0; i < tabcontent.length; i++) {
          tabcontent[i].style.display = "none";
        }
        tablinks = document.getElementsByClassName("tablinks");
        for (i = 0; i < tablinks.length; i++) {
          tablinks[i].className = tablinks[i].className.replace("active", "");
        }
        document.getElementById(cityName).style.display = "block";
        evt.currentTarget.className += " active";
      }
    }
  }
</script>

<style lang="scss" scoped>

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
