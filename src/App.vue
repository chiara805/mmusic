<template>
  <v-app id="inspire">
    <div class="loading__page" v-if="loading == 0">
      <img src="assets/IMG_2599_2.svg alt="Immagine SVG">
    </div>
      
    <v-main class="main__page" v-if="loading == 1">
      <v-app-bar prominent v-if="logged">
        <v-toolbar-title @click="$router.push({ path: '/' })">
         <img src=assets/IMG_2599_2.svg alt="Immagine SVG">
         
        </v-toolbar-title>

        <v-spacer></v-spacer>

        <div class="pa-4 text-center">
    <v-dialog max-width="800">
      <template v-slot:activator="{ props: activatorProps }">
        <svg v-bind="activatorProps" width="30" height="30" viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg">
          <mask id="path-1-inside-1_325_538" fill="white">
          <path d="M21.4408 18.8679H20.0858L19.6055 18.4048C21.2864 16.4494 22.2985 13.9108 22.2985 11.1492C22.2985 4.99142 17.307 0 11.1492 0C4.99142 0 0 4.99142 0 11.1492C0 17.307 4.99142 22.2985 11.1492 22.2985C13.9108 22.2985 16.4494 21.2864 18.4048 19.6055L18.8679 20.0858V21.4408L27.4443 30L30 27.4443L21.4408 18.8679ZM11.1492 18.8679C6.87822 18.8679 3.43053 15.4202 3.43053 11.1492C3.43053 6.87822 6.87822 3.43053 11.1492 3.43053C15.4202 3.43053 18.8679 6.87822 18.8679 11.1492C18.8679 15.4202 15.4202 18.8679 11.1492 18.8679Z"/>
          </mask>
          <path d="M21.4408 18.8679H20.0858L19.6055 18.4048C21.2864 16.4494 22.2985 13.9108 22.2985 11.1492C22.2985 4.99142 17.307 0 11.1492 0C4.99142 0 0 4.99142 0 11.1492C0 17.307 4.99142 22.2985 11.1492 22.2985C13.9108 22.2985 16.4494 21.2864 18.4048 19.6055L18.8679 20.0858V21.4408L27.4443 30L30 27.4443L21.4408 18.8679ZM11.1492 18.8679C6.87822 18.8679 3.43053 15.4202 3.43053 11.1492C3.43053 6.87822 6.87822 3.43053 11.1492 3.43053C15.4202 3.43053 18.8679 6.87822 18.8679 11.1492C18.8679 15.4202 15.4202 18.8679 11.1492 18.8679Z" fill="#1E1E1E" fill-opacity="0.28"/>
          <path d="M21.4408 18.8679L24.2721 16.0423L23.1 14.8679H21.4408V18.8679ZM20.0858 18.8679L17.3092 21.7473L18.4713 22.8679H20.0858V18.8679ZM19.6055 18.4048L16.5722 15.7973L14.1096 18.6619L16.8289 21.2842L19.6055 18.4048ZM18.4048 19.6055L21.2842 16.8289L18.6619 14.1096L15.7973 16.5722L18.4048 19.6055ZM18.8679 20.0858H22.8679V18.4713L21.7473 17.3092L18.8679 20.0858ZM18.8679 21.4408H14.8679V23.1L16.0423 24.2721L18.8679 21.4408ZM27.4443 30L24.6187 32.8313L27.4471 35.654L30.2727 32.8284L27.4443 30ZM30 27.4443L32.8284 30.2727L35.654 27.4471L32.8313 24.6187L30 27.4443ZM21.4408 14.8679H20.0858V22.8679H21.4408V14.8679ZM22.8623 15.9885L22.382 15.5254L16.8289 21.2842L17.3092 21.7473L22.8623 15.9885ZM22.6388 21.0123C24.9187 18.3601 26.2985 14.9049 26.2985 11.1492H18.2985C18.2985 12.9167 17.6542 14.5387 16.5722 15.7973L22.6388 21.0123ZM26.2985 11.1492C26.2985 2.78228 19.5162 -4 11.1492 -4V4C15.0979 4 18.2985 7.20056 18.2985 11.1492H26.2985ZM11.1492 -4C2.78228 -4 -4 2.78228 -4 11.1492H4C4 7.20056 7.20056 4 11.1492 4V-4ZM-4 11.1492C-4 19.5162 2.78228 26.2985 11.1492 26.2985V18.2985C7.20056 18.2985 4 15.0979 4 11.1492H-4ZM11.1492 26.2985C14.9049 26.2985 18.3601 24.9187 21.0123 22.6388L15.7973 16.5722C14.5387 17.6542 12.9167 18.2985 11.1492 18.2985V26.2985ZM15.5254 22.382L15.9885 22.8623L21.7473 17.3092L21.2842 16.8289L15.5254 22.382ZM14.8679 20.0858V21.4408H22.8679V20.0858H14.8679ZM16.0423 24.2721L24.6187 32.8313L30.2698 27.1687L21.6935 18.6096L16.0423 24.2721ZM30.2727 32.8284L32.8284 30.2727L27.1716 24.6158L24.6158 27.1716L30.2727 32.8284ZM32.8313 24.6187L24.2721 16.0423L18.6096 21.6935L27.1687 30.2698L32.8313 24.6187ZM11.1492 14.8679C9.08735 14.8679 7.43053 13.2111 7.43053 11.1492H-0.569468C-0.569468 17.6294 4.66908 22.8679 11.1492 22.8679V14.8679ZM7.43053 11.1492C7.43053 9.08736 9.08736 7.43053 11.1492 7.43053V-0.569468C4.66908 -0.569468 -0.569468 4.66908 -0.569468 11.1492H7.43053ZM11.1492 7.43053C13.2111 7.43053 14.8679 9.08735 14.8679 11.1492H22.8679C22.8679 4.66908 17.6294 -0.569468 11.1492 -0.569468V7.43053ZM14.8679 11.1492C14.8679 13.2111 13.2111 14.8679 11.1492 14.8679V22.8679C17.6294 22.8679 22.8679 17.6294 22.8679 11.1492H14.8679Z" fill="#1E1E1E" mask="url(#path-1-inside-1_325_538)"/>
          </svg>
      </template>

      <template v-slot:default="{ isActive }">
        <v-card >
          <template v-slot:text>
            
              
          <v-card-actions>
            <v-spacer></v-spacer>

            <h3 style="cursor: pointer;"
              @click="isActive.value = false; artists = []"
            >Chiudi</h3>
          </v-card-actions>
            <input type="text" v-model="query" @keyup.enter="searchArtists()" @input="searchArtists()"
            placeholder="Cerca artista o canzone" />
          <div v-if="artists.length > 0"
            style="background-color: white;">
            <ul style="list-style: none;">
              <li style="padding: 1vh 0 1vh 0; cursor: pointer;" v-for="artist in artists" :key="artist.id"
                @click="$router.push({ path: '/artista:' + artist.id })">
                {{ artist.name }}
              </li>
              <li style="padding: 1vh 0 1vh 0; cursor: pointer;" v-for="music in music" :key="music.id"
                @click="$router.push({ path: '/canzone:' + music.id })">
                {{ music.name }}
              </li>
            </ul>
          </div>
          </template>
        </v-card>
      </template>
    </v-dialog>
  </div>

