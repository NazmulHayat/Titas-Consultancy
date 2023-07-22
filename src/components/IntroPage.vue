<template>
    <v-container fluid fill-height>
        <v-row no-gutters>
            <v-col>
            <video autoplay muted loop :src="videoSrc" class="fullscreen-video"></video>
            </v-col>
        </v-row>
        <div class="overlay mr-0 ml-0">
            <v-row>
                <v-col cols="12" class="text-center">
                    <div class="welcome pb-4"> WELCOME TO TITAS CONSULTANCY </div>
                    <v-row class="sh" justify="center">
                        <div class="opening pt-4 pr-2">COMING SOON</div>
                        <div class="exc pt-4 "> !! </div>
                    </v-row>
                </v-col>
            </v-row>
        </div>
    </v-container>
</template>

<script>
export default {
  data() {
    return {
      videoSrc: require('../assets/intro-video.mp4')
    };
  },
  mounted(){      
        window.setTimeout(()=>{
                document.getElementsByClassName('sh')[0].style.animation = "transitionIn3 2.0s forwards";
        },1000);
    }
};
</script>


<style>

@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@700&display=swap');

.fullscreen-video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  opacity: 1;
  filter: brightness(60%);
}

.sh{
    opacity: 0;
}

.v-row{
    margin: 0px;
}

.overlay{
    margin-left: 12px !important;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 1; /* Higher z-index to cover the video */
}

.welcome, .opening, .exc {
    font-family: 'Oswald', sans-serif !important;
    font-size: 30px;
    font-weight: bold;
    color: white;
}

.exc{
    color: red;
}

*, ::before, ::after {
    background-repeat: no-repeat;
    box-sizing: content-box !important;
    overflow: hidden;
    margin: 0px;
}

@media screen and (min-width: 550px) {
    .welcome, .opening, .exc{
        font-size: 40px;
    }
}

@media screen and (min-width: 750px) {
    .welcome, .opening, .exc{
        font-size: 45px;
    }
}

@media screen and (min-width: 1000px) {
    .welcome, .opening, .exc{
        font-size: 50px;
    }
}

@media screen and (min-width: 1200px) {
    .welcome, .opening, .exc{
        font-size: 55px;
    }
}


@keyframes transitionIn3 {
        from {
            opacity: 0;
            transform: translateX(300px);
        }
        to{
            opacity: 1;
            transform: translateY(0);
        }
    }

</style>