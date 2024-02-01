<template>
  <main>
    <div class="container">
      <header>
        <h1>My notes</h1>
        <button>+</button>
      </header>
      <div class="cards">
        <div class="card">
          <p class="text">sicing elit. Quisquam voluptatum, quibusdam, quia, quae voluptates voluptatem quod voluptatibus quos doloribus quas doloremque. Quisquam voluptatum, quibusdam, quia,</p>
          <p class="date"></p>
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
  margin: 20px 0;
}

h1 {
  font-size: 40px;
  font-weight: bold;
}

button {
  font-size: 30px;
  font-weight: bold;
  background: black;
  color: white;
  border: none;
  border-radius: 100%;
  cursor: pointer;
}

.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 20px;
}

.card {
  background: #d8a626;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  width: 200px;
  height: 200px;
}

.text {
  font-size: 20px;
  font-weight: bold;
  height: 100px;
  overflow: hidden;
}
</style>
