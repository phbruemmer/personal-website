<template>
  <div class="container">
    <div class="center">
      <h1 class="typewriter">~ {{ message }}</h1>
      <img src="@/assets/vibing_cat.gif" alt="" class="hidden-img" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Welcome",
  data() {
    return {
      message: "",
      /* Messages to display (in order) */
      messages: [
        "Welcome! ~",
        "Willkommen! ~",
        "Hello. ~",
        "Hallo! ~",
        "Bonjour! ~",
        "Hola! ~",
        "Ciao! ~",
        "God dag! ~",
        "Salut! ~",
        "Bienvenidos! ~",
        "Benvenuto! ~",
        "Velkommen! ~",
        "Guten Tag! ~",
        "Buenas tardes! ~",
        "Buongiorno! ~",
      ],
      currentMessageIndex: 0,
    };
  },
  mounted() {
    this.typeWriter();
  },
  methods: {
    typeWriter() {
      let i = 0;
      let speed = 150;
      const currentMessage = this.messages[this.currentMessageIndex];

      const type = () => {
        if (i < currentMessage.length) {
          this.message += currentMessage.charAt(i);
          i++;
          setTimeout(type, speed);
        } else {
          setTimeout(this.deleteMessage, 2000);
        }
      };
      type();
    },
    deleteMessage() {
      let i = this.message.length;
      let speed = 100;

      const erase = () => {
        if (i > 0) {
          this.message = this.message.slice(0, i - 1);
          i--;
          setTimeout(erase, speed);
        } else {
          this.currentMessageIndex =
            (this.currentMessageIndex + 1) % this.messages.length;
          this.typeWriter();
        }
      };
      erase();
    },
  },
};
</script>

<style scoped>
.center {
  background-image: url("@/assets/image.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  height: 60vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.typewriter {
  color: #fff;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 48px;
  white-space: nowrap;
  overflow: hidden;
  border-right: 4px solid #fff;
  animation: blink 0.7s step-end infinite;
}

@keyframes blink {
  50% {
    border-color: transparent;
  }
}

h1:hover {
  cursor: default;
}

.container {
  position: relative;
}

.hidden-img {
  width: 60px;
  position: absolute;
  top: -35px;
  right: 20%;
  opacity: 0;
  transition: opacity 1s ease-in-out;
}

.center:hover .hidden-img {
  opacity: 0.6;
}
</style>
