<template>
  <div :class="styles.root">
    <div :class="styles.header">
      <header>
        <NuxtLink to="/">ここはヘッダーです</NuxtLink>
      </header>
    </div>
    <div :class="styles.nav">
      <nav>
        <ul>
          <li><NuxtLink to="/a">PageA</NuxtLink></li>
          <li><NuxtLink to="/b">PageB</NuxtLink></li>
          <li><NuxtLink to="/c">PageC</NuxtLink></li>
          <li><NuxtLink to="/cards">Cards</NuxtLink></li>
        </ul>
      </nav>
    </div>
    <main :class="styles.main">
      <slot />
    </main>
  </div>
</template>

<style module="styles">
.root {
  display: grid;
  grid-template-areas: "header header" "nav main";
  grid-template-rows: minmax(50px, auto) 1fr;
  grid-template-columns: minmax(200px, auto) 1fr;
  height: 100vh;
  overflow: hidden;
}
.header {
  grid-area: header;
  display: flex;
  justify-content: center;
  padding: 8px 16px;
  background-color: skyblue;
}
.nav {
  grid-area: nav;
  padding: 32px 16px;
  background-color: lightblue;
}
.main {
  grid-area: main;
  padding: 16px;
  overflow: auto;
}
</style>
