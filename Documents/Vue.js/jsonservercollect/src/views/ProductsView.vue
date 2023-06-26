<template>
    <div id="players">
        <h1>Players</h1>
        <footer></footer>
    </div>
    <footer/>
</template>

<script>
async function getPlayers(){
    const soccer_stars = await fetch ('https://siya021.github.io/JSONserver/soccer.json')
    const jsonPlayer = await soccer_stars.json()
    console.log(jsonPlayer);
    let fetchedData = jsonPlayer.soccer_stars

    const display = document.querySelector('#players')

    fetchedData.forEach(soccer_stars =>{
        display.innerHTML += `
        <div class="card">
            <img src="${soccer_stars.image}" style="width: 18rem">
            <div class="cardbody">
            <h3 class="card-title">${soccer_stars.name}</h3>
            <p class="card-text">${soccer_stars.position}</p>
            <p class="card-text">${soccer_stars.team}</p>
            </div>
        </div>`
    })
}
getPlayers()
import footer from '@/components/Footer.vue'
    export default {
        name: "footer",
        components: {
            footer
        }
    }
</script>

<style lang="scss" scoped>

</style>