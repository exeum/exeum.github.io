<template>
  <div class="d-block member mb-5 mb-md-0">
    <div class="d-flex d-md-block">
      <img :src="data.photo" class="align-self-start photo" />
      <div class="align-self-start flex-grow-1">
        <div class="name">{{ data.name }}</div>
        <div class="position">{{ data.position }}</div>
      </div>
    </div>
    <div class="bio">
      {{ data.bio }}
    </div>
  </div>
</template>

<script>

export default {
  name: 'Team',
  data () {
    return {}
  },
  props: ['data']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../scss/res.scss";

.member {
  width: $feature-width;

  @media (max-width: 767px) { // sm, xs
    width: 100%;
    padding-left: 1rem;
    padding-right: 1rem;
  }
}

.photo {
  width: 100%;

  @media (max-width: 767px) { // sm, xs
    width: 120px;
  }
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.name {
  @extend %h6;
  text-align: left;
  padding-left: 0rem;
  padding-right: 0rem;
  padding-top: $member-name-pt;
  padding-bottom: $member-name-pb;

  @media (max-width: 767px) { // sm, xs
    width: 100%;
    padding-left: $member-name-sm-pl;
    padding-top: $member-name-sm-pt;
    padding-bottom: $member-name-sm-pb;
  }
}

.position {
  @extend %subtitle2;
  text-align: left;
  padding-left: 0rem;
  padding-right: 0rem;
  padding-top: $member-position-pt;
  padding-bottom: $member-position-pb;

  @media (max-width: 767px) { // sm, xs
    width: 100%;
    padding-left: $member-position-sm-pl;
    padding-top: $member-name-sm-pt;
    padding-bottom: $member-name-sm-pb;
  }
}

.bio {
  @extend %body2;
  text-align: left;
  padding-left: 0rem;
  padding-right: 0rem;

  @media (max-width: 767px) { // sm, xs
    width: 100%;
    text-align: left;
    padding-left: 0rem;
    padding-right: 0rem;
    padding-top: 0.5rem;
  }
}

</style>
