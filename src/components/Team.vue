<template>
  <section>
    <div class="d-block header">
      <div class="title">
        Team
      </div>
      <div class="briefing">
        Exeum is an open source project run by passionate members who believe in the vision of a truly decentralized economy. To fairly reward contributions by new and existing team members, the team has adopted a dynamic 'token' share model - everyone is rewarded on a slicing pie basis within the allocated amount of Exeum tokens for the initial development (and partly in cash as soon as the project gets funded). Join the team and help us make financial stability a common resource, which will fundamentally change the lives of many people in developing countries.
      </div>
      <div class="briefing">
        Members who do not have conflict of interest issues are listed below:
      </div>
    </div>
    <div class="body">
      <div class="d-flex flex-column flex-md-row justify-content-between mb-3 mb-md-5" v-for="row in members" :key="row.id">
        <Member :data="member" v-for="member in row.data" :key="member.id"/>
      </div>
    </div>
  </section>
</template>

<script>
import Member from '@/components/Member.vue'

export default {
  name: 'Team',
  data () {
    return {
      members: [
        {
          id: 0,
          data: [
            {
              id: 0,
              name: 'Jaehyung Lee',
              position: 'Founder',
              bio: 'Jaehyung was the co-founder and CTO at Enswers Inc., which was acquired by Gracenote in 2015. He has 15+ years of industry experience, handling systems serving millions of multimedia queries per second, and has been a crypto enthusiast since 2014, personally investing in projects such as BitShares. Jaehyung received his B.S. (summa cum laude) in Computer Science and Ph.D. in Bio and Brain Engineering at KAIST, and is an inventor of over 30 patents including eight in the US.',
              photo: require('@/assets/images/gloine.jpg')
            },
            {
              id: 1,
              name: 'Minhyung Cho',
              position: 'Co-Founder / Research',
              bio: 'Minhyung was most recently a Principal Research Engineer at Gracenote with over 10+ years of industry experience in applying machine learning techniques to production. He presented two geometric optimization papers on deep learning at NIPS in 2015 and 2017. For over 3 years, Minhyung has been working on algorithmic trading in his spare time and is deeply interested in machine learning driven market making strategies. Minhyung completed his B.S. in Electrical and Computer Engineering at Seoul National University and M.S. in Biosystems at KAIST.',
              photo: require('@/assets/images/mhcho.jpg')
            },
            {
              id: 2,
              name: 'Sherman Li',
              position: 'Co-Founder / Business Development',
              bio: 'Sherman was most recently the VP of Video Personalization at Gracenote and currently supports the business development needs of Exeum. He was the co-founder and COO/CFO for Enswers (acquired by Gracenote in 2015), CEO of Soompi (acquired by Crunchyroll in 2014), Entrepreneur-in-Residence at Softbank Ventures, co-founder of Evixar (acquired by LG Telecom in 2005), and received his degree in Computer Systems Engineering from Stanford University in 2003.',
              photo: require('@/assets/images/Sherman.jpg')
            }
          ]
        },
        {
          id: 1,
          data: [
            {
              id: 0,
              name: 'Yongsun Choi',
              position: 'Co-Founder / Product Management',
              bio: 'Yongsun is currently the CEO of Extales, a startup developing web/app services and white-labeled cryptocurrency solutions, such as multicoin wallets and crypto price monitoring apps. Prior to Extales, he was a Senior Engineer at Samsung Electronics and (co-)founded a number of startup companies, including a venture focused on Equity Linked Security (ELS) management systems. Yongsun received B.S. / M.S. in EECS and Ph.D. in Bio and Brain Engineering at KAIST.',
              photo: require('@/assets/images/ever4cys.jpg')
            },
            {
              id: 1,
              name: 'Jinchul Jung',
              position: 'Co-Founder / Engineering',
              bio: 'Jinchul is the CTO of Extales, a startup developing white-labeled blockchain solutions. Prior to Extales, he co-founded Moment, a location-based social media service startup. He has 10+ years of software development experience, including messaging services on a cellular network and advanced IME software for Android mobile devices (embedded in Samsung Galaxy S3). Jinchul received both B.S. and M.S. in Computer Science & Engineering at Incheon National University.',
              photo: require('@/assets/images/mario.jpg')
            },
            {
              id: 2,
              name: 'Jihye Ahn',
              position: 'Co-Founder / Design',
              bio: 'Jihye specializes in UI/UX design at Extales. Her portfolio includes logo, background image, layout and UX design for a number of mobile games, apps, and websites. She is as interested in illustration as graphic design, and focused on representing the concept of Exeum in a unique logo that visualized the connection between the real world and the decentralized economy. Jihye received a B.S. degree in Motion Art Design at Namseoul University.',
              photo: require('@/assets/images/anji.jpg')
            }
          ]
        }
      ]
    }
  },
  components: {
    Member
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../scss/res.scss";

section > div.body {
  background-color: #f5f4f4
}

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
