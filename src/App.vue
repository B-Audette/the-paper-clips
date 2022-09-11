<template>
  <q-layout view="lHh lpr lFf">
    <q-header class="q-py-sm" style="background-color: #1c1b21;" :style="'border-bottom: 2px solid '+ theme_color" id="id_home">
        <q-toolbar>
        <span :style="'font-size: 35px;color:'+theme_color" class="pricedown-font text-h6 q-mr-md">The Paper Clips</span>
        <q-space ></q-space>
      <q-tabs v-model="selected_tab" shrink>
        <q-tab :style= "[selected_tab == 't_0' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_home');" style="width:120px;min-height:auto !important;color: white" label="Home" />
                <q-tab :style= "[selected_tab == 't_4' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_about_us');" style="width:120px;min-height:auto !important;color: white" label="About Us" />
        <q-tab :style= "[selected_tab == 't_1' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_media');" style="width:120px;min-height:auto !important;color: white" label="Media" />
        <q-tab :style= "[selected_tab == 't_5' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_events');" style="width:120px;min-height:auto !important;color: white" label="Events" />
        <q-tab :style= "[selected_tab == 't_2' ? {backgroundColor: theme_color} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_contact_us');" style="width:120px;min-height:auto !important;color: white" label="Connect" />

 
      </q-tabs>
        
      </q-toolbar>
    </q-header>
    <q-page-container>
      <q-page>
   <q-carousel
          v-model="slide"
          arrows
          swipeable
          navigation
          infinite
          control-color="white"
          transition-prev="slide-right"
          transition-next="slide-left"
          height="800px"
        >
     <q-carousel-slide class="q-pa-none" :name="1" img-src="./statics/images/paperclips_mob1.jpg">
<div class="full-height full-width flex flex-center" style="background-color: rgba(0, 0, 0, 0.68) !important;">
            <div class="custom-caption">
              <div class="text-h2 main_line animation_2" :style="'color:'+theme_color">The Paper Clips</div><br><br>
              <div class="text-h4">Motown Trombone Sound</div><br><br>
<div class="animation_2">
  <div class ="q-mx-xl text-h6">The Paper Clips are a Twin-Cities-based quartet combining the excitement of the Motown sound and beyond with the power of trombone ensemble. Founded in 2019, we bring enthusiastic and moving performances to audiences and educational settings with fresh arrangements of classic hits.</div>
</div>
            </div>
</div>
          </q-carousel-slide>
          <q-carousel-slide class="q-pa-none" :name="2" img-src="./statics/images/paperclipbackdrop.jpg">
<div class="full-height full-width flex felx-center" style="background-color: rgba(0, 0, 0, 0.68) !important;">
            <div class="custom-caption">
    	      <br><br><br><br><br><br><div class="q-mt-xl text-h4 " style="font-size:42px;"><span :style="'color:'+theme_color">We are 2022-2023 MPR Class Notes Artists</span></div><br>
              <div class="q-mx-xl text-h6">We are excited to be bringing our unique educational program to student audiences across Minnesota for a second season! <br></div><br>
              <q-btn size="md" :style="'background:'+ theme_color +'; color: white'" label="LEARN MORE" type="a" href="https://www.yourclassical.org/story/2022/06/14/class-notes-concerts-202223-artist-menu"/><br>
              <div class="q-mt-md q-mx-xl text-h6">Recognizing that it is an honor to perform Black American popular music as white people, we are dedicating 10% of our proceeds from each gig to two local music school Walker West, to encourage music education in under-served communities and perserve Black cultural heritage.</div><br><br>
<div class="animation_2">

</div>
            </div>
