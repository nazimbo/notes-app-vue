<template>
  <main>
    <div class="container">
      <header>
        <h1>My notes</h1>
        <button>+</button>
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
</style>
