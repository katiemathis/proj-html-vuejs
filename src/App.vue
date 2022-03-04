<template>
  <div id="app">
    <MyHeader :navMenuItems="navMenuItems"/>
    <MyMain />
    <MyFooter :popularTopics="popularTopics" :recentTopics="recentTopics" :latestReplies="latestReplies"/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import MyFooter from './components/MyFooter.vue'

export default {
  name: 'App',
  components: {
    //HelloWorld
    MyHeader,
    MyMain,
    MyFooter
  },
  data () {
    return {
        navMenuItems: ['Home', 'Apple', 
        'Microsoft', 'Android', 'Forums', 'Contact Us', 
        ],
        popularTopics: [
                  'Here is a popular topic for you right here',
                  'Here is another popular topic. Cool, right?',
                  'What about this popular topic. Check it out.',
                  'Last popular topic',

        ],
        recentTopics: [
                'This topic is so hot right now.',
                'Here is another recent topic that you should know about',
                'Topic - fresh off the presses',
                'Everyone is talking about this thing right now',

        ],
        latestReplies: [
                'This just in - someone replied',
                'Someone is saying something about this thing',
                'Someone else is saying something else about this other thing',
                'The very latest reply',
        ]

    }
  }
}
</script>

<style>

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Source Sans Pro', sans-serif;
}

</style>