</div>
          </q-carousel-slide>
        </q-carousel>
  <div class="row" id="id_about_us">
           <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
              <h3 class="text-center">About Us
                <br>
              </h3>
            </div>
    <div class="q-pa-lg q-gutter-md fit row wrap justify-center items-center content-center">
 
      <q-card class="my-card" style="order: 1">
      <img src="./statics/images/paperclips_ben.jpg">
        <q-card-section>
          <div class="text-h6">Ben Bussey</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <q-toolbar class="flex flex-center text-white" style="background-color: #ffffff;" :style="'border-top: 2px solid '+ theme_color">
           <div class="q-pa-sm q-gutter-sm">
	    <q-btn round type="a" href="https://www.facebook.com/ben.busbus"
                     :style="'background:'+ theme_color +'; color: white !important;'" icon="fab fa-facebook" />
                     	    <q-btn round type="a" href="https://www.instagram.com/benbusbus/"
                     :style="'background:'+ theme_color +'; color: white !important;'" glossy text-color="black" icon="fab fa-instagram" />
            <q-btn round type="a" href="https://www.tromboneben.com"
                     :style="'background:'+ theme_color +'; color: white !important;'" icon="web" />

	  </div>
        </q-toolbar>
        <!-- <a href="https://www.tromboneben.com" style="  color: #ef6c00;
  text-decoration: none;">tromboneben.com</a> -->
        </q-card-section>
      </q-card>


      <q-card class="my-card" style="order: 4">
      <img src="./statics/images/paperclips_brooke.jpg">
        <q-card-section>
          <div class="text-h6">Brooklynne Audette</div>
        </q-card-section>
          <q-card-section class="q-pt-none">
                       <q-toolbar class="flex flex-center text-white" style="background-color: #ffffff;" :style="'border-top: 2px solid '+ theme_color">
           <div class="q-pa-sm q-gutter-sm">
             <q-btn round type="a" href="https://www.facebook.com/Brooklynne.Audette/"
                     :style="'background:'+ theme_color +'; color: white !important;'" icon="fab fa-facebook" />
             <q-btn round type="a" href="https://www.instagram.com/brooklynneposaune/"
                     :style="'background:'+ theme_color +'; color: white !important;'" glossy text-color="black" icon="fab fa-instagram" />
                     </div>
                     </q-toolbar>
          </q-card-section>
        </q-card>

          <q-card class="my-card" style="order: 2">
      <img src="./statics/images/paperclips_lauren.jpg">
        <q-card-section>
          <div class="text-h6">Lauren Husting</div>
        </q-card-section>
          <q-card-section class="q-pt-none">
                      <q-toolbar class="flex flex-center text-white" style="background-color: #ffffff;" :style="'border-top: 2px solid '+ theme_color">
           <div class="q-pa-sm q-gutter-sm">
              <q-btn round type="a" href="https://www.instagram.com/laurenhusting/"
                     :style="'background:'+ theme_color +'; color: white !important;'" glossy text-color="black" icon="fab fa-instagram" />
              <q-btn round type="a" href="https://www.laurenhusting.com"
                     :style="'background:'+ theme_color +'; color: white !important;'" icon="web" />
                     </div>
                     </q-toolbar>
          </q-card-section>
        </q-card>

          <q-card class="my-card" style="order: 3">
      <img src="./statics/images/paperclips_chris.jpg">
        <q-card-section>
          <div class="text-h6">Chris Allen</div>
        </q-card-section>
          <q-card-section class="q-pt-none">
                      <q-toolbar class="flex flex-center text-white" style="background-color: #ffffff;" :style="'border-top: 2px solid '+ theme_color">
           <div class="q-pa-sm q-gutter-sm">
             <q-btn round type="a" href="https://www.facebook.com/cdallen"
                     :style="'background:'+ theme_color +'; color: white !important;'" icon="fab fa-facebook" />
              <q-btn round type="a" href="https://www.basstrombonechris.com"
                     :style="'background:'+ theme_color +'; color: white !important;'" icon="web" />
                     </div>
                     </q-toolbar>
          </q-card-section>
        </q-card>

      </div>
    </div>


        
          <div class="row" id="id_media">
          <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
            <h3 class="text-center">Media
              <br>
            
            </h3>
          </div>
        </div>
        <div class="row text-center flex flex-center">
          <div class="col-md-12 col-lg-12 col-sx-12 col-sm-12 q-gutter-md flex flex-center">
            <div class="col-md-4 col-lg-4 col-sx-12 col-sm-12">
                <iframe height="325px" width="480" src="https://www.youtube.com/embed/kZa7IS3Lgjw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
          </div>
        </div>
        <br>
        <br>      
        <div class="pricing" id="id_events">
          <div class="" style="background-color: #000000ad !important;">
            <div class="column">
              <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
                <h3 class="text-center text-white">Events 2022-2023
                  <br>
                  <span
                    class="q-mx-xl text-center text-grey text-h6">Come hear us at one of our public performances! We will update as we add events throughout the season.</span>
                </h3>
              </div>
            </div> 
            <div class="q-pa-lg q-gutter-md column">
              <q-list bordered padding class="rounded-borders" style="max-width: 500px">

      <q-item>
        <q-item-section avatar top>
               <q-avatar icon="queue_music" color="secondary" text-color="white" size="50px" />
        </q-item-section>

        <q-item-section top class="col-2 gt-sm">
          <q-item-label class="q-mt-sm" style="color: #ffffff" >Fridays in the Valley</q-item-label>
        </q-item-section>

        <q-item-section top>
          <q-item-label lines="1">
            <span class="text-weight-medium" style="color: #ffffff">Valley Community Presbyterian Church</span>
          </q-item-label>
           <q-item-label style="color: #ffffff" caption>October 14th, 2022 - 7:00PM-8:00PM</q-item-label>
                        <q-item-label style="color: #ffffff" caption></q-item-label>
         
          <q-item-label lines="1" class="q-mt-xs text-body2 text-weight-bold text-primary text-uppercase" style="color: #ffffff">
            <a style="color: #5c9fd6; text-decoration: none;" href="https://www.valleychurch.net/events">More Info</a>
          </q-item-label>
        </q-item-section>

        <q-item-section top side>
          <div class="text-grey-8 q-gutter-xs">
            <q-btn class="gt-xs" color="secondary" size="20px" flat dense round icon="directions" type="a"  href="https://goo.gl/maps/njr8d2SuAkm5LiG67" />
      
          </div>
        </q-item-section>
      </q-item>

      <q-separator spaced />
       <q-item>
                 <q-item-section avatar top>
               <q-avatar icon="queue_music" color="secondary" text-color="white" size="50px" />
        </q-item-section>
      <q-item-section top class="col-2 gt-sm">
          <q-item-label class="q-mt-sm" style="color: #ffffff">Schmitt Music</q-item-label>
        </q-item-section>

        <q-item-section top>
          <q-item-label lines="1">
            <span class="text-weight-medium" style="color: #ffffff">Schmitt Music West Bloomington</span>
          </q-item-label>
           <q-item-label style="color: #ffffff" caption>November 5th, 2022 - 12:00PM-1:00PM</q-item-label>
                        <q-item-label style="color: #ffffff" caption></q-item-label>
         
          <q-item-label lines="1" class="q-mt-xs text-body2 text-weight-bold text-primary text-uppercase" style="color: #ffffff">
            <a style="color: #5c9fd6; text-decoration: none;" href="https://www.schmittmusic.com/moving-to-bloomington/">More Info</a>
          </q-item-label>
        </q-item-section>

        <q-item-section top side>
          <div class="text-grey-8 q-gutter-xs">
            <!-- <q-btn class="gt-xs" color="secondary" size="20px" flat dense round icon="map" type="a" /> //waiting on address-->
      
          </div>
        </q-item-section>
   </q-item>
    <q-separator spaced />
       <q-item>
                 <q-item-section avatar top>
               <q-avatar icon="queue_music" color="secondary" text-color="white" size="50px" />
        </q-item-section>
      <q-item-section top class="col-2 gt-sm">
          <q-item-label class="q-mt-sm" style="color: #ffffff" >SPCM Coffee Concert</q-item-label>
        </q-item-section>

        <q-item-section top>
          <q-item-label lines="1">
            <span class="text-weight-medium" style="color: #ffffff">Saint Paul Conservatory of Music</span>
          </q-item-label>
           <q-item-label style="color: #ffffff" caption>December 7th, 2022 - 12:00PM-1:00PM</q-item-label>
                        <q-item-label style="color: #ffffff" caption></q-item-label>
         
          <q-item-label lines="1" class="q-mt-xs text-body2 text-weight-bold text-primary text-uppercase" style="color: #ffffff">
            <a style="color: #5c9fd6; text-decoration: none;" href="https://thespcm.org/events">More Info</a>
          </q-item-label>
        </q-item-section>

        <q-item-section top side>
          <div class="text-grey-8 q-gutter-xs">
            <q-btn class="gt-xs" color="secondary" size="20px" flat dense round icon="directions" type="a"  href="  https://goo.gl/maps/C2MsV3anRyTjRDoB7" />
          </div>
        </q-item-section>
   </q-item>
              </q-list>
            </div>
          </div>
        </div>

     


