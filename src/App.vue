<template>
<div id="app">
    <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
    </div>
    <router-view />
</div>
</template>

<style>
@font-face {
    font-family: 'GalanoGrotesque';
    src: url('./GalanoGrotesque-Bold.woff') format('woff2'),
        url('./GalanoGrotesque-Bold.woff') format('woff');
    font-weight: bold;
    font-style: normal;
    font-display: swap;
}

@font-face {
    font-family: 'HelveticaNeue';
    src: url('./HelveticaNeue-Light.woff2') format('woff2'),
        url('./HelveticaNeue-Light.woff') format('woff');
    font-weight: 300;
    font-style: normal;
    font-display: swap;
}

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #fff;
}

#nav {
    padding: 30px;
    display: none
}

#nav a {
    font-weight: bold;
    color: #fff;
}

#nav a.router-link-exact-active {
    color: #923e0e;
}
</style>
