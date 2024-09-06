<template>
  <div class="home">
    <div class="about container">
      <h1>BitHeart.org</h1>
      <div class="content">
        <p>BitHeart.org is an open organization focused on fundamental blockchain technology research, including Bitcoin, Ethereum, and more.</p>
        <p>Our mission is to contribute to the advancement of blockchain technology through in-depth research and innovation, and to promote its application across various fields.</p>
      </div>
    </div>

    <div class="research container">
      <h1>Research Areas</h1>
      <div class="research-areas">
        <div class="research-item" v-for="(item, index) in researchAreas" :key="index">
          <i :class="item.icon"></i>
          <h3>{{ item.title }}</h3>
          <p>{{ item.description }}</p>
        </div>
      </div>
    </div>

    <div class="contact container">
      <h1>Contact Us</h1>
      <div class="contact-info">
        <div class="contact-item">
          <i class="fas fa-envelope"></i>
          <p>info@bitheart.org</p>
        </div>
        <div class="contact-item">
          <i class="fab fa-github"></i>
          <p>github.com/bitheart-org</p>
        </div>
        <div class="contact-item">
          <i class="fab fa-twitter"></i>
          <p>@BitHeartOrg</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'HomePage',
  setup() {
    const researchAreas = ref([
      { icon: 'fas fa-bitcoin', title: 'Bitcoin Protocol Optimization', description: 'Research and improve the Bitcoin protocol to enhance its performance and security.' },
      { icon: 'fas fa-file-contract', title: 'Ethereum Smart Contract Security', description: 'Analyze and enhance the security of Ethereum smart contracts to reduce potential risks.' },
      { icon: 'fas fa-network-wired', title: 'Blockchain Scalability Solutions', description: 'Explore innovative methods to increase the throughput and efficiency of blockchain networks.' },
      { icon: 'fas fa-link', title: 'Cross-chain Technology Research', description: 'Develop and refine interoperability solutions between different blockchain networks.' },
      { icon: 'fas fa-coins', title: 'Decentralized Finance (DeFi) Applications', description: 'Research and develop new decentralized finance applications and protocols.' }
    ])

    return { researchAreas }
  }
}
</script>

<style scoped>
.home > div {
  margin-bottom: 60px;
}

.about, .research, .contact {
  padding: 40px 0;
}

h1 {
  text-align: center;
  margin-bottom: 30px;
}

.content {
  background-color: #ffffff;
  border-radius: 8px;
  padding: 30px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

.research-areas {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.research-item {
  background-color: #ffffff;
  border-radius: 8px;
  padding: 20px;
  text-align: center;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.research-item:hover {
  transform: translateY(-5px);
}

.research-item i {
  font-size: 48px;
  color: #3498db;
  margin-bottom: 15px;
}

.research-item h3 {
  margin-bottom: 10px;
}

.contact-info {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.contact-item {
  background-color: #ffffff;
  border-radius: 8px;
  padding: 20px;
  text-align: center;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  margin: 10px;
  flex: 1;
  min-width: 200px;
}

.contact-item i {
  font-size: 36px;
  color: #3498db;
  margin-bottom: 10px;
}
</style>