<!--         <div class="combobox__modify">
          <input type="text" v-model="query" @keyup.enter="searchArtists()" @input="searchArtists()"
            placeholder="Cerca destinazione" />
          <div class="ods__mini__card" v-if="artists.length > 0"
            style="position: fixed;max-height: 8cm;overflow-y: scroll; z-index: 99; background-color: white;">
            <div style="margin: 3vh 0 3vh 0;">
              <h4 @click="artists = []" style="cursor: pointer;">Chiudi</h4>
            </div>
            <ul style="list-style: none;">
              <li style="padding: 1vh 0 1vh 0; cursor: pointer;" v-for="artist in artists" :key="artist.id"
                @click="$router.push({ path: '/artista:' + artist.id })">
                {{ artist.name }}
              </li>
              <li style="padding: 1vh 0 1vh 0; cursor: pointer;" v-for="music in music" :key="music.id"
                @click="$router.push({ path: '/canzone:' + music.id })">
                {{ music.name }}
              </li>
            </ul>
          </div>
        </div> -->
        <div class="profile">
          <svg @click="$router.push({ path: '/profilo:' + user })" width="27" height="27" viewBox="0 0 27 27"
            fill="none" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
            <rect width="27" height="27" fill="url(#pattern0_268_439)" />
            <defs>
              <pattern id="pattern0_268_439" patternContentUnits="objectBoundingBox" width="1" height="1">
                <use xlink:href="#image0_268_439" transform="scale(0.0104167)" />
              </pattern>
              <image id="image0_268_439" width="96" height="96"
                xlink:href="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAACXBIWXMAAAsTAAALEwEAmpwYAAAG70lEQVR4nO1dS4xURRStwS+iJipjT3fXOdUzGR0cY9TMCuOPj7pQ8Q/BGNfi4Ieo4E6NLIgGQZAFwbhgyUbQ1YjGjWCiGEWRGMKgjqNGcUBiQvzNPHOxElEHeK+76lW9nneSm0y63/Q7t6pe1a17b92nVIkSJUqUKFGiRIkSJUpEhJ6enou11reQfJTkBgBvk/yU5DDJQwB+E5G/7Wfy3Xa5luQjAG7u6urqDK1HYVCtVs8BcAeAl21jTpBMWpQJ+1trASzQWk8PrWdsmAbgWpIbARxx0OCnkqMktwC4XSl1mpqqMMacrbV+GMCBHBr9RDIMYIlwUVNpmiH5JIDvAjb8v0S4GGOeEG6qnSGPPYAvQzc4TyyjJO9T7QZjTAPAmxE0cJJStjUaDaPaAVrrO62ZGLpRk4zT0hEAi1RR0dvbe5Y1J5OCy0bRRRUJtVrtIgDvR9B4iaOnYYfW+kJVBACo2Y1P8Iaj207Y29PTQxUzjDGzSI54bIQvSK4iOU/uValUZojY+86T7+w1vjpiRO6lYoTWug7gK0+Kf0hyblouJK8B8J4nLqPRWUh2zt/rYcT/LjtVpVRHE7Q6SA7Kb3jg9Xk0a4K1dnwsuGPGmBtb5WeMmePDDAawMwrrCMArPka+MWaOQ47XWbe1a57rVEiQvNfDyE/stOOa61IfXEneowK6F372oNAHTc75adaEXR4Gy+Egi7Iv345xOPX8FyTne3oK3lAB/Ds+pp69vrn72ifYAE9uYUNf9v4q3/wBvOCpAw7kEu6UYIqnxk9kN+ubP4CbfPEHsMwrebF7SX7rS4F6vX6JVwWUUo1Go89jB3zv9SmQGK7H0Z90dnaeqzxD7uFTBwAP+cxe8BpA7+vrO095htzDd6Dfixltt/Q+iSe1Wu1S58T/r8cs33porW9wTpzka76Jk5yvPEOy5XzrAeBVp6RlYfG0600CmKEv5tABR5wuxpIumEPjJ7JJUp5Bcl8eupC8zRnpnIPrc1XxXBGTyUsuiecW4wXwsVhcqiDOuFPo4SZF3FGWchYZVI4h6eo56zBerVZntkzc5ufnSTyxYcS5sQdkcrHq7OGIJIAccuGalo4MmJm31EUHbAhEPrFPwtImd5bT7LTzR0D+6110wPZQCvAf2ZXFUyqPPoCPIuA95KIDPotAkcTKPvHni0tZXAriWBMxxlwmO1zr68/Lzk8ju1vuAI/Bl6TdRZyXLp6AsdCKsLhy0MUTEMJ8S9pBAPxadgAL3gHlFMTgU1C5CDPsIhyTGZoUTHa3y0YsKagMFdoVwYKLk+zpgM64pA1ksJDuaLaPtO6Olno7AQIyiYgkAgB4Vx5lSfszxtxljLlKUuNJXjAwMHCGiPwtnxljrpZr5FrxRNr/zaMCy2QyLke3lAvIap4T6REAm7TWi22aoosEpw7JNzLG3C/pIiS/KVRIUiDFjnwS5d8Jv/0qJwC43FZs+cRjJ6x2SXiB40b/QQhqra9QgdFoNK6UDAaSPzrugFtjTMw6SHJFjHV5KpXKDACPuahj5Dwxy0Fq4i8kn4qx4SfrCJLLLedmO2CTcg05s9skmXeir7EwCeTgnVhRzeistb5eecA0Wxoy60JU5MJ4p5Nck1Hn/Z5OeR5bjJdkGPnPqTYByZUxHNA4Vukw5SL1urdREAaS1rg1hd6j3ssXSHXBFKPga2e7wAggO+00p4MAPJ7XMdU0lQ+3tclT0JHyUPpwblV5M2zMlquCA8DTuW+80kCO56cgNU7yAVVQAHjQ6pBmzQtiJx9OQe5PAAtVwaC1XizcU+h3KNg+xxhzdxpXtU2yLUxFWgCLUib1Toj7OzTZdSnnyAl7CM/H6ReX5uaKlNOOyBoVScmyHSkJH5sv8ziQnRW9vb3ni+WWVg8pCtjf33+migFSwE4K2WXohP2S4awigQ27ZnGz7ImmaF+LZSu3yBm0UJy7u7srADZn5DwarXOxmcKtAA4DeD7Pd73Yg4crU1pxx8uIVFtRMaNWqyHjdJRYOSoVGH0qaAfIBvsak6z89tTrda2KALsm7GxCycSKnEt+xkXIUn4DwLOtpFjKghvdnJ/SOkproiYnEYnVDtm60IuMMbPlSJIxpku8syIkq/az2daGl/rSb9kQaCv3FtN5bTTWTgt1Jor6AoeFqh0gbouUvqMkEtkaraXj4CU+IV9blZxChnP3auYNG09Y5rP4H7PLqARTptRb9uwivaSJQL/TES8x3CiqoIcEyQFbk+innBJ+N9vM5XaI2LmD1nq6VJqSVEGbt5nWK3kyGbf5p6tlfp9Sry1sFdVqdaatdCtvwlgvtr3tGJm2xo57ne2YnU7kuyF77aCMcic1e0qUKFGiRIkSJUqUKFFCucNfVoNEk2F82KUAAAAASUVORK5CYII=" />
            </defs>
          </svg>
        </div>
      </v-app-bar>
      <div class="app__container">
        <router-view></router-view>
      </div>
    </v-main>
  </v-app>
  <div>

  </div>
