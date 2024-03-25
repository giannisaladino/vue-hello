## PRIMO APPROCCIO CON IL VUE-JS

 - Base di vue-js

Lo script-src di Vue-js va inserito prima di quello del js-vanilla perchè altrimenti non vedrebbe le modifiche applicate con vue.

Link vue-js: <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<!-- const { createApp } = Vue

createApp({
data() {
    return {
    message: 'Hello Vue!'
    }
}
}).mount('#app') -->

Questo è la build base da cui partire per utilizzare vue; la funzione "data()" ritorna un oggetto con le proprietà che noi andremo ad inserire e che utilizzeremo come fossero delle variabili per scrivere sull'HTML attraverso il template necessario:

<div id="app">{{ message }}</div>

Creiamo quindi un div principale nell'html nel quale andremo ad inserire il contenuto con vue-js;
invece di inserire il contenuto manualmente infatti, utilizzeremo le proprietà dichiarate nell'oggetto che ritorna dalla funzione di vue-js, messe all'interno delle {{}}.

- - -

Nel caso in cui però volessi andare ad utilizzare una proprietà come valore dell'attributo sul tag html, non potrò utilizzare il template {{}}, ma vengono in soccoro le "v-directive"; nel caso di un immagine per esempio:

<img v-bind:src= "srcImage" alt="">

utilizzerò quindi la directive v-bind per poter utilizzare la mia proprietà "srcImage" nell src dell'immagine senza che me la cerchi come stringa.

<img :src= "srcImage"

posso anche abbreviare la sintassi e utilizzare solo i ":" prima dell'attributo per assegnargli la directive.

- - -

Come "v-bind" ne esistono tante altre di directive come: v-on, v-if/v-elseif/v-else, v-for.

"v-on" ad esempio potrebbe sostituire l'addEventListener del JS, permettendomi di applicare l'evento direttamente sul tag HTML e risparmiandomi la richiamata dell'elemento del DOM dal js:

<a v-on:click="doSomething"> ... </a>

che si può sintetizzare in...

<a @click="doSomething"> ... </a>


