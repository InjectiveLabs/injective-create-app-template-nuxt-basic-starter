<template>
  <div>
    <div class="header">
      <AppConnectWallet />
    </div>
    <main>
      <div class="hero">
        <InjectiveLogo class="logo" />
        <h3>Create Injective App</h3>
        <a
          target="_blank"
          href="https://docs.ts.injective.network"
          >Learn how to build on Injective</a
        >
      </div>
    </main>
  </div>
</template>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
body {
  background: #151518;
  color: white;
  font-family: Arial, Helvetica, sans-serif;
}
main {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.header {
  position: absolute;
  left: 0;
  right: 0;

  display: flex;
  justify-content: flex-end;
  padding: 1rem;
}

.logo {
  width: 20vw;
  margin-bottom: 2rem;
}
.hero {
  display: flex;
  gap: 1rem;
  flex-direction: column;
  align-items: center;
}

a {
  color: lightgreen;
}
</style>
