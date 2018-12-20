<template>
 <div></div>
  <!-- <div class="bookNow main-section" v-if="sourceView" id="booknow">
      <h2 class="font-Flat title">{{sourceView.title.rendered}}</h2>


      <center v-html="sourceView.content.rendered"></center>

      <div v-if="this.$route.query.param || this.$route.query.param === 'zanzibar'" class="item">
        <div v-for="(item, index) in bookButtons" class="item" v-if="index == 2">
            <a :href="item.url_button   " target="_blank">
                <div class="signButton sign-green">
                    <div class="font-Flat" v-html="item.name_button"> -->
                        <!--{{item.name_button}}-->
                    <!-- </div>
                </div>
            </a>
        </div>
      </div>


      <div v-for="(item, index) in bookButtons" class="item" v-if="index < 2">
          <a :href="item.url_button" target="_blank">
              <div class="signButton sign-green">
                <div class="font-Flat" v-html="item.name_button"> -->
                    <!--{{item.name_button}}-->
                <!-- </div>
              </div>
        </a>
      </div>

      <div class="note font-Cae fluid-container bgGray" v-html="sourceView.acf.note">
      </div>
      <div class="sign">
        <div class="sign-arrow-light">
          <img src="/static/images/Flecha_3_off.png" alt="sign">
        </div>
      </div>
  </div> -->
</template>

<script>
    import Vue from 'vue';
    import {
        mapGetters
    } from 'vuex';
    // animations
    import {
        TweenMax,
        TimelineMax
    } from 'gsap';
    import ScrollMagic from 'scrollmagic';
    import AnimationPlugin from '../../node_modules/scrollmagic/scrollmagic/minified/plugins/animation.gsap.min.js';

    export default {
        name: 'BookNow',
        data() {
            return {
                sourceView: null,
                typePage: 'register_here',
                id: '1131',
                bookButtons:[]
            }
        },
        methods: {
            getData(typePage, id, lang) {
                return this.$http.get(Vue.config.source.ENDPOINT + typePage + '/' + id + '&lang=' + lang)
                    .then(response => {
                        this.sourceView = response.body;
                        this.getBookUrl();
                    }, response => {
                        console.log('Error', Error(response.message));
                    });
            },
            chargeInfo() {
                this.$emit('chargeInfo', this.checkerdata);
                this.checkerdata++;
            },
            getBookUrl() {

                this.bookButtons =  this.sourceView.acf.button;

                if(this.$route.query.param === 'zanzibar'){

                    for(var i = 0 ; i < this.bookButtons.length ; i ++){
                        this.bookButtons[i].url_button = this.bookButtons[i].url_button+'?param=zanzibar'+ '&lang=' + this.$store.state.lang;
                    }
                }else {
                    for(var i = 0 ; i < this.bookButtons.length ; i ++){
                        this.bookButtons[i].url_button = this.bookButtons[i].url_button+'?lang=' + this.$store.state.lang;
                    }

                }
            },
            animate() {
                const selector = '#booknow';

                TweenMax.to(selector + ' .sign > div', .7, {
                    x: '10px',
                    yoyo: true,
                    repeat: -1,
                    ease: Linear.easeNone
                });

                const SMController = new ScrollMagic.Controller();
                const tween = new TimelineMax()
                    .to(selector + ' .sign', .5, {
                        scale: 1,
                        x: 0,
                        force3D: true,
                        ease: Expo.easeOut
                    })
                    .staggerTo(selector + ' .item', 1.5, {
                        opacity: 1,
                        scale: 1,
                        delay: 0.5,
                        ease: Elastic.easeOut,
                        force3D: true
                    }, 0.2);

                let scene = new ScrollMagic.Scene({
                    triggerElement: selector
                });
                scene.setTween(tween);
                scene.addTo(SMController);
            }
        },
        created() {
            this.getData(this.typePage, this.id, this.$store.state.lang).then(function() {
                this.animate();
                this.chargeInfo();
            });
        }
       
    }
</script>

<style lang="scss">
</style>