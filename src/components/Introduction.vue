<template>
  <!-- <section :style="myStyles"> -->
  <section>
    <div class="d-block header">
      <img src="../assets/images/logo-full.svg" />
      <div class="subtitle1">
        Decentralized Financial Platform
      </div>
      <div class="subtitle2">
        for Price-Stable Cryptocurrencies
      </div>
    </div>
    <div class="body">
      <div class="msg">
        Exeum is a decentralized financial platform on which people can trade special financial derivatives used for backing up price-stable cryptocurrencies (a.k.a stablecoins). Powered by the Exeum platform, any price-stable real world asset can become a stablecoin.
      </div>
      <div class="d-flex justify-content-center buttons">
        <a :href="whitepaperUrl" target="_blank" class="btn btn-primary mr-1" >Read Whitepaper</a>
        <a  :href="subscriptionUrl" target="_blank" class="btn btn-secondary btn-exeum ml-1">Subscribe for Update</a>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: 'Introduction',
  data () {
    return {
      whitepaperUrl: 'https://arxiv.org/pdf/1808.03482.pdf',
      subscriptionUrl: 'https://exeum.us19.list-manage.com/subscribe?u=a412c99ae6213101c313c875c&id=c8204190ae',
      window: {
        width: 0,
        height: 0
      }
    }
  },
  created () {
    window.addEventListener('resize', this.handleResize)
    this.handleResize();
  },
  destroyed () {
    window.removeEventListener('resize', this.handleResize)
  },
  methods: {
    handleResize () {
      this.window.width = window.innerWidth
      this.window.height = window.innerHeight - 73
    }
  },
  computed: {
    myStyles () {
      return {
        height: `${this.window.height}px`
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../scss/res.scss";

section > div.body {
  background: #F5F4F4;
}

img {
  width: 480px;

  @media (max-width: 767px) { // sm, xs
    width: 80%;
  }
}

.subtitle1 {
  @extend %h5;
  padding-top: 2rem;
}

.subtitle2 {
  @extend %body1;
  padding-top: 1rem;
}

.msg {
  @extend %body2;
  padding-left: 0rem;
  padding-right: 0rem;
  max-width: $max-contents-width;

  @media (min-width: 768px) and (max-width: 991px) { // md
    max-width: $max-contents-width-md;
    padding-left: 1rem;
    padding-right: 1rem;
  }

  @media (max-width: 767px) { // sm, xs
    max-width: $max-contents-width-sm;
    padding-left: 2rem;
    padding-right: 2rem;
  }
}

.buttons {
  padding-top: 2rem;
}
</style>
