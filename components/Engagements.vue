<template>
 <v-layout row wrap align-center>
          <v-flex xs12 md4>
            <div class="text-xs-center">
              <h4 class="inline"> Coder | Speaker</h4>
            </div>
          </v-flex>
          <v-flex xs12 md5 offset-md2>
            <div v-for="item in items" :key="item.title">
              <v-card class="my-3" hover>
                <v-card-media
                  class="white--text"
                  height="190px"
                  :src="item.imgUrl"
                >
          <v-container fill-height fluid>
            <v-layout fill-height>
              <v-flex xs6 align-start flexbox>
                <v-chip label class="indigo white--text">
                  <v-avatar>
                     <v-icon>{{item.icon}}</v-icon>
                  </v-avatar>
                  {{item.type}}
                </v-chip>
              </v-flex>
              <v-flex xs6 align-end flexbox>
                <span class="headline mb-0 inline-block">{{item.event}}</span>
              </v-flex>
            </v-layout>
          </v-container>
                </v-card-media>
                <v-card-text>
                  {{ item.title }}
                </v-card-text>
                <v-card-actions>
                  <v-btn icon class="red--text" :href="'http://reddit.com/submit?url=https://ThangNT.github.io/engagements/' + '&title=' + item.event +' '+ item.title">
                    <icon name="reddit-alien"></icon>
                  </v-btn>
                  <v-btn icon class="light-blue--text" :href="'https://twitter.com/share?url=https://ThangNT.github.io/engagements/'+'&via=ThangNT&text='+ item.event +' '+ item.title">
                    <icon name="twitter"></icon>
                  </v-btn>
                  <v-btn icon class="blue--text text--darken-3" :href="'http://www.facebook.com/sharer.php?'+'u=https://ThangNT.github.io/engagements/' +'&t=' + item.event +' '+ item.title">
                    <icon name="facebook-f"></icon>
                  </v-btn>
                  <v-spacer></v-spacer>
                  <v-btn flat class="orange--text" :href="item.link" target="_blank">Link</v-btn>
                </v-card-actions>
              </v-card>
            </div>
          </v-flex>
        </v-layout>
</template>

<script>
  export default {
    name: 'about',
    data () {
      return {
        items: [
        { title: '14.11.2017 / IBM Cloud - The growth platform for your business', event: 'Webinar enabling startups', link: 'https://bluemix.net/', type: 'talk', icon: 'mic', imgUrl: '/static/images/cards/docks.jpg' },
        { title: '11.11.2017 / Compositions and FSH: The next leap in Serverless Computing', event: 'Above Serverless and Beyond Containers', link: 'https://www.meetup.com/BlueCoders/events/244683579', type: 'talk', icon: 'mic', imgUrl: '/static/images/cards/docks.jpg' },
        { title: '27.10.2017 / Panel Discussion', event: 'Serverless Summit, Bangalore', link: 'http://inserverless.com/', type: 'talk', icon: 'mic', imgUrl: '/static/images/cards/serverless.png' },
        { title: '25.10.2017 / IBM Cloud - The growth platform for your business', event: 'Webinar enabling startups', link: 'https://bluemix.net/', type: 'talk', icon: 'mic', imgUrl: '/static/images/cards/docks.jpg' },
        { title: '10-13.10.2017 / 2 Talks and a lab covering Mobile & Cloud', event: 'IBM Cloud University, Berlin, Germany', link: 'http://conference.learnquest.com/CTU17/sessions/', type: 'talk', icon: 'mic', imgUrl: '/static/images/cards/plane.jpg' },
        { title: '5-6.10.2017 / Mobile and Serverless: an untold story', event: 'Mobile & Disruptive Summit, Bangalore', link: 'http://www.developermarch.com/mds/session.html?insert=Vidyasagar', type: 'talk', icon: 'mic', imgUrl: '/static/images/cards/mods.jpeg' },
        { title: 'An Android Chatbot powered by Watson with Speaker Diarization.', event: 'WatBot', link: 'https://github.com/ThangNT/WatBot', type: 'project', icon: 'code', imgUrl: '/static/images/cards/drop.jpg' },
        { title: 'Master the art of data science | Watson Machine Learning', event: 'BlueCoders Meetup, Bangalore', link: 'http://meetu.ps/c/2M8MP/sM1Rj/f', type: 'talk', icon: 'mic', imgUrl: '/static/images/cards/bluecoders_ml.jpeg' },
        { title: '1 Talk & 4 Hands-On Labs covering Cloud & Mobile', event: 'IBM Interconnect 2017 ,Las Vegas ,USA', link: 'https://myibm.ibm.com/events/interconnect/all-sessions', type: 'talk', icon: 'mic', imgUrl: '/static/images/cards/plane.jpg' },
        { title: 'My personal website built with Vue.JS as I am exploring it :) ', event: 'ThangNT', link: 'https://github.com/ThangNT/ThangNT.github.io', type: 'project', icon: 'code', imgUrl: '/static/images/cards/drop.jpg' },
        { title: 'My Contributions >>>>>', event: 'Older Engagements', link: 'https://vmacwrites.wordpress.com/about/my-contributions-to-developer-community/', type: 'talk', icon: 'mic' }
        ]
      }
    }
  }
</script>
<style>
.inline{
color: #66c0ec;
}
.inline-block{
background-color: #66c0ec;
display: inline-block;

}
</style>
