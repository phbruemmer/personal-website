<template>
  <div
    class="box-container"
    @mouseover="showLikeButton = true"
    @mouseleave="showLikeButton = false"
  >
    <h2 class="box-title">{{ title }}</h2>
    <p class="box-text"><slot /></p>

    <transition name="fade">
      <!-- v-if = Directive used to conditionally render elements in vue.js :) -->
      <button
        v-if="showLikeButton"
        class="like-button"
        :class="{ liked: liked }"
        @click="toggleLike"
      >
        {{ liked ? "❤️" : "❤" }} {{ likes }}
      </button>
    </transition>
  </div>
</template>

<script>
export default {
  name: "Box",
  props: {
    title: {
      type: String,
    },
  },
  data() {
    return {
      likes: 0,
      liked: false,
      showLikeButton: false,
    };
  },
  methods: {
    toggleLike() {
      if (this.liked) {
        this.likes--;
      } else {
        this.likes++;
      }
      this.liked = !this.liked;
    },
  },
};
</script>

<style scoped>
.box-container {
  position: relative;
  width: 100%;
  max-width: 400px;
  margin: 20px auto;
  padding: 20px;
  background-color: #fffbf3;
  border-radius: 32px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
  font-family: "Arial", sans-serif;
  transition: all 0.3s ease-in-out;
}

.box-title {
  font-size: 20px;
  color: #333333d1;
  margin-bottom: 12px;
  text-align: center;
  font-weight: 600;
}

.box-text {
  font-size: 16px;
  color: #555;
  text-align: center;
  line-height: 1.5;
  padding: 10px;
}

.like-button {
  position: absolute;
  bottom: 10px;
  right: 10px;
  background-color: #ff4d4d;
  color: white;
  border: none;
  border-radius: 20px;
  padding: 6px 12px;
  cursor: pointer;
  font-size: 14px;
  transition: transform 0.2s, background-color 0.3s;
}

.like-button.liked {
  background-color: white;
  color: #ff4d4d;
}

.like-button:hover {
  transform: scale(1.1);
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
