<template>
  <div id="app">

    <!--
    <div style="overflow:hidden;z-index:1;position:absolute;top:0;left:0;bottom:0;right:0;width:100%;height:100%;">
      <SvgTrack />
    </div>
    -->

    <section class="intro">
      <div>
        <h1 class="title">Hello, I'm David 👋</h1>
        <h3 class="subtitle">A creative developer focused on front-end development and user experience</h3>
      </div>

      <div class="containerTest">
        <div class="svg-wrapper">
          <svg
            version="1.1"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            x="0px"
            y="0px"
            width="100%"
            height="100%"
            xml:space="preserve"
            viewBox="0 0 360 360"
          >

            <path
              class="street"
              d="M180,48A132,132,0,1,1,48,180,132,132,0,0,1,180,48"
            />

            <path
              ref="stripesTest"
              class="stripes"
              d="M180,48A132,132,0,1,1,48,180,132,132,0,0,1,180,48"
            />

            <g
              class="bike"
              transform="translate(-50 -11)"
            >
              <title>bike</title>
              <rect
                x="49"
                y="11"
                width="31"
                height="3"
              />
              <rect
                y="11"
                width="31"
                height="3"
              />
              <rect
                class="cls-1"
                x="14"
                y="11"
                width="52"
                height="3"
              />
              <rect
                class="cls-2"
                x="25"
                y="5"
                width="15"
                height="15"
              />
              <rect
                x="28"
                y="7"
                width="11"
                height="11"
              />
              <rect
                class="cls-3"
                x="40"
                y="14"
                width="6"
                height="6"
              />
              <rect
                class="cls-3"
                x="40"
                y="5"
                width="10"
                height="6"
              />
              <rect
                class="cls-4"
                x="39"
                y="7"
                width="2"
                height="11"
              />
              <rect
                class="cls-2"
                x="25"
                width="9"
                height="5"
              />
              <rect
                class="cls-2"
                x="25"
                y="20"
                width="9"
                height="5"
              />
              <polygon
                class="cls-1"
                points="54 7 53 7 53 6 52 6 52 5 51 5 51 4 50 4 50 1 53 1 53 2 54 2 54 3 55 3 55 4 56 4 56 5 57 5 57 12 54 12 54 7"
              />
              <rect
                class="cls-4"
                x="34"
                width="18"
                height="5"
              />
              <polygon
                class="cls-1"
                points="54 18 53 18 53 19 52 19 52 20 51 20 51 21 50 21 50 24 53 24 53 23 54 23 54 22 55 22 55 21 56 21 56 20 57 20 57 13 54 13 54 18"
              />
              <rect
                class="cls-4"
                x="34"
                y="20"
                width="18"
                height="5"
              />
            </g>
          </svg>
        </div>
      </div>
    </section>

    <section class="about">
      <main>
        <div class="container">
          <h1 class="titleAbout">
            About me
          </h1>

          <p style="margin:16px 0 40px;">
            I'm David, and I live in Brussels, Belgium. I recently completed my studies in applied computer science at Erasumus Hogeschool and I am looking for a job that combines my passion for design and technology.
          </p>

          <div class="about-wrapper">

            <div class="about-box">
              <div class="about-box__side">
                <h3>Contact</h3>
              </div>
              <div>
                <p>davidkahlenborn@gmail.com</p>
                <p>0032 488 72 78 23</p>
              </div>
            </div>

            <div class="about-box">
              <div class="about-box__side">
                <h3>Showcase</h3>
              </div>
              <div>
                <ul
                  v-for="s in showcase"
                  :key="s.linkName"
                  class="breadcrumb"
                >
                  <li>
                    <a
                      target="_blank"
                      :href="s.hostUrl"
                    >{{s.linkName}}</a>
                  </li>
                  <li>
                    <a
                      target="_blank"
                      :href="s.githubUrl"
                    >
                      Github
                    </a>
                  </li>
                </ul>

                <!--
                <ul class="breadcrumb">
                  
                  
                  
                  <li><a
                      target="_blank"
                      :href="showcase.landingPage.host"
                    >landingpage.herokuapp.com</a></li>
                  <li><a
                      target="_blank"
                      :href="showcase.landingPage.host"
                    >landingpage.herokuapp.com</a></li>
                  <li><a
                      target="_blank"
                      :href="showcase.landingPage.github"
                    >
                      Github
                    </a>
                  </li>
                </ul>

                <ul
                  class="breadcrumb"
                  style="padding: 0;"
                >
                  
                  <li><a
                      target="_blank"
                      :href="showcase.webshopPage.host"
                    >webshop.herokuapp.com</a></li>
                  <li><a
                      target="_blank"
                      :href="showcase.webshopPage.github"
                    >
                      Github
                    </a></li>
                </ul>
                -->
              </div>
            </div>

            <div class="about-box">
              <div class="about-box__side">
                <h3>Skills</h3>
              </div>
              <div>
                <div class="pills">
                  <header>
                    <div class="flex align-center">
                      <p>Knowledge</p>
                      <span class="primary"></span>
                    </div>
                    <div
                      class="flex align-center"
                      style="margin-left:12px;"
                    >
                      <p>Learning</p>
                      <span class="secondary"></span>
                    </div>
                  </header>
                  <main>
                    <div style="margin-bottom:12px;">
                      <span
                        v-for="k in skills.knowledge"
                        :key="k"
                        class="chip primary"
                      >{{ k }}</span>

                      <div style="margin:1rem;"></div>

                      <span
                        v-for="l in skills.learning"
                        :key="l"
                        class="chip secondary"
                      >{{ l }}</span>
                    </div>
                  </main>
                </div>
              </div>
            </div>
            <div class="about-box">
              <div class="about-box__side">
                <h3>Languages</h3>
              </div>
              <div>
                <ul class="breadcrumb">
                  <li>English</li>
                  <li>French</li>
                  <li>Dutch</li>
                  <li>German <span class="hide-xs">(native)</span></li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </main>
      <footer>
        <p>Made with Vue.js</p>
      </footer>
    </section>

  </div>
