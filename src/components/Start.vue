<template>
  <section id="start">
    <h1>Palavras Secretas</h1>
    <p>com VUE</p>
    <button>Começar</button>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
//
#start {
  max-width: 800px;
  min-height: 90vh;
  margin: 0 auto;
  padding: 0 20px;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  justify-items: center;

  h1 {
    text-align: center;
    font-size: 2rem;
    color: #aa9ad9;
  }

  p {
    text-align: center;
  }

  button {
    width: 100%;
    max-width: 300px;
    margin-left: auto;
    margin-right: auto;
    display: block;
    padding: 10px 30px;
    border-radius: 4px;
    background: #aa9ad9;
    color: #ffffff;
    text-align: center;
    font-size: 1rem;
    transition: all 0.3s;
    border: none;
    cursor: pointer;
    box-shadow: 0 4px 8px rgba(30, 60, 90, 0.2);
    font-family: Avenir, Helvetica, Arial, sans-serif;

    &:hover {
      background: #c4a1e3;
      transform: scale(1.1);
    }
  }
}
</style>
