<template>   
<div>
    <li class="l-section section">
        <div class="bg-contact">
                <div class="hire">
                  <h2>Ön Başvurunu Yap!</h2>
                  <!-- checkout formspree.io for easy form setup -->
                  <form class="work-request" id="app" @submit="postForm" method="post">
                    <div class="work-request--information">
                      <div class="information-name">
                        <input  name="name" v-model="posts.name" id="name" type="text" spellcheck="false"> 
                        <label for="name">İsim</label>
                      </div> <br> <br>
                      <div class="information-name">
                        <input name="surname" v-model="posts.surname" id="surname" type="text" spellcheck="false">
                        <label for="surname">Soyisim</label>
                      </div> <br> <br>
                      <div class="information-name">
                        <input name="phoneNumber"  v-model="posts.phoneNumber" id="phoneNumber" type="text" spellcheck="false">
                        <label for="phoneNumber">Telefon</label>
                      </div> <br> <br>
                      <div class="information-email">
                        <input name="emailAddress" v-model="posts.emailAddress" id="emailAddress" type="email" spellcheck="false">
                        <label for="email">Email</label>
                      </div> <br> <br>
                      <div class="information-email">
                        <select name="university" id="university"  class="select-form">
                          <option selected value="">Üniversite Seçiniz...</option>
                        </select>
                      </div>
                      <div class="information-email">
                        <select name="department" id="department" class="select-form">
                          <option selected value="">Bölüm Seçiniz...</option>
                        </select>
                      </div>
                      <div class="information-email">
                        <select name="class" id="selectClass"  class="select-form">
                          <option selected value="">Sınıf Seçiniz...</option>
                          <option value="1">1.Sınıf</option>
                          <option value="2">2.Sınıf</option>
                          <option value="3">3.Sınıf</option>
                          <option value="4">4.Sınıf</option>
                          <option value="5">Yeni Mezun</option>
                        </select>
                      </div>
                      <div class="information-email">
                        <input name="graduationYear" maxlength="4" id="graduationYear" type="text" spellcheck="false">
                        <label for="graduateDate">Mezuniyet Yılı</label>
                      </div>
                    </div>
                    <!-- <div class="work-request--options">
                      <p style="margin-bottom: 20px;">Hangi Click4Career Etkinliklerine Katılacaksınız?</p>
                      <span class="options-a">
                        <input name="eventsChosen" id="opt-1" type="checkbox" value="app design">
                        <label for="opt-1">
                          <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 150 111"
                            style="enable-background:new 0 0 150 111;" xml:space="preserve">
                            <g transform="translate(0.000000,111.000000) scale(0.100000,-0.100000)">
                              <path
                                d="M950,705L555,310L360,505C253,612,160,700,155,700c-6,0-44-34-85-75l-75-75l278-278L550-5l475,475c261,261,475,480,475,485c0,13-132,145-145,145C1349,1100,1167,922,950,705z" />
                            </g>
                          </svg>
                          Gelecek Veri Analitiğinde!
                        </label>
                        <input name="eventsChosen" id="opt-2" type="checkbox" value="graphic design">
                        <label for="opt-2">
                          <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 150 111"
                            style="enable-background:new 0 0 150 111;" xml:space="preserve">
                            <g transform="translate(0.000000,111.000000) scale(0.100000,-0.100000)">
                              <path
                                d="M950,705L555,310L360,505C253,612,160,700,155,700c-6,0-44-34-85-75l-75-75l278-278L550-5l475,475c261,261,475,480,475,485c0,13-132,145-145,145C1349,1100,1167,922,950,705z" />
                            </g>
                          </svg>
                          Gelecek Çeviklikte!
                        </label>
                        <input name="eventsChosen" id="opt-3" type="checkbox" value="motion design">
                        <label for="opt-3">
                          <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 150 111"
                            style="enable-background:new 0 0 150 111;" xml:space="preserve">
                            <g transform="translate(0.000000,111.000000) scale(0.100000,-0.100000)">
                              <path
                                d="M950,705L555,310L360,505C253,612,160,700,155,700c-6,0-44-34-85-75l-75-75l278-278L550-5l475,475c261,261,475,480,475,485c0,13-132,145-145,145C1349,1100,1167,922,950,705z" />
                            </g>
                          </svg>
                          Gelecek Mobility'de!
                        </label>
                      </span>
                      <span class="options-b">
                        <input name="eventsChosen" id="opt-4" type="checkbox" value="ux design">
                        <label for="opt-4">
                          <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 150 111"
                            style="enable-background:new 0 0 150 111;" xml:space="preserve">
                            <g transform="translate(0.000000,111.000000) scale(0.100000,-0.100000)">
                              <path
                                d="M950,705L555,310L360,505C253,612,160,700,155,700c-6,0-44-34-85-75l-75-75l278-278L550-5l475,475c261,261,475,480,475,485c0,13-132,145-145,145C1349,1100,1167,922,950,705z" />
                            </g>
                          </svg>
                          Gelecek Çözüm Üretmekte!
                        </label>
                        <input name="eventsChosen" id="opt-5" type="checkbox" value="webdesign">
                        <label for="opt-5">
                          <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg"
                            xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 150 111"
                            style="enable-background:new 0 0 150 111;" xml:space="preserve">
                            <g transform="translate(0.000000,111.000000) scale(0.100000,-0.100000)">
                              <path
                                d="M950,705L555,310L360,505C253,612,160,700,155,700c-6,0-44-34-85-75l-75-75l278-278L550-5l475,475c261,261,475,480,475,485c0,13-132,145-145,145C1349,1100,1167,922,950,705z" />
                            </g>
                          </svg>
                          Gelecek TOFAŞ'ta!
                        </label>
                      </span>
                    </div>
                    <!<button type="button" v-on:click="uploadFile()">Add 1</button>
                    <p>The button above has been clicked {{ counter }} times.</p> --> 
                    <input type="submit" value="Başvur">
                  </form>
                </div>
              </div>
            </li>