<div class="contact_us" id="id_contact_us">
  <div style="background-color: #000000ad !important;">
    <div class="row" id="id_news">
      <div class="col-md-12 col-lg-12 col-xs-12 col-sm-12">
        <h3 class="text-center text-white">Contact Us
          <br>
            <span
              class="text-center text-grey text-h6">Have questions? You can reach us through our socials or email!</span>
        </h3>
      </div>
    </div>
  <div class="row text-center flex flex-center q-pb-lg">
</div>
</div>

</div>
        <q-toolbar class="flex flex-center text-white" style="background-color: #1c1b21;" :style="'border-top: 2px solid '+ theme_color">
           <div class="q-pa-sm q-gutter-sm">
	    <q-btn round type="a" href="https://www.facebook.com/paperclipstrombonequartet"
                     :style="'background:'+ theme_color +'; color: white !important;'" icon="fab fa-facebook" size="20px" />
            <q-btn round type="a" href="mailto:thepaperclipstrombones@gmail.com"
                     :style="'background:'+ theme_color +'; color: white !important;'" icon="email" size="20px"/>
	    <q-btn round type="a" href="https://www.instagram.com/the_paper_clips/"
                     :style="'background:'+ theme_color +'; color: white !important;'" glossy text-color="black" icon="fab fa-instagram" size="20px"/>
	  </div>
        </q-toolbar>

      </q-page>
    </q-page-container>
  </q-layout>
