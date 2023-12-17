<template>
  <router-view/>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@100;200;300;400;500;600;700;800;900&display=swap');

#app {  
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgb(255, 255, 255);
  background-color: black;
}

::-webkit-scrollbar{
  background-color: black;
  // border: 1px solid white;
}
::-webkit-scrollbar-thumb {
  background-color: #FFC700; 
  border-radius: 10px;
}

*{
  font-family: 'Noto Sans KR', sans-serif;

}
a{
  text-decoration: none;
  color: white;
}

h1,h2,h3,figure,p,body,ul{
  margin: 0;
}

ul{
  padding: 0;
}

li{
  list-style: none;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

@media (max-width:767px) {

  ::-webkit-scrollbar{
  background-color: black;
  // border: 1px solid white;
  width: 10px;
}
::-webkit-scrollbar-thumb {
  background-color: #FFC700; 
  border-radius: 10px;
}
}

</style>
