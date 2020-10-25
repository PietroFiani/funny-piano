<template>
  <div class="pianoContainer flex flex-col items-center m-0">
    <div class="emoji h-48 w-48">
      <div
        style="width: 100%; height: 0; padding-bottom: 100%; position: relative"
      >
        <iframe
          id="gif"
          src=""
          width="100%"
          height="100%"
          style="position: absolute"
          frameBorder="0"
          class="giphy-embed"
          allowFullScreen
        >
        </iframe>
      </div>
    </div>

    <div class="keys-container flex items-center relative">
      <!--Piano-->

      <div class="whitekeys flex">
        <!--Touches Blanches-->
        <span class="whitekey wk1">
          <svg whitekey
            width="69"
            height="252"
            viewBox="0 0 69 252"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path class="test"
              v-on:click="playWk('./assets/sounds/C.mp3')"
              v-on:mouseleave="removeColorWk()"
              d="M0 5C0 2.23857 2.23858 0 5 0H69V252H5C2.23858 252 0 249.761 0 247V5Z"
              fill="white"
            />
          </svg>
        </span>
        <span class="whitekey wk2">
          <svg
            width="69"
            height="252"
            viewBox="0 0 69 252"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect
              v-on:click="playWk('./assets/sounds/D.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorWk()"
              width="69"
              height="252"
              fill="white"
            />
          </svg>
        </span>
        <span class="whitekey wk3">
          <svg
            width="69"
            height="252"
            viewBox="0 0 69 252"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect
              v-on:click="playWk('./assets/sounds/E.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorWk()"
              width="69"
              height="252"
              fill="white"
            />
          </svg>
        </span>
        <span class="whitekey wk4">
          <svg
            width="69"
            height="252"
            viewBox="0 0 69 252"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect
              v-on:click="playWk('./assets/sounds/F.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorWk()"
              width="69"
              height="252"
              fill="white"
            />
          </svg>
        </span>
        <span class="whitekey wk4">
          <svg
            width="69"
            height="252"
            viewBox="0 0 69 252"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect
              v-on:click="playWk('./assets/sounds/G.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorWk()"
              width="69"
              height="252"
              fill="white"
            />
          </svg>
        </span>
        <span class="whitekey wk6">
          <svg
            width="69"
            height="252"
            viewBox="0 0 69 252"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect
              v-on:click="playWk('./assets/sounds/A.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorWk()"
              width="69"
              height="252"
              fill="white"
            />
          </svg>
        </span>
        <span class="">
          <svg
            width="69"
            height="252"
            viewBox="0 0 69 252"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              v-on:click="playWk('./assets/sounds/B.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorWk()"
              d="M0 0H64C66.7614 0 69 2.23858 69 5V247C69 249.761 66.7614 252 64 252H0V0Z"
              fill="white"
            />
          </svg>
        </span>
      </div>

      <div class="blackkeys flex absolute">
        <!--Touches Noires-->
        <span class="blackkey bk1">
          <svg
            width="30"
            height="184"
            viewBox="0 0 30 184"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              v-on:click="playBk('./assets/sounds/C%23.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorBk()"
              d="M0 0H30V179C30 181.761 27.7614 184 25 184H5C2.23858 184 0 181.761 0 179V0Z"
              fill="black"
            />
          </svg>
        </span>
        <span class="blackkey bk2">
          <svg
            width="30"
            height="184"
            viewBox="0 0 30 184"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              v-on:click="playBk('./assets/sounds/D%23.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorBk()"
              d="M0 0H30V179C30 181.761 27.7614 184 25 184H5C2.23858 184 0 181.761 0 179V0Z"
              fill="black"
            />
          </svg>
        </span>
        <span class="blackkey bk3">
          <svg
            width="30"
            height="184"
            viewBox="0 0 30 184"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              v-on:click="playBk('./assets/sounds/F%23.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorBk()"
              d="M0 0H30V179C30 181.761 27.7614 184 25 184H5C2.23858 184 0 181.761 0 179V0Z"
              fill="black"
            />
          </svg>
        </span>
        <span class="blackkey bk4">
          <svg
            width="30"
            height="184"
            viewBox="0 0 30 184"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              v-on:click="playBk('./assets/sounds/G%23.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorBk()"
              d="M0 0H30V179C30 181.761 27.7614 184 25 184H5C2.23858 184 0 181.761 0 179V0Z"
              fill="black"
            />
          </svg>
        </span>
        <span class="blackkey bk5">
          <svg
            width="30"
            height="184"
            viewBox="0 0 30 184"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              v-on:click="playBk('./assets/sounds/A%23.mp3'), emojiDisplay()"
              v-on:mouseleave="removeColorBk()"
              d="M0 0H30V179C30 181.761 27.7614 184 25 184H5C2.23858 184 0 181.761 0 179V0Z"
              fill="black"
            />
          </svg>
        </span>
      </div>
    </div>

    <div class="note-text flex relative">
      <span class="do note">DO</span>
      <span class="re note">RÉ</span>
      <span class="mi note">MI</span>
      <span class="fa note">FA</span>
      <span class="sol note">SOL</span>
      <span class="la note">LA</span>
      <span class="si note">SI</span>
    </div>
  </div>