</template>

<script lang="ts">
import DataService from "./dataservice";
export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      dialog: false,
      drawer: false,
      group: null,
      loading: 0,
      logged: false,
      section__app: 0,
      user: localStorage.getItem("login"),
      query: '',
      artists: [],
      music: []
    }
  },
  watch: {
    group() {
      this.drawer = false
    },
  },
  // Methods are functions that mutate state and trigger updates.
  // They can be bound as event handlers in templates.
  methods: {
    checkLog() {
      this.logged = DataService.isAuthenticated()
    },
    searchArtists: async function () {
      try {
        const response = await DataService.getGene(this.query);
        this.music = response.data._embedded.results.map((result: any) => ({
          id: response.data._embedded.results[0]._links.permalink.href.replace("https://www.music.net/music/", ""),
          name: result.title,
        }));

        console.log(response.data._embedded.results)
        
        const response2 = await DataService.searchArtists(this.query);
        this.artists = response2.data._embedded.results.map((result: any) => ({
          id: response2.data._embedded.results[0]._links.self.href.replace("https://api.music.net/api/artists/", ""),
          name: result.title,
        }));
      } catch (error) {
        console.error(error);
      }
    },
  },

  mounted() {
    setTimeout(() => {
      this.loading = 1;
    }, 3000);
    this.checkLog()
  },
  setup() {
  },
};
</script>

