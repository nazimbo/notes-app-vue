<script setup>
import { ref } from "vue";

const showModal = ref(false);
const newNote = ref("");
const notes = ref([]);

const saveNote = () => {
  notes.value.push({
    text: newNote.value,
    date: new Date().toLocaleDateString(),
  });
  showModal.value = false;
  newNote.value = "";
};
</script>

<template>
  <main>
    <div v-if="showModal" class="overlay">
      <div class="modal">
        <textarea v-model="newNote" id="new-note" name="new-note" placeholder="New note" cols="30" rows="10"></textarea>
        <button @click="saveNote">Save</button>
        <button class="cancel" @click="showModal = false">Cancel</button>
      </div>
    </div>
    <div class="container">
      <header>
        {{ notes }}
        <h1>My notes</h1>
        <button @click="showModal = true">+</button>
      </header>
      <div class="cards">
        <div class="card">
          <p class="text">My first note</p>
          <p class="date">20/10/2020</p>
        </div>
        <div class="card">
          <p class="text">My second note</p>
          <p class="date">20/10/2020</p>
        </div>
        <div class="card">
          <p class="text">My third note</p>
          <p class="date">20/10/2020</p>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  width: 100vw;
  height: 100vh;
}

.container {
  max-width: 1000px;
  padding: 0 20px;
  margin: 0 auto;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h1 {
  font-size: 40px;
  font-weight: bold;
}

header button {
  font-size: 40px;
  font-weight: bold;
  background: black;
  color: white;
  border: none;
  border-radius: 30%;
  cursor: pointer;
}

.cards {
  display: flex;
  flex-wrap: wrap;
}

.card {
  background: firebrick;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  width: 200px;
  height: 200px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 10px;
}

.text {
  font-size: 20px;
  font-weight: bold;
  height: 100px;
  overflow: hidden;
}

.date {
  font-size: 12px;
  font-weight: bold;
  text-align: right;
}

.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  z-index: 10;
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal {
  position: relative;
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  width: 50%;
  height: 50%;
  display: flex;
  flex-direction: column;
}

#new-note {
  height: 100%;
  resize: none;
  border: none;
  outline: none;
  font-size: 20px;
  font-weight: bold;
}

.modal button {
  font-size: 20px;
  font-weight: bold;
  background: black;
  color: white;
  border: none;
  border-radius: 10px;
  padding: 10px;
  cursor: pointer;
  margin-top: 10px;
}

.modal .cancel {
  background: gray;
}
</style>