</div>
</template>
<script>

import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'
Vue.use(VueAxios, axios)

// import LoadScript from 'vue-plugin-load-script';
 
//   Vue.use(LoadScript);
// Vue.loadScript("https://cdnjs.cloudflare.com/ajax/libs/meyer-reset/2.0/reset.min.css")

// Vue.loadScript("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css")

// Vue.loadScript("https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js")
// import '../node_modules/bootstrap/scss/bootstrap.scss';
// import "assets/css/loader-keyframes.css?ver=2.9";
// import "assets/css/loader-keyframes.css?ver=2.9";

export default {
    name: "PostComponent",
    data() {
        return { // reload edildiğinde bilgiler gitsin diye
            posts: {
                name: null,
                surname: null,
                phoneNumber:null,
                emailAddress: null,
                university: null,
                department: null,
                class: null,
                graduationYear: null,
            }
        }
    },
    methods: { // functiondır yani object
        postData(e){
            this.axios.post("//jsonplaceholder.typicode.com/posts",this.posts) //örnek bir localhost veriler buraya gider
            .then((result)=>{
                console.warn(result)
            } )
              e.preventDefault();
        }
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px; }

.bg-contact {
   width: 100%;
    height: auto !important;
    margin-top: 125px;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    /* background-image: url("../img/contact-visual.png"); */
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat
}

.bg-contact {
    top: 60px !important;
}

.bg-contact {
    top: 60px !important;
}

.hire ul {
    margin: 100px 0 0 !important;
}

.hire {
    position: relative;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    width: 700px;
    max-width: 75%;
    height: 100%;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -webkit-flex-direction: column;
    -ms-flex-direction: column;
    flex-direction: column;
    -webkit-box-pack: center;
    -webkit-justify-content: center;
    -ms-flex-pack: center;
    justify-content: center;
    margin: 0 auto;
}

@media (max-width: 1180px) {
    .hire {
        max-width: 100%
    }
}

.hire h2 {
    margin: 0 0 20px 0;
    font-size: 30px;
    text-align: center
}

.hire h2 {
    font-size: 21px !important;
}

.hire ul {
    margin: 100px 0 0 !important;
}

.work-request--information {
    flex-flow: row wrap;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    width: 100%;
    -webkit-box-pack: justify;
    -webkit-justify-content: space-between;
    -ms-flex-pack: justify;
    justify-content: space-between;
    margin-bottom: 60px
}

.work-request--information .information-name,
.work-request--information .information-email {
    position: relative;
    width: 45%;
    /* height: 50px; */
    font-size: 17px;
    font-weight: 300;
    margin: 10px;
}

.work-request--information input[type="text"],
.work-request--information input[type="email"] {
    width: 100%;
    padding: 0 0 5px 0;
    background-color: transparent;
    border: none;
    border-bottom: 1px solid #ff3d00;
    border-radius: 0
}

.work-request--information input[type="text"]:focus,
.work-request--information input[type="email"]:focus {
    outline: none;
    background-color: #0c0c0c
}

.work-request--information label {
    position: absolute;
    top: 0;
    left: 0;
    pointer-events: none;
    -webkit-transition: top .2s ease-in-out, font-size .2s ease-in-out;
    transition: top .2s ease-in-out, font-size .2s ease-in-out
}

.work-request--information input:focus+label,
.work-request--information input.has-value+label {
    top: -15px;
    font-size: 14px
}

@media (max-width: 767px) {
    .work-request--options {
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -webkit-flex-direction: row;
        -ms-flex-direction: row;
        flex-direction: row;
        -webkit-justify-content: space-around;
        -ms-flex-pack: distribute;
        justify-content: space-around
    }
    .work-request--options .options-a,
    .work-request--options .options-b {
        /* display: block;
        width: auto */
        display: -webkit-box;
        display: -webkit-flex;
        display: -ms-flexbox;
        display: flex;
        width: 90%;
        -webkit-box-pack: justify;
        -webkit-justify-content: space-between;
        -ms-flex-pack: justify;
        justify-content: space-between;
    }
}

@media (max-width: 600px) {
    .work-request--options {
        margin: 20px 0
    }
    .about--options>a {
        width: 107px !important;
        height: 110px !important;
    }
    .accordion .accordion-content p {
        font-size: 0.9rem !important;
    }
}

@media (max-width: 600px) and (max-width: 415px) {
    .work-request--options {
        -webkit-box-pack: justify;
        -webkit-justify-content: space-between;
        -ms-flex-pack: justify;
        justify-content: space-between;
        text-align: center;
    }
}

@media (max-width: 600px) {
    .work-request--options label {
        width: 48%;
        margin-bottom: 6px;
        font-size: 10px;
    }
    .work-request--options label:nth-child(6) {
        width: 100%;
    }
    /* .work-request--options .options-b label {
        line-height: 21px !important;
    } */
    .work-request--options input[type="checkbox"]:checked+label svg {
        width: 12px
    }
    .work-request--information {
        margin-bottom: 30px
    }
    .work-request--information .information-name,
    .work-request--information .information-email {
        height: 22px;
        font-size: 24px
    }
    .work-request--information .information-email input[type="text"] {
        padding: 0 0 15px 0;
    }
    .hire h2 {
        font-size: 21px !important;
    }
    .work-request--options p {
        font: caption !important;
    }
    .work-request input[type="submit"] {
        width: 70%;
    }
}

</style>