<style>
.profile {
  margin: 0 4vh 0 4vh;
  cursor: pointer;
}

.app__container{
  margin-top: 4cm
}

.v-app-bar {
  padding: 4vh;
}

.fill__notopen__link {
  fill: #1e1e1e48;
}

.fill__open__link {
  fill: #FF5400;
}

.menu__laterale div {
  margin: 8vh 2vh 8vh 2vh;
  display: flex;
  width: 100%;
  align-items: center;

}

.menu__laterale div span {
  margin-right: 6vw;

}

.navbar__cell {
  display: none
}

.navigation {
  display: block
}

.navigation__inside {
  position: fixed;
}

.navigation {
  height: 100%;
  overflow: hidden;
  transition: 0.5s;
  padding: 1vh 3vw 0 3vw;
}

.navigation ul {
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  border-right: 1px solid var(--vt-c-divider-dark-1);
  padding-right: 2vw;
}

.navigation ul li {
  position: relative;
  width: 100%;
  list-style: none;
  margin: 5vh 0 5vh 0;
}

.navigation ul li path {
  transition-duration: .2s;
}

.navigation ul li:hover path {
  fill: #FF5400 !important;
}

.navigation ul li a {
  position: relative;
  display: block;
  width: 100%;
  display: flex;
  text-decoration: none;
  color: var(--color-text);
}

.navigation ul li a .icon {
  position: relative;
  display: block;
  min-width: 60px;
  height: 60px;
  line-height: 60px;
  text-align: center;
  display: flex;
  align-items: center;

}

.navigation ul li a .icon .fa {
  font-size: 24px;
}

.navigation ul li a .title {
  position: relative;
  display: block;
  padding: 0 10px;
  height: 60px;
  line-height: 60px;
  text-align: start;
  white-space: nowrap;
}

.loading__page {
  position: fixed;
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.loading__page svg {
  padding: 1vh 1vw 1vh 1vw;
}

@media only screen and (max-width: 800px) {
  .navbar__cell {
    display: block
  }

  .navigation {
    display: none
  }

  .v-spacer{
    display: none;
  }
}

@media only screen and (max-width: 1200px) {
  .svg_arrow {
    display: none;
  }

  .loading__page {
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: center;
    padding: 0;
  }
}
</style>