</template>

<script>
import PanelSnap from "panelsnap";
//import SvgTrack from "./components/SvgTrack";

export default {
  name: "App",
  components: {
    //HelloWorld
    //SvgTrack,
  },
  data: () => ({
    contact: {
      phone: "0032 488 72 78 23",
      email: "davidkahlenborn@gmail.com",
    },
    showcase: [
      {
        linkName: "Victoire Real Estate",
        hostUrl: "https://d-kah.github.io/victoire-real-estate/",
        githubUrl: "https://github.com/d-kah/victoire-real-estate",
      },
      {
        linkName: "landingpage.herokuapp.com",
        hostUrl: "https://nodalview-frontend.herokuapp.com/",
        githubUrl: "https://github.com/d-kah/nv-frontend",
      },
      {
        linkName: "webshop.herokuapp.com",
        hostUrl: "http://webshop-tutorial3.herokuapp.com/",
        githubUrl: "https://github.com/d-kah/nv-webshop",
      },
    ],

    skills: {
      knowledge: [
        "Javascript",
        "Typescript",
        "Vue.js",
        "Nuxt.js",
        "React",
        "SQL",
        "jQuery",
        "HTML5",
        "CSS / SCSS",
        "Bootstrap",
        "UX / UI Design",
        "Java",
        ".NET C#",
        "ASP.NET",
      ],
      learning: ["Node.js", "Express", "MongoDB", "Mongoose", "GraphQL"],
    },
    languages: ["English", "French", "Dutch", "German (Mother tongue)"],
  }),
  mounted() {
    // space dashes evenly on street circle.
    // console.log('Test here',this.$refs.stripesTest.getTotalLength() / 40);

    var options = {
      container: document.body,
      panelSelector: " section",
      directionThreshold: 10,
      delay: 0,
      duration: 800,
      easing: function (t) {
        return t;
      },
    };

    this.panelSnap = new PanelSnap(options);
  },
};
</script>

<style>
#app {
  font-family: "Inter", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  /*margin-top: 60px;*/
}

a:hover {
  color: var(--primary-color);
}

section {
  min-height: 100vh;

  z-index: 100;
}

.chip {
  display: inline-block;
  padding: 0.25em 0.4em;
  font-size: 0.8rem;
  letter-spacing: 0.015em;
  font-weight: 700;
  line-height: 1;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: 10rem;

  color: #fff;

  padding: 0.5rem !important;
  margin-bottom: 0.25rem !important;
  margin-right: 0.25rem !important;
}

.primary {
  background-color: var(--primary-color);
}

.secondary {
  background-color: var(--secondary-color);
}

.github-marker {
  height: 32px;
  width: 32px;
}

.github-marker:hover {
  fill: var(--primary-color);
}

ul.breadcrumb {
  list-style: none;
  padding: 0;
}
ul.breadcrumb li {
  display: inline;
}
ul.breadcrumb li + li:before {
  padding: 0.5em;
  color: black;
  content: "|\00a0";
}

.title {
  font-weight: 700;
  margin-bottom: 1vh;
  line-height: 1.25;
}

.subtitle {
  color: #292929;
  line-height: 1.25;
  margin-bottom: 1vh;
}

/*
  breakpoints: {
    values: {
      xs: 0,
      sm: 640, 
      md: 990, 
      lg: 1440, 
      xl: 1920
    }
  }
*/

#app {
  position: relative;
}

section {
  position: relative;
  z-index: 100;
  padding: 24px !important;
}

