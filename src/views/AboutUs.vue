<template>
  <div class="aboutus">
    <Header />
    <div class="header">
      <div class=" mb-2">
        <h4 id="textitle"><strong>About Us</strong></h4>
      </div>
      <div class="overflow-hidden pr-2 pl-2 pb-1 pt-2  shadow "
      style="max-width: 540px; background: #e07a1b; margin-right: 30px; margin-left:30px; margin-top: 15px; margin-bottom: 10px; border-radius: 20px">
      
      <div class="d-flex flex-column align-items-center p-4" id="text">
        <h5 class="mt-3">
          {{ info.title }}
        </h5>
        <h6 class="h6 mt-3" id="text">
          {{ info.description }}
        </h6>
        <h5 class="mt-3" id="text">{{ info.title2 }}</h5>
        <h6 class="h6 m-3 " id="text">{{ info.description2 }}</h6>
      </div>
    </div>
    </div>
    <h4 class="mt-4" id="textitle"><strong>Meet our team</strong></h4>
    <div class="body d-flex flex-lg-row align-items-center justify-content-center">
      <div class="card " v-for="item in items" :key="item.message">
        <div class="imgBox">
          <img :src="item.imageDog" />
          <img :src="item.imageMe" alt="" />
        </div>
        <div class="details">
          <div class="content" id="text">
            {{ item.namePerson }}
            <div>
              <p class="infoCard" id="text">{{ item.profession }}</p>
              <p class="infoCard" id="text">{{ item.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import Niki from "@/assets/DogMartin.png";
import Martin from "@/assets/martin.jpg";
import Pingo from "@/assets/DogCris.jpg";
import Cris from "@/assets/cris.jpg";
import janna from "@/assets/janna.jpg";
import janna1 from "@/assets/janna1.jpg";
import thierno from "@/assets/thierno.jpeg";
import Amr1 from "@/assets/Amr1.jpeg";
import Amr from "@/assets/Amr.jpeg";
import conejo from "@/assets/conejo.jpeg";
import crock from "@/assets/crock.jpg";
import abdulha from "@/assets/abdulha.jpg";
export default {
  name: "aboutus",
  components: {
    Header,
    Footer,
    Niki,
    Martin,
    Pingo,
    Cris,
    thierno,
    janna,
    janna1,
    Amr,
    Amr1,
    conejo,
    crock,
    abdulha,
  },
  data() {
    return {
      info: {
        title:
          "Welcome to DoggyF, the App for doggy-lovers. The couchsurfing for dogs",
        description:
          "Do you lack time to take care or walk your dog? Would you like to walk other people's dog? Would you like to help create an altruistic community ofdoggy-lovers?",
        title2: "In DoggyF you will find the answers!",
        description2:
          "In order to participate in the DoggyF community, the first thing you must do is register as a user.From there, you can edit post ads according to the Dogs or Sitters category and contact other users.If not, you can only consult the published announcements.",
      },
      items: [
        {
          namePerson: "Martín",
          profession: "Doggy-lover and programmer",
          description: "I love bothering dogs",
          imageDog: Niki,
          imageMe: Martin,
        },
        {
          namePerson: "Thierno",
          profession: "Graphic designer and Doggy-lover",
          description: "My rabbit is my life",
          imageDog: conejo,
          imageMe: thierno,
        },
        {
          namePerson: "Cris",
          profession: "Doggy-lover and programmer",
          description: "To err is human — to forgive, canine.",
          imageDog: Pingo,
          imageMe: Cris,
        },
        {
          namePerson: "Amr",
          profession: "Graphic designer and Doggy-lover",
          description: "Animation and shisha and dancing",
          imageDog: Amr1,
          imageMe: Amr,
        },
        {
          namePerson: "Zhanna",
          profession: "Doggy-lover and Graphic designer",
          description: "Future for all with animals",
          imageDog: janna,
          imageMe: janna1,
        },
        {
          namePerson: "Abdulha",
          profession: "Programmer and and Doggy-lover",
          description: "More programming and walks",
          imageDog: crock,
          imageMe: abdulha,
        },
      ],
    };
  },
};
</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.aboutus {
  background-image: url("../assets/background1.png");
}
.header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px;
}
.body {
  margin: 20px;
  min-height: 100vh;
  flex-wrap: wrap;
}
p {
  margin-top: 20px;
  margin-bottom: 20px;
}
#text {
  color: black;
}

#textitle {
  color: black;
  font-weight: bold;
}
.card {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  position: relative;
  width: 250px;
  height: 350px;
  background: white;
  transform-style: preserve-3d;
  transform: perspective(1000px);
  box-shadow: 10px 20px 40pc rgba(0, 0, 0, 0.25);
  transition: 1s;
 margin: 100px;
  
}
.card:hover {
  transform: translateX(50%);
}
.card .imgBox {
  position: relative;
  width: 100%;
  height: 100%;
  z-index: 1;
  transform-origin: left;
  transform-style: preserve-3d;
  background: black;
  transition: 1s;
  box-shadow: 10px 20px 40pc rgba(0, 0, 0, 0.25);
}
.card:hover .imgBox {
  transform: rotateY(-180deg);
}
.card .imgBox img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  transform-style: preserve-3d;
  backface-visibility: hidden;
}
.card .imgBox img:nth-child(2) {
  transform: rotateY(180deg);
}
.card .details {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  padding: 10px;
  margin-top: 5px;
}
.card .details .content {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.details {
  font-size: 15px;
}
@media (max-width: 420px) {
  body{
display: flex;
justify-content: center;
align-items: center;
margin: 0;
  }
  .card {
    justify-content: center;
    align-items: center;
    position: relative;
    width: 140px;
    height: 180px;
    background: white;
    transform-style: preserve-3d;
    transform: perspective(1000px);
    box-shadow: 10px 20px 40pc rgba(0, 0, 0, 0.25);
    transition: 1s;
    margin: 20px;
    
  }
.infoCard {
  width: 100px;
  display: flex;
  flex-wrap: wrap;
  font-size: 10px;
}
}
</style>