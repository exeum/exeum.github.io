<template>
  <section>
    <div class="d-block header">
      <div class="title">
        What is Exeum?
      </div>
      <div class="briefing">
        Carbon is a trustless stable cryptocurrency which closely correlates with the US Dollar. This is achieved through algorithmically adjusting coin supply based on the demand.
      </div>
    </div>
    <div class="body">
      <div class="d-flex flex-column flex-md-row justify-content-between">
        <div class="d-flex flex-row flex-md-column feature mb-5 mb-md-0" v-for="item in items" :key="item.id">
          <img :src="item.image" class="align-self-start symbol" />
          <div class="align-self-center flex-grow-1">
            <p class="name">{{ item.title }}</p>
            <p class="description"> {{ item.description }} </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: 'Features',
  data () {
    return {
      items: [
        {
          id: 0,
          image: require('@/assets/images/cash.svg'),
          title: 'Immediate Issuance',
          description: 'Pay in Exeum tokens and immediately receive stablecoins. No market fluctuations due to limited supply.'
        },
        {
          id: 1,
          image: require('@/assets/images/piggy-bank.svg'),
          title: 'Zero Hidden Costs',
          description: 'No hidden costs. No stability fees, no dynamic transaction fees nor automatic liquidations due to black swan events.'
        },
        {
          id: 2,
          image: require('@/assets/images/network.svg'),
          title: 'Decentralized End-to-End',
          description: 'Collateral, price feed, and finally, market making - the point of hidden centralized control. Become an arbitrage miner and join the force!'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../scss/res.scss";

section > div.body {
  background-color: #F5F4F4
}

.feature {
  width: $feature-width;

  @media (max-width: 767px) { // sm, xs
    width: 100%;
    padding-left: 1rem;
    padding-right: 1rem;
  }
}

.symbol {
  width: 120px;
  margin-left: auto;
  margin-right: auto;

  @media (max-width: 767px) { // sm, xs
    width: 100px;
  }
}

.name {
  @extend %h6;
  text-align: center;
  padding-left: 0rem;
  padding-right: 0rem;
  padding-top: 1rem;

  @media (max-width: 767px) { // sm, xs
    width: 100%;
    text-align: left;
    padding-left: 1rem;
    padding-right: 0rem;
  }
}

.description {
  @extend %body2;
  text-align: left;
  padding-left: 1rem;
  padding-right: 0rem;

  @media (max-width: 767px) { // sm, xs
    width: 100%;
    text-align: left;
    padding-left: 1rem;
    padding-right: 0rem;
    margin: 0rem;
  }
}
</style>