section.intro {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

section.about {
  display: flex;
  flex-direction: column;
}

section.about > main {
  flex: 1 0 auto;
}

section.about > footer {
  flex-shrink: 0;
  text-align: center;
  padding: 32px;
  font-weight: 600;
  opacity: 0.6;
  letter-spacing: 0.01em;
  font-size: 0.9rem;
}

.container {
  width: 100%;
  max-width: 888px;
  margin: 0 auto;
}

.titleAbout {
  font-weight: 600;
  font-style: normal;
  font-size: 48px;
}

.about-wrapper h3 {
  padding: 0;

  font-weight: 700;
  letter-spacing: -0.02em;
  font-size: 1.4rem;
  /*padding-top: calc(calc(calc(16px * 1.5) / 2) *0.75);
  padding-bottom: calc(var(--baseline)*0.25);*/
  /*margin-bottom: var(--baseline);*/
  line-height: 1.5rem;
  margin-bottom: 12px;
}

.about-box {
  display: flex;
  margin-bottom: 40px;
}

.about-box__side {
  min-width: 234px;
}

.pills {
  margin-bottom: 16px;
}

.pills > header {
  display: flex;
  align-items: center;
  margin-bottom: 16px;
}

.pills > header p {
  margin: 0;
}

.pills > header span {
  margin-left: 6px;
  padding: 10px;
  display: inline-block;
  font-size: 75%;
  font-weight: 700;
  line-height: 1;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: 10rem;
}

.flex {
  display: flex;
}

.align-center {
  align-items: center;
}

.primary {
  background: var(--primary-color);
}
.secondary {
  background: grey;
}

.hide-xs {
  visibility: visible;
}

@media only screen and (max-width: 639px) {
  .title {
    font-size: calc(1.25vw + 32px);
  }
  .subtitle {
    font-size: 20px;
  }
  .about-box {
    flex-direction: column;
  }
  .hide-xs {
    visibility: hidden;
  }

  .svg-wrapper {
    height: calc(40vw + 200px);
    width: calc(40vw + 200px);
  }
  .titleAbout {
    margin-top: 200px;
  }
}

@media only screen and (min-width: 640px) {
  .title {
    font-size: calc(2.28571vw + 25.37143px);
    margin-bottom: 1.5vh;
  }
  .subtitle {
    font-size: calc(0.57143vw + 16.34286px);
    margin-bottom: 1.5vh;
  }
  .svg-wrapper {
    height: calc(24vw + 300px);
    width: calc(24vw + 300px);
  }
  .titleAbout {
    margin-top: 320px;
  }
}

@media only screen and (min-width: 990px) {
  .title {
    font-size: calc(1.77384vw + 30.43902px);
    margin-bottom: 2vh;
  }
  .subtitle {
    font-size: calc(0.44346vw + 17.60976px);
    margin-bottom: 2vh;
  }

  .svg-wrapper {
    height: calc(18vw + 360px);
    width: calc(18vw + 360px);
  }
  .titleAbout {
    margin-top: 320px;
  }
}

@media only screen and (min-width: 1440px) {
  .title {
    font-size: calc(1.66667vw + 31.98333px);
  }
  .subtitle {
    font-size: 24px;
  }

  .svg-wrapper {
    height: calc(15vw + 410px);
    width: calc(15vw + 410px);
  }

  .titleAbout {
    margin-top: 320px;
  }
}

@media only screen and (min-width: 1920px) {
  .title {
    font-size: 64px;
  }

  .svg-wrapper {
    height: 700px;
    width: 700px;
  }
  .titleAbout {
    margin-top: 320px;
  }
}

.containerTest {
  position: absolute;
  bottom: 0;
}

.svg-wrapper {
  /*height: calc(20vw + 200px);
  width: calc(20vw + 200px);*/
  margin-bottom: -50%;
}

.svg-wrapper svg .stripes {
  fill: none;
  stroke: white;
  stroke-width: 4;
  stroke-dasharray: 20.737437438964843;
  stroke-dashoffset: 10.368718719482422;
}

.svg-wrapper svg .street {
  fill: none;
  stroke: grey;
  stroke-width: 70;
}

.svg-wrapper svg polygon {
  fill: orange;
}

@keyframes move {
  0% {
    offset-distance: 0%;
    motion-offset: 0%;
  }
  100% {
    offset-distance: 100%;
    motion-offset: 100%;
  }
}

.bike {
  offset-path: path("M180,48A132,132,0,1,1,48,180,132,132,0,0,1,180,48");
  animation: move 12s linear infinite;
}

.bike > .cls-1 {
  fill: #ea2f09;
}

.bike > .cls-2 {
  fill: #03b0d2;
}

.bike > .cls-3 {
  fill: #392c39;
}

.bike > .cls-4 {
  fill: #f9b38c;
}
</style>
