<template>
<div id="app">
  <div class="header">
    <router-link to="/">
      <div class="logo">
        <img src="/hearts-icon-19-48.png">
      </div>
    <div class="title">
      <h1>Me and My Best Friend</h1>
    </div>
    </router-link>
  </div>
  <div class="content">
    <router-view />
  </div>
  <div class="footer">

    <router-link to="/admin">Add Memories</router-link>
    <div class="otherpage">
      <router-link to="/future">Future Memories</router-link>
    </div>
      <div class="git">
      <a href="https://github.com/bjamin5/CreativeProject4BandK.git"> Github Repository</a>
    </div>
  </div>
</div>
</template>

<style>
html {
  box-sizing: border-box;
}

body {
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  background: #5BDEFF;
  padding: 0px;
  margin: 0px;
}

/* Header */
.header {
  display: center;
  padding: 10px 100px 10px 100px;
  background-color: #FFFF66;
  color: #1C454F;
}

.header .logo {
  text-align: center;
}
.home {
  text-align: center;
}
.title {
  margin-top: 5px;

}

.title h1 {
  font-size: 30px;
  text-align: center;
}

.content {
  padding: 20px 100px;
  min-height: 500px;
}

/* Footer */
.footer {
  height: 50px;
  padding: 20px 100px 0px 100px;
  background: #e3e3e3;
  font-size: 12px;
}

.footer {
  color: #000;
  background-color: #FFFF66;
  display:inline-flex;
  width:25%;

}



.footer .otherpage {
  padding-left: 60px;
}

.footer .git {
  padding-left: 60px;


}
h1 {
  font-size: 20px;
}

h2 {
  font-size: 14px;
}
</style>
