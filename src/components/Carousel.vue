<template>
  <div class="carousel">
    <div class="in">
      <header class="app">
        <h1>Vue Carousel</h1>
      </header>
      <div class="slider-outer">
        <div class="slider">
          <div class="slider-inner">
            <div class="slide">
              <img src="../assets/images/slide1.jpg" alt class="slide-img">
              <div class="slide-content">
                <h2 class="slide-title">Slide 1</h2>
                <h3 class="slide-description">Some words about slide 1</h3>
              </div>
            </div>

            <div class="slide">
              <img src="../assets/images/slide2.jpg" alt class="slide-img">
              <div class="slide-overlay"></div>
              <div class="slide-content">
                <h2 class="slide-title">Slide 2</h2>
                <h3 class="slide-description">Some words about slide 2</h3>
              </div>
            </div>

            <div class="slide">
              <img src="../assets/images/slide3.jpg" alt class="slide-img">
              <div class="slide-overlay"></div>
              <div class="slide-content">
                <h2 class="slide-title">Slide 3</h2>
                <h3 class="slide-description">Some words about slide 3</h3>
              </div>
            </div>

            <div class="slide">
              <img src="../assets/images/slide4.jpg" alt class="slide-img">
              <div class="slide-overlay"></div>
              <div class="slide-content">
                <h2 class="slide-title">Slide 4</h2>
                <h3 class="slide-description">Some words about slide 4</h3>
              </div>
            </div>
          </div>

          <div class="slider-nav">
            <div class="prev">&#x2039;</div>
            <div class="next">&#x203A;</div>
          </div>

          <div class="indicators">
            <ul class="indicator-dots">
              <li class="indicator-dot"></li>
              <li class="indicator-dot"></li>
              <li class="indicator-dot"></li>
              <li class="indicator-dot"></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Carousel",
  props: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.slider-outer {
  width: 80%;
  height: auto;
  max-width: 25rem;
  margin: 0 auto;
  box-sizing: border-box;
  z-index: 10;
}

.slider {
  overflow: hidden;
}

.slider-inner {
  display: flex;
  width: 400%;
  max-width: 100rem;
  overflow: hidden;
}

.slide {
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  max-width: 25rem;
}

.slide-img {
  width: 100%;
  height: auto;
}

.slide-content {
  position: absolute;
  top: 42.5%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #fff;
}

.slider-nav {
  position: absolute;
  top: 42.5%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
  max-width: 25rem;
  display: flex;
  flex-wrap: nowrap;
  color: #fff;
  z-index: 30;
}

.prev,
.next {
  flex: 1 0 50%;
  width: 50%;
  font-size: 2rem;
  transition: ease-in-out 0.3s;
}

.prev:hover,
.next:hover {
  color: rgba(255, 255, 255, 0.5);
}

.prev {
  text-align: left;
  padding-left: 1rem;
  box-sizing: border-box;
}

.next {
  text-align: right;
  padding-right: 1rem;
  box-sizing: border-box;
}

.indicator-dots {
  position: relative;
  top: -2.25rem;
  left: 0;
  display: flex;
  justify-content: center;
  list-style-type: none;
  background-color: transparent;
  margin: -0.5rem 0 0;
  padding: 1rem;
  box-sizing: border-box;
  z-index: 10;
}

.indicator-dot {
  width: 8px;
  height: 8px;
  margin-right: 0.5rem;
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 0.9);
  transition: ease-in-out 0.3s;
}

.indicator-dot:active,
.indicator-dot:hover {
  background-color: rgba(255, 255, 255, 0.5);
}

.indicator-dot:last-child {
  margin-right: 0;
}
</style>