</template>


<script>
  import { scroll } from 'quasar'
  const { getScrollTarget, setScrollPosition } = scroll


    export default {

        data() {
            return {
                slide: 1,
		            review_slide: 'style',
                selected_tab: 't_0',
                team_slide: 1,
                bg_color: 'rgb(0, 163, 82)',
                hover: false,
                active: false,
                theme_color: '#ef6c00',
                background_style: 'background-color:rgba(0, 163, 82, 0.7);',
                about_heading_1: [],
                about_heading_2: [],
                about_heading_3: [],
                about_heading_color_1: '#424242',
                about_heading_color_2: '#424242',
                about_heading_color_3: '#424242'
            }
        },
        computed: {
            style() {
                return {
                    width: '340px',
                    height: '263px',
                    backgroundImage: `./statics/images/paperclipbackdrop.jpg`, // eslint-disable-line
                    textAlign: 'center',
                    boxShadow: '1px 1px 2px #e6e6e6',
                    display: 'inline-block'
                }
            },
            team_style() {
                return {
                    width: '260px',
                    height: '263px',
                    backgroundImage: `./statics/images/paperclipbackdrop.jpg`, // eslint-disable-line
                    textAlign: 'center',
                    boxShadow: '1px 1px 2px #e6e6e6',
                    display: 'inline-block'
                }
            }
        },
        methods: {
          scrollToElement (id) {
            let el = document.getElementById(id)
            const target = getScrollTarget(el)
            const offset = el.offsetTop + 3
            const duration = 900
            setScrollPosition(target, offset, duration)
          },
            changeBgColor() {
                this.theme_color = this.bg_color;
                this.background_style = 'background-color:' + this.bg_color.split(')')[0] + ',0.7)';
            },
            hoverOver: function(index) {
              this['about_heading_color_' + index] = this.theme_color;
              this['about_heading_' + index] = ['animated', 'bounceIn'];              
            },
            hoverOutTimeout: function(index) {
              this['about_heading_color_' + index] = '#424242';
              setTimeout(() => {
                this['about_heading_' + index] = [];                
              }, 1000);              
            },
        }
    }
