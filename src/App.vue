<template>
  <div id="app">
    <header>
      <img
        style="margin: 30px 0 13px 0; width: 200px"
        src="https://www.bild-studio.com/wp-content/uploads/2023/03/logo_veliki.png"
        alt="logo"
      />
    </header>
    <div :class="[info ? 'showInfo' : '', 'form']">
      <div class="showInfo-title">
        <h2>Your Info</h2>
        <svg
          @click="showInfo(false)"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          viewBox="0,0,256,256"
          width="24px"
          height="24px"
          fill-rule="nonzero"
        >
          <g
            fill="none"
            fill-rule="nonzero"
            stroke="none"
            stroke-width="none"
            stroke-linecap="none"
            stroke-linejoin="none"
            stroke-miterlimit="10"
            stroke-dasharray=""
            stroke-dashoffset="0"
            font-family="none"
            font-weight="none"
            font-size="none"
            text-anchor="none"
            style="mix-blend-mode: normal"
          >
            <g transform="scale(5.33333,5.33333)">
              <path
                d="M44,17l-5,-5c-0.8,-0.8 -2,-0.8 -2.8,0l-8.2,8.2l-8.2,-8.2c-0.8,-0.8 -2,-0.8 -2.8,0l-5,5c-0.8,0.8 -0.8,2 0,2.8l8.2,8.2l-8.2,8.2c-0.8,0.8 -0.8,2 0,2.8l5,5c0.8,0.8 2,0.8 2.8,0l8.2,-8.2l8.2,8.2c0.8,0.8 2,0.8 2.8,0l5,-5c0.8,-0.8 0.8,-2 0,-2.8l-8.2,-8.2l8.2,-8.2c0.8,-0.8 0.8,-2 0,-2.8z"
                fill="#1ee697"
                stroke="none"
                stroke-width="1"
                stroke-linecap="butt"
                stroke-linejoin="miter"
              />
              <path
                d="M11.7,28.5l-3.7,3.7c-0.8,0.8 -0.8,2 0,2.8l5,5c0.8,0.8 2,0.8 2.8,0l8.2,-8.2l8.2,8.2c0.8,0.8 2,0.8 2.8,0l5,-5c0.8,-0.8 0.8,-2 0,-2.8l-8.2,-8.2l8.2,-8.2c0.8,-0.8 0.8,-2 0,-2.8l-2.6,-2.6"
                fill="none"
                stroke="#18193f"
                stroke-width="3"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M33.1,7.1l-9.1,9.1l-8.2,-8.2c-0.8,-0.8 -2,-0.8 -2.8,0l-5,5c-0.8,0.8 -0.8,2 0,2.8l8.2,8.2"
                fill="none"
                stroke="#18193f"
                stroke-width="3"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </g>
          </g>
        </svg>
      </div>
      <div class="form-input">
        <label>Name</label>
        <input v-model="name" type="text" placeholder="Your name" />
      </div>
      <div class="form-input">
        <label>Position</label>
        <input v-model="position" type="text" placeholder="Your position" />
      </div>
      <div class="form-input">
        <label>Mobile number</label>
        <input v-model="number" type="text" placeholder="Your number" />
      </div>
      <div class="form-input">
        <label>Office number</label>
        <input v-model="office" type="text" placeholder="Your number" />
      </div>
    </div>
    <div :class="[instructions ? 'showInfo' : '', 'form']">
      <div class="showInfo-title">
        <h2>Instructions</h2>
        <svg
          @click="showInstructions(false)"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          viewBox="0,0,256,256"
          width="24px"
          height="24px"
          fill-rule="nonzero"
        >
          <g
            fill="none"
            fill-rule="nonzero"
            stroke="none"
            stroke-width="none"
            stroke-linecap="none"
            stroke-linejoin="none"
            stroke-miterlimit="10"
            stroke-dasharray=""
            stroke-dashoffset="0"
            font-family="none"
            font-weight="none"
            font-size="none"
            text-anchor="none"
            style="mix-blend-mode: normal"
          >
            <g transform="scale(5.33333,5.33333)">
              <path
                d="M44,17l-5,-5c-0.8,-0.8 -2,-0.8 -2.8,0l-8.2,8.2l-8.2,-8.2c-0.8,-0.8 -2,-0.8 -2.8,0l-5,5c-0.8,0.8 -0.8,2 0,2.8l8.2,8.2l-8.2,8.2c-0.8,0.8 -0.8,2 0,2.8l5,5c0.8,0.8 2,0.8 2.8,0l8.2,-8.2l8.2,8.2c0.8,0.8 2,0.8 2.8,0l5,-5c0.8,-0.8 0.8,-2 0,-2.8l-8.2,-8.2l8.2,-8.2c0.8,-0.8 0.8,-2 0,-2.8z"
                fill="#1ee697"
                stroke="none"
                stroke-width="1"
                stroke-linecap="butt"
                stroke-linejoin="miter"
              />
              <path
                d="M11.7,28.5l-3.7,3.7c-0.8,0.8 -0.8,2 0,2.8l5,5c0.8,0.8 2,0.8 2.8,0l8.2,-8.2l8.2,8.2c0.8,0.8 2,0.8 2.8,0l5,-5c0.8,-0.8 0.8,-2 0,-2.8l-8.2,-8.2l8.2,-8.2c0.8,-0.8 0.8,-2 0,-2.8l-2.6,-2.6"
                fill="none"
                stroke="#18193f"
                stroke-width="3"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M33.1,7.1l-9.1,9.1l-8.2,-8.2c-0.8,-0.8 -2,-0.8 -2.8,0l-5,5c-0.8,0.8 -0.8,2 0,2.8l8.2,8.2"
                fill="none"
                stroke="#18193f"
                stroke-width="3"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </g>
          </g>
        </svg>
      </div>
      <div class="instructions-data">
        <ul>
          <li>Select edit and enter your data.</li>
          <li>Press 'Copy Signature'.</li>
          <li>Open your Gmail account on your computer.</li>
          <li>
            Click on the gear icon in the upper-right corner of your screen.
          </li>
          <li>Select "See all settings" from the dropdown menu.</li>
          <li>Scroll down to the "Signature" section.</li>
          <li>Click on the "Create new" button to create a new signature.</li>
          <li>Enter a name for your signature and click "Create".</li>
          <li>In the text box, paste your HTML code for the signature.</li>
          <li>
            If the signature looks good, select the signature from the drop-down
            menu under "For new emails use" to add it to all new emails you
            compose in Gmail.
          </li>
          <li>
            If you want to add the signature to all replies and forwards as
            well, select the signature from the drop-down menu under "On
            reply/forward" as well.
          </li>
          <li>
            Once you're done, scroll to the bottom of the page and click "Save
            Changes".
          </li>
        </ul>
      </div>
    </div>
    <div class="cards">
      <div class="preview-edit" @click="showInfo(true)">Edit</div>
      <div class="preview-instructions" @click="showInstructions(true)">
        How to use?
      </div>

      <div :class="[isCopied ? 'open' : '', 'preview-copied']">
        Successfully copied!
      </div>
      <div class="preview">
        <br/>
        <div ref="content">
          <h1
            style="
              font-family: 'Roboto', sans-serif;
              font-size: 19px;
              line-height: 28px;
              font-weight: 700;
              color: #000;
              margin: 0;
            "
          >
            {{ name }}
          </h1>
          <p
            style="
              font-family: 'Roboto', sans-serif;
              font-size: 13px;
              line-height: 20px;
              font-weight: 400;
              color: #000;
              margin: 0;
            "
          >
            {{ position }}
          </p>
          <div
            style="width: 20px; border-top: 1px solid #000; margin: 24px 0 22px"
          ></div>
          <p
            v-if="number.length"
            style="
              font-family: 'Roboto', sans-serif;
              font-size: 13px;
              line-height: 20px;
              font-weight: 400;
              color: #000;
              margin: 0;
            "
          >
            mob: {{ number }}
          </p>
          <p
            v-if="office.length"
            style="
              font-family: 'Roboto', sans-serif;
              font-size: 13px;
              line-height: 20px;
              font-weight: 400;
              color: #000;
              margin: 0;
            "
          >
            office: {{ office }}
          </p>
          <p
            style="
              font-family: 'Roboto', sans-serif;
              font-size: 13px;
              line-height: 20px;
              font-weight: 400;
              color: #000;
              margin: 0 0 13px 0;
            "
          >
            web: www.bild-studio.com
          </p>
          <img id="big-img" style="width: 100px;" src="https://www.bild-studio.com/wp-content/uploads/2023/03/logo_veliki.png" alt="logo" />
          <p
            style="
              font-family: 'Roboto', sans-serif;
              font-size: 11px;
              line-height: 15px;
              font-weight: 400;
              color: #999999;
              margin: 10px 0 0 0;
            "
          >
            Think about the planet and give your contribution to the
            sustainability.
          </p>
          <p
            style="
              font-family: 'Roboto', sans-serif;
              font-size: 11px;
              line-height: 15px;
              font-weight: 400;
              color: #999999;
              margin: 0;
            "
          >
            Seriously, don't print, unless necessary.
          </p>
          <br/>
        </div>
      </div>
      <button @click="copyContent()">Copy Signature</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      name: "Stefan Darmanović",
      position: "Graphic designer",
      number: "+382 69 358 725",
      office: "+382 67 000 275",
      info: false,
      isCopied: false,
      instructions: false,
    };
  },

  methods: {
    showInfo(val) {
      this.info = val;
      this.instructions = false;
    },
    showInstructions(val) {
      this.instructions = val;
      this.info = false;
    },
    copyContent() {
      if (this.isCopied) return;
      const range = document.createRange();
      range.selectNode(this.$refs.content);

      const selection = window.getSelection();
      selection.removeAllRanges();
      selection.addRange(range);

      document.execCommand("copy");

      selection.removeAllRanges();
      this.showCopyTooltip();
    },
    showCopyTooltip() {
      this.isCopied = true;
      setTimeout(() => {
        this.isCopied = false;
      }, 1500);
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap");
#app {
  font-family: "Roboto", sans-serif;
  background: #fafafa;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  gap: 40px;
  padding: 0 16px;
  position: relative;
  overflow: hidden;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

::selection {
  color: #000;
  background-color: rgb(30, 230, 151);
}

/* width */
::-webkit-scrollbar {
  width: 8px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: rgb(30, 230, 151);
  border-radius: 20px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: rgba(30, 230, 151, 0.7);
}

input {
  padding: 12px 16px;
  border-radius: 8px;
  border: 1px solid rgb(118, 118, 118);
  color: rgb(118, 118, 118);
  background: transparent;
  font-family: "Roboto", sans-serif;
}

input:focus {
  outline: none;
}

input[type="checkbox"] {
  accent-color: rgb(30, 230, 151);
}

::placeholder {
  /* Chrome, Firefox, Opera, Safari 10.1+ */
  color: rgba(0, 0, 0, 0.87);
  opacity: 1; /* Firefox */
}

:-ms-input-placeholder {
  /* Internet Explorer 10-11 */
  color: rgba(0, 0, 0, 0.87);
}

::-ms-input-placeholder {
  /* Microsoft Edge */
  color: rgba(0, 0, 0, 0.87);
}

header {
  margin-bottom: 40px;
}

.form {
  border-right: 1px solid rgba(0, 0, 0, 0.87);
  background: white;
  padding: 30px 26px;
  width: 100%;
  max-width: 400px;
  height: 100%;
  display: flex;
  flex-direction: column;
  gap: 20px;
  position: absolute;
  left: -400px;
  top: 0;
  transition: all 0.3s ease-in-out;
  z-index: 10;
}

.showInfo {
  left: 0;
  transition: all 0.3s ease-in-out;
  overflow: auto;
}

.showInfo-title {
  display: flex;
  justify-content: space-between;
}

.showInfo-title svg {
  cursor: pointer;
}

.form-input {
  display: flex;
  flex-direction: column;
}

.form-input label {
  font-size: 14px;
  line-height: 22px;
}

.form h2 {
  margin-bottom: 10px;
}

.preview {
  background-color: #fff;
  box-shadow: 0 0px 1px 2px rgba(30, 230, 151, 0.4),
    0 2px 2px 0 rgba(30, 230, 151, 0.44), 2px 1px 5px 0 rgba(30, 230, 151, 0.42);
  padding: 0 20px;
  border-radius: 14px;
  max-width: 471px;
}

.preview-edit {
  position: absolute;
  top: -26px;
  color: rgb(30, 230, 151);
  text-decoration: underline;
  cursor: pointer;
  right: 10px;
}

.preview-instructions {
  position: absolute;
  top: -26px;
  color: rgb(30, 230, 151);
  text-decoration: underline;
  cursor: pointer;
  left: 10px;
}

.instructions-data ul {
  margin-left: 20px;
}

.instructions-data li {
  padding-bottom: 10px;
  font-size: 16px;
  line-height: 24px;
}

.preview-copied {
  position: absolute;
  bottom: -48px;
  color: rgb(30, 230, 151);
  text-decoration: underline;
  right: 0px;
  background: rgba(0, 0, 0, 0.87);
  padding: 8px 14px;
  border-radius: 8px;
  opacity: 0;
  transition: opacity 0.3s ease-in-out;
}

.preview-copied::after {
  content: "";
  position: absolute;
  left: 25px;
  top: -7px;
  width: 0;
  height: 0;
  border-left: 8px solid transparent;
  border-right: 8px solid transparent;
  border-top: 8px solid #000;
  clear: both;
  transform: rotate(180deg);
}

.preview-copied.open {
  opacity: 1;
  transition: opacity 0.3s ease-in-out;
}

.preview-edit:hover {
  color: rgba(30, 230, 151, 0.5);
}

.cards {
  position: relative;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  align-items: stretch;
  justify-content: center;
  gap: 20px;
}

.cards button {
  background: rgba(30, 230, 151, 1);
  border: 1px solid #000;
  padding: 12px 16px;
  border-radius: 8px;
  cursor: pointer;
}

.cards button:hover {
  background: rgba(30, 230, 151, 0.7);
}
</style>
