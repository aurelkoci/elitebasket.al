<script setup lang="ts">
const instaUrl = 'https://www.instagram.com/elite_basket_center/'

useHead({
  title: 'Elite Basket Center | Kurs Basketbolli',
  meta: [
    { name: 'description', content: '⛹🏻 Kurs Basketbolli për Djem & Vajza | 🏃 Personal Training | 📍 Shkolla Naim Frasheri' },
    { property: 'og:title', content: 'Elite Basket Center' },
    { property: 'og:description', content: 'Kurs Basketbolli për Djem & Vajza - Personal Training' },
    { property: 'og:image', content: 'https://scontent.cdninstagram.com/v/t51.2885-19/348720653_792526432281704_7090284363882871307_n.jpg' },
    { property: 'og:url', content: instaUrl },
    { name: 'viewport', content: 'width=device-width, initial-scale=1' },
    { name: 'theme-color', content: '#FF6B35' }
  ]
})

const photos = [
  '/foto/1.jpg',
  '/foto/2.jpg'
]
</script>

<template>
  <main class="container">
    <!-- Header -->
    <header class="header">
      <div class="profile-card">
        <img 
          src="https://scontent.cdninstagram.com/v/t51.2885-19/348720653_792526432281704_7090284363882871307_n.jpg?stp=dst-jpg_s150x150_tt6&_nc_cat=101&ccb=7-5&_nc_sid=f7ccc5&efg=eyJ2ZW5jb2RlX3RhZyI6InByb2ZpbGVfcGljLnd3dy45NTYuQzMifQ%3D%3D&_nc_ohc=QB15pY1pdzwQ7kNvwHMj0q3&_nc_oc=AdodRbM0_ktw857844rXUckjJAPdmQO-p1VZIed8pMjgX7hc8pVhyenUBl2kY5Tmgu0&_nc_zt=24&_nc_ht=scontent.cdninstagram.com&_nc_ss=7b689&oh=00_AQKAdNksg28DRjp4-cxqyXpYTRniB_dCzosvtpBIo4JyXA&oe=6A9B0F53"
          alt="Elite Basket Center"
          class="profile-pic"
        >
        <h1>Elite Basket Center</h1>
        <p class="tagline">⛹🏻 Kurs Basketbolli për Djem & Vajza ⛹🏼‍♀️</p>
        
        <div class="stats">
          <div class="stat">
            <strong>866</strong>
            <span>Followers</span>
          </div>
          <div class="stat">
            <strong>356</strong>
            <span>Following</span>
          </div>
        </div>
      </div>
    </header>

    <!-- Bio Section -->
    <section class="bio-section">
      <p class="bio-title">Ofrimet Tona</p>
      <ul class="features">
        <li>⛹️ Kurs Basketbolli për Djem & Vajza</li>
        <li>🏃 Personal Training</li>
        <li>📍 Shkolla "Naim Frasheri"</li>
      </ul>
    </section>

    <!-- Photos Gallery -->
    <section class="gallery" v-if="photos.length">
      <h2>Galerija</h2>
      <div class="photos-grid">
        <img 
          v-for="photo in photos" 
          :key="photo"
          :src="photo"
          :alt="`Elite Basket Center photo`"
          class="gallery-photo"
        >
      </div>
    </section>

    <!-- Contact Section -->
    <section class="contact-section">
      <h2>Na Kontaktoni</h2>
      <div class="contact-info">
        <p class="phone">📞 <a href="tel:+355698918330">+355 698 918 330</a></p>
        <p class="location">📍 Shkolla "Naim Frasheri"</p>
      </div>
      <a :href="instaUrl" target="_blank" rel="noopener" class="btn-instagram">
        Vizito Instagram
      </a>
    </section>
  </main>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.container {
  max-width: 600px;
  margin: 0 auto;
  padding: 2rem 1rem;
  min-height: 100dvh;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.header {
  text-align: center;
  margin-bottom: 2rem;
}

.profile-card {
  background: white;
  border-radius: 20px;
  padding: 2rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.profile-pic {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid #FF6B35;
  margin-bottom: 1rem;
}

h1 {
  font-size: 1.8rem;
  color: #333;
  margin-bottom: 0.5rem;
  font-family: system-ui, -apple-system, sans-serif;
}

.tagline {
  font-size: 1rem;
  color: #666;
  margin-bottom: 1.5rem;
}

.stats {
  display: flex;
  justify-content: space-around;
  margin-top: 1.5rem;
  border-top: 1px solid #eee;
  padding-top: 1.5rem;
}

.stat {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.25rem;
}

.stat strong {
  font-size: 1.4rem;
  color: #FF6B35;
}

.stat span {
  font-size: 0.8rem;
  color: #999;
}

.bio-section {
  background: white;
  border-radius: 20px;
  padding: 2rem;
  margin-bottom: 2rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.bio-title {
  font-size: 1.2rem;
  color: #333;
  margin-bottom: 1rem;
  font-weight: 600;
}

.features {
  list-style: none;
}

.features li {
  padding: 0.75rem 0;
  color: #555;
  font-size: 1rem;
  border-bottom: 1px solid #f0f0f0;
}

.features li:last-child {
  border-bottom: none;
}

.gallery {
  background: white;
  border-radius: 20px;
  padding: 2rem;
  margin-bottom: 2rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.gallery h2 {
  font-size: 1.3rem;
  color: #333;
  margin-bottom: 1.5rem;
}

.photos-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
}

.gallery-photo {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 15px;
  transition: transform 0.3s ease;
}

.gallery-photo:hover {
  transform: scale(1.05);
}

.contact-section {
  background: white;
  border-radius: 20px;
  padding: 2rem;
  text-align: center;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.contact-section h2 {
  font-size: 1.3rem;
  color: #333;
  margin-bottom: 1.5rem;
}

.contact-info {
  margin-bottom: 1.5rem;
}

.contact-info p {
  font-size: 1rem;
  color: #555;
  margin-bottom: 0.5rem;
}

.phone a {
  color: #FF6B35;
  text-decoration: none;
  font-weight: 600;
}

.phone a:hover {
  text-decoration: underline;
}

.btn-instagram {
  display: inline-block;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 0.8rem 2rem;
  border-radius: 25px;
  text-decoration: none;
  font-weight: 600;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
}

.btn-instagram:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(102, 126, 234, 0.6);
}
</style>
