# vue-audio-play-controls

A Better Media Player for Vue.

This package is folked by [danstans/vue-audio-visualizer](https://github.com/danstans/vue-audio-visualizer)

<!-- # Demo -->

[Demo](https://vue-audio-play-controls.netlify.com/)

# Installation


## NPM or Yarn (recommended)

```shell
$ npm install --save vue-audio-play-controls
$ yarn add vue-audio-play-controls
```

### In your project

After installing via Yarn or NPM, use the following snippet in the script portion of the Vue component which you wish to render the Markdown.

```js
import Vue from 'vue'
import AudioPlayControls from 'vue-audio-play-controls'
Vue.use(AudioPlayControls)
...
```

### Browser globals

> The **dist** folder contains `vue-audio-play-controls.js`.

```html
<body>
  <div>
    <div class="content">
      This is where you put the rest of your site
    </div>
    <audio-play-controls
      avHeight="82px"
      :playlist="playlist"
    ></audio-play-controls>
  </div>
</body>
<script src="path/to/vue.js"></script>
<script src="path/to/vue-audio-play-controls.js"></script>
<script>
    Vue.use(AudioPlayControls);
    var vm = new Vue({
        el: "body"
    });
</script>
```

# Brief Use-case
```html
<template>
  <div id="app">
    <div class="content">
      This is where you put the rest of your site
    </div>
    <audio-play-controls
     avHeight="82px"
     :playlist="playlist"
     :canvas="true"
    ></audio-play-controls>
  </div>
</template>

<script>
export default {
  data () {
    return {
      playlist: [
        {
          audioName: 'Agnes',
          audioLive: '/static/agnes.mp3',
          authorName: 'Glass Animals',
          audioImg: 'https://pbs.twimg.com/profile_images/765322021060354048/0ppD4P6Y_400x400.jpg',
          audioDuration: '3:55'
        },
        {
          audioName: 'TaKillya (Baby Driver Soundtrack)',
          audioLive: '/static/takillya.mp3',
          authorName: 'Vinnie Maniscalco',
          audioImg: 'https://adamology.net/wp-content/uploads/2017/07/Baby-Driver.jpg',
          audioDuration: '3:46'
        },
        {
          audioName: 'Kipod',
          audioLive: '/static/kipod.mp3',
          authorName: 'Infected Mushrrom',
          audioImg: 'https://is4-ssl.mzstatic.com/image/thumb/Music/45/71/ff/mzi.mtqdovgf.jpg/1200x630bb.jpg',
          audioDuration: '5:48'
        },
        {
          audioName: 'Spitfire',
          audioLive: '/static/spitfire.mp3',
          authorName: 'Infected Mushrrom',
          audioImg: 'https://is4-ssl.mzstatic.com/image/thumb/Music/45/71/ff/mzi.mtqdovgf.jpg/1200x630bb.jpg',
          audioDuration: '7:15'
        }
      ]
    }
  }
}
</script>
```
# Props

| Prop | Type | Default | Describe |
| ---- | ---- | ------- | ------- |
| avHeight | String | '82px' | The size of the media player at the bottom of the page. |
| playlist | Array | `null` | The playlist data |
| canvas | Boolean | true | Enable/Disable the audio-visualizer component |


# License

Copyright (c) 2018 [danstans](https://github.com/danstans) by [MIT](https://opensource.org/licenses/MIT)