</template>

<script>
import { GiphyFetch } from "@giphy/js-fetch-api";

export default {
  name: "VPiano",
  components: {},
  mounted() {},
  methods: {
    playBk(sound) {
      const audio = document.createElement("audio"); // crée la div audio au click
      audio.src = sound;
      event.target.classList.add("bkColorChange");
      audio.play();
    },

    playWk(sound) {
      const audio = document.createElement("audio"); // crée la div audio au click
      audio.src = sound;
      event.target.classList.add("wkColorChange");
      audio.play();
    },

    removeColorBk() {
      event.target.classList.remove("bkColorChange");
    },

    removeColorWk() {
      event.target.classList.remove("wkColorChange");
    },

    async emojiDisplay() {
      const gf = new GiphyFetch("oVaWWqzGhsHRIGtsD8eTiR7s5bNkQjF9");
      let randomIndice = Math.floor(Math.random() * 50);
      try {
        const result = await gf.emoji({ limit: 50 });
        const embedUrl = result.data[randomIndice].embed_url;
        const container = document.querySelector("#gif");
        container.src = embedUrl;
        console.log(`gif`, embedUrl, container);
      } catch (error) {
        console.error(`gif`, error);
      }
    },
  },
};
</script>

<style lang="postcss" scoped>
@import url("https://fonts.googleapis.com/css2?family=PT+Mono&display=swap");

.emoji {
  margin: 10px;
}
.keys-container {
  border: solid black 8px;
  border-radius: 14px;
}

.wk-svg {
  width: 69px;
  height: 252px;
}
.whitekey {
  margin: 0px;
  padding: 0px;
  border-right: black solid 2px;
}
.blackkey {
  position: relative;
  bottom: 2.15em;
}

.bk1 {
  left: 3.5em;
}
.bk2 {
  left: 6em;
}
.bk3 {
  left: 13em;
}
.bk4 {
  left: 15.6em;
}
.bk5 {
  left: 18.15em;
}
.note-text {
  padding-right: 18px;
  padding-top: 48px;
}
.note {
  position: absolute;
  font-family: "PT Mono", monospace;
  font-weight: 400;
  color: rgba(255, 255, 255, 40%);
}
.do {
  right: 13.2em;
}
.re {
  right: 9em;
}
.mi {
  right: 4.5em;
}
.fa {
}
.sol {
  left: 4.1em;
}
.la {
  left: 8.9em;
}
.si {
  left: 13.4em;
}

.bkColorChange {
  fill: rgba(229, 1, 111, 1);
}
.wkColorChange {
  fill: rgba(255, 209, 45, 1);
}
</style>
