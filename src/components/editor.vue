<template>
  <div id="vditor" name="description"></div>
</template>
<script>
import Vditor from "vditor";
import "vditor/dist/index.css";
export default {
  data() {
    return {
      contentEditor: "",
    };
  },
  mounted() {
      this.contentEditor = new Vditor('vditor', {
      toolbarConfig: {
        pin: true,
      },
      cache: {
        enable: false,
      },
      hint: {
        emoji: {
          pray: '🙏',
          broken_heart: '💔',
          ok_hand: '👌',
          smile: '😄',
          laughing: '😆',
          smirk: '😏',
          heart_eyes: '😍',
          grin: '😁',
          stuck_out_tongue: '😛',
          expressionless: '😑',
          unamused: '😒',
          sob: '😭',
          joy: '😂',
          tired_face: '😫',
          blush: '😊',
          cry: '😢',
          fearful: '😨'
        }
      },
      upload: {
        accept: 'image/*,.mp3, .wav, .rar',
        token: 'test',
        url: '/api/upload/editor',
        linkToImgUrl: '/api/upload/fetch',
        filename (name) {
          return name
        },
      },
      height: 360,
      counter: 65535,
      typewriterMode: true,
      after: () => {
        this.contentEditor.setValue('# hello, Vditor + Vue!')
      },
    }
    );

    },
  methods: {
      
  },
};
</script>