</script>

<style lang="sass" scoped>

    .main_line
      font-size: 75px
      letter-spacing: 5px
      line-height: 60px
      font-weight: 600

    .custom-caption
      text-align: center
      padding: 12px
      color: white

    .animation_1
      -webkit-animation: bounceIn 1s ease-in 800ms both
      animation: bounceIn 1s ease-in 800ms both

    .animation_2
      -webkit-animation: flipInX 2s ease-in-out 800ms both
      animation: flipInX 1s ease-in-out 800ms both

    .animation_3
      -webkit-animation: lightSpeedIn 1s ease-in 800ms both
      animation: lightSpeedIn 1s ease-in 800ms both

    .description
      padding: 10px
      background-color: black
      color: white
      box-shadow: 1px 1px 2px #e6e6e6

    .my-header
      width: 200px
      top: 0
      height: 45px
      color: black
      background-color: rgba(255,255,255, 0.8)
      text-transform: uppercase
      text-align: center
      font-size: 17px
      margin: 20px 0 0 68px
      padding: 25px

    .my-text
      width: 100%
      top: 0
      height: 90px
      color: white
      text-align: center
      font-size: 15px
      margin: 79px 0 0 0
      padding: 20px
      line-height: normal
      font-family: Georgia, serif
      font-style: italic

    .my-button-container
      width: 100%

    .my-button
      text-decoration: none
      text-transform: uppercase
      margin: 0 0 20px 0
      text-align: center
      padding: 7px 14px
      background-color: #000
      color: #fff
      text-transform: uppercase
      box-shadow: 0 0 1px #000
      transition-delay: 0.2s

    .my-button:hover
      box-shadow: 0 0 5px #000

    .box-shadow:hover
      box-shadow: 0 10px 13px -6px rgba(0, 0, 0, 0.2), 0 20px 31px 3px rgba(0, 0, 0, 0.14), 0 8px 38px 7px rgba(0, 0, 0, 0.12) !important

    .my-card
      max-width: 250px
      margin-top: 10px

    .team-header
      width: 100%
      top: 0
      height: 45px
      color: white
      text-transform: uppercase
      text-align: center
      font-size: 17px
      margin: 60px 0 0 0
      padding: 12px

    .team-text
      width: 100%
      top: 0
      height: 90px
      color: white
      text-align: center
      font-size: 15px
      margin: 100px 0 0 0
      padding: 20px
      line-height: normal
      font-family: Georgia, serif
      font-style: italic
    
    // .quote
    //   background: url(./statics/images/paperclipbackdrop.jpg)
    //   background-size: cover
    //   background-position: center
    //   background-attachment: fixed
    //   background-repeat: no-repeat
    
    .pricing
      background: url(./statics/images/paperclipbackdrop.jpg)
      background-size: cover
      background-position: center
      background-attachment: fixed
      background-repeat: no-repeat
    
    .contact_us
      background: url(./statics/images/paperclipbackdrop.jpg)
      background-size: cover
      background-position: center
      background-attachment: fixed
      background-repeat: no-repeat
    
    .custom_tab
      width: 130px
</style>

