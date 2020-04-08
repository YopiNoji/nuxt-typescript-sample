<template>
  <div>
    <nav>
      <ul>
        <li><nuxt-link to="/">Top</nuxt-link></li>
        <li><nuxt-link to="/composition">Composition</nuxt-link></li>
      </ul>
    </nav>
    <nuxt />
  </div>
</template>

<style scoped>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
nav {
  position: fixed;
  top: 100px;
  left: 50px;
}
ul li {
  position: relative;
  height: 3em;
  color: #888;
}
</style>
