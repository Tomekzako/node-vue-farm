<template>
  <figure class="card">
    <div class="card__emoji">{{product.image}}{{product.image}}</div>

    <div class="card__title-box">
      <h2 class="card__title">{{product.productName}}</h2>
    </div>

    <div class="card__details">
      <div class="card__detail-box" v-if="product.organic">
        <h6 class="card__detail card__detail--organic">Organic!</h6>
      </div>

      <div class="card__detail-box">
        <h6 class="card__detail">{{product.quantity}} per 📦</h6>
      </div>

      <div class="card__detail-box">
        <h6 class="card__detail card__detail--price">{{product.price}}</h6>
      </div>
    </div>

    <a class="card__link" href="#">
      <span>Detail <i class="emoji-right">👉</i></span>
    </a>
  </figure>
</template>

<script>
export default {
  props: ['product']
}
</script>


<style>
.card {
  background: white;
  box-shadow: 0 2rem 6rem 1rem rgba(0, 0, 0, 0.15);
  margin-bottom: 5rem;
  transform: skewX(-20deg);
  display: flex;
  transition: all 0.5s;
  cursor: pointer;
}

.card__emoji {
  font-size: 5.5rem;
  line-height: 1.2;
  padding: 1.5rem 6rem 0.5rem 1.5rem;
  letter-spacing: -4rem;
  transform: skewX(20deg);
}

.card__title-box {
  background: linear-gradient(to bottom, #9be15d, #00e3ae);
  margin-right: auto;
  display: flex;
  align-items: center;
  padding: 0 3rem;
}

.card__title {
  font-family: "Megrim", sans-serif;
  color: white;
  font-size: 3.25rem;
  transform: skewX(20deg);
}

.card__details {
  display: flex;
}

.card__detail-box {
  align-self: stretch;
  border-right: 1px solid #ddd;
  display: flex;
  align-items: center;
}

.card__detail-box:last-child {
  border: none;
}

.card__detail {
  font-weight: 400;
  font-size: 1.8rem;
  transform: skewX(20deg);
  padding: 1.75rem;
}

.card__detail--organic {
  font-weight: 900;
  text-transform: uppercase;
  font-size: 1.9rem;
  background-image: linear-gradient(to right, #9be15d, #00e3ae);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.card__detail--price {
  font-weight: 900;
  font-size: 1.9rem;
}

.card__link:link,
.card__link:visited {
  flex: 0 0 auto;
  background-color: #79e17b;
  color: white;
  font-size: 1.6rem;
  font-weight: 900;
  text-transform: uppercase;
  text-decoration: none;
  padding: 2.5rem;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s;
}

.card__link:hover,
.card__link:active {
  background-color: #9be15d;
}

.card__link span {
  transform: skewX(20deg);
}

.card:hover {
  transform: skewX(-20deg) scale(1.08);
  box-shadow: 0 3rem 8rem 2rem rgba(0, 0, 0, 0.15);
}

.emoji-left {
  font-size: 2rem;
  margin-right: 1rem;
}

.emoji-right {
  font-size: 2rem;
  margin-left: 1rem;
}

.not-organic {
  display: none;
}
</style>
