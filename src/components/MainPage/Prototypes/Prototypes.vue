<template>
  <LargeBox title="~ Enter Prototype Code ~">
    To see your prototype enter the prototype code to continue.
    <br />
    To test the function enter '<i>A1-B2-C3</i>'.

    <div class="small-box">
      <input type="text" placeholder="A1-B2-C3" />
      <button>>></button>
    </div>
  </LargeBox>
</template>

<script>
import LargeBox from "@/components/MainPage/LargeBox.vue";

export default {
  name: "Prototypes",
  components: {
    LargeBox,
  },
};
</script>

<style scoped>
input {
  border-style: none;
  width: 40%;
  height: 40px;
  border-radius: 12px;
  font-size: 18px;
  font-family: Arial, Helvetica, sans-serif;
  font-weight: 100;
  padding: 5px 10px;
  outline: none;
  box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.11);
}

input:focus {
  outline: none;
  border-style: none;
  box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.2);
}

button {
  background-color: #3498db;
  color: white;
  border: none;
  padding: 12px 12px;
  margin-left: 4px;
  font-size: 18px;
  font-weight: bold;
  border-radius: 10px;
  cursor: pointer;
  transition: all 0.1s ease-in-out;
  box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.11);
}

button:hover {
  background-color: #2980b9;
  transform: scale(1.05);
}

button:active {
  background-color: #1f6690;
  transform: scale(0.98);
}

.small-box {
  background-color: #e8f6fc;
  padding: 20px;
  margin: 20px;
  border-radius: 20px;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
  transition: all 0.3s ease-in-out;
}

.small-box:hover {
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.15);
}
</style>
