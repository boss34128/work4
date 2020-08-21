<template>
  <div id="app">
    <Carousel />
    <div>
      <div class="container marketing">
        <br>
        <hr class="featurette-divider" />
        <br>
        <div class="row featurette">
          <div class="col-md-7 order-md-2 wen">
            <div>
              <h2 class="featurette-heading">@Group</h2>

              <p class="lead">Best friend forever</p>

              <Counter @cc="sum" />
              <br />
              {{total}}
            </div>
          </div>
          <div class="col-md-5 order-md-1">
            <img class="card-img top card" src="./assets/1.jpg" />
          </div>
        </div>
        <br>
        <hr class="featurette-divider" />
        <br>
      
        <div class="row featurette">
          <div class="col-md-7 wen">
            <div>
              <h2 class="featurette-heading">@Game</h2>
              <p class="lead">I think it's a game of finger skills.</p>

              <Counter @bb="sun" />
              <br />
              {{total}}
            </div>
          </div>
          <div class="col-md-5">
            <img class="card-img top cark" src="./assets/3.png" />
          </div>
        </div>
        <hr class="featurette-divider" /><br>
      </div>
    </div>
  </div>
</template>

<script>
import Counter from "./components/Counter";
import Carousel from "./components/Carousel";

export default {
  name: "App",
  components: {
    Counter,
    Carousel,
  },

  data: function () {
    return {
      total: 0,
    };
  },

  methods: {
    sum(counterValue) {
      this.total += counterValue;
    },
    sun(counterValue) {
      this.total += counterValue;
    },
  },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.card {
  width: 450px;
}
.cark {
  width: 450px;
}
.wen {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>