<template>
  <div class="home-page">
    <!-- Hero Section -->
    <section class="hero">
      <div class="container">
        <div class="hero-content">
          <h1 class="hero-title">
            <span class="highlight">Windglass Apucarana</span><br>
            Soluções em Vidro com Qualidade e Elegância
          </h1>
          <p class="hero-subtitle">
            Transformamos ambientes com vidros temperados, espelhos, box para banheiro e muito mais. 
            Mais de 15 anos de experiência trazendo sofisticação e segurança para seu espaço.
          </p>
          <div class="hero-buttons">
            <NuxtLink to="/contato" class="btn-primary">Solicitar Orçamento</NuxtLink>
            <NuxtLink to="/produtos" class="btn-secondary">Ver Produtos</NuxtLink>
          </div>
        </div>
        <div class="hero-image">
          <div class="glass-showcase">
            <div class="glass-panel glass-1"></div>
            <div class="glass-panel glass-2"></div>
            <div class="glass-panel glass-3"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- Destaques Section -->
    <section class="destaques">
      <div class="container">
        <h2 class="section-title">Por que escolher a Windglass?</h2>
        
        <div class="destaques-grid">
          <div class="destaque-card">
            <div class="destaque-icon">✓</div>
            <h3>Mais de 15 anos</h3>
            <p>de experiência no mercado vidreiro</p>
          </div>

          <div class="destaque-card">
            <div class="destaque-icon">✓</div>
            <h3>Garantia Total</h3>
            <p>em todos os produtos e serviços</p>
          </div>

          <div class="destaque-card">
            <div class="destaque-icon">✓</div>
            <h3>Atendimento Rápido</h3>
            <p>orçamento sem compromisso</p>
          </div>

          <div class="destaque-card">
            <div class="destaque-icon">✓</div>
            <h3>Qualidade Certificada</h3>
            <p>produtos testados e aprovados</p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="cta-section">
      <div class="container">
        <h2>Pronto para transformar seu ambiente?</h2>
        <p>Entre em contato e solicite um orçamento personalizado</p>
        <div class="cta-buttons">
          <NuxtLink to="/portfolio" class="btn-white">Ver Nossos Trabalhos</NuxtLink>
          <NuxtLink to="/contato" class="btn-outline">Falar Conosco</NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  head() {
    return {
      title: 'Windglass Apucarana - Soluções em Vidro',
      meta: [
        { hid: 'description', name: 'description', content: 'Vidros temperados, espelhos e box para banheiro em Apucarana. Mais de 15 anos de experiência.' }
      ]
    }
  }
}
</script>

<style scoped>
.home-page {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

/* Hero Section */
.hero {
  background: linear-gradient(135deg, #1a365d 0%, #2c5282 50%, #1e40af 100%);
  padding: 140px 0 100px 0;
  color: white;
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg"><rect width="100" height="100" fill="none" stroke="rgba(255,255,255,0.05)" stroke-width="1"/></svg>');
  opacity: 0.3;
}

.hero .container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
  position: relative;
  z-index: 1;
}

.hero-content {
  animation: fadeInUp 1s ease-out;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 800;
  line-height: 1.2;
  margin-bottom: 1.5rem;
}

.highlight {
  color: #60a5fa;
  display: block;
}

.hero-subtitle {
  font-size: 1.25rem;
  line-height: 1.8;
  margin-bottom: 2.5rem;
  color: rgba(255, 255, 255, 0.9);
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.btn-primary, .btn-secondary, .btn-white, .btn-outline {
  padding: 1rem 2rem;
  text-decoration: none;
  border-radius: 10px;
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.3s ease;
  display: inline-block;
}

.btn-primary {
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  color: white;
  box-shadow: 0 10px 30px rgba(96, 165, 250, 0.3);
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 15px 40px rgba(96, 165, 250, 0.4);
}

.btn-secondary {
  background: rgba(255, 255, 255, 0.1);
  color: white;
  border: 2px solid rgba(255, 255, 255, 0.3);
  backdrop-filter: blur(10px);
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.2);
  border-color: rgba(255, 255, 255, 0.5);
}

.hero-image {
  display: flex;
  justify-content: center;
  align-items: center;
}

.glass-showcase {
  position: relative;
  width: 100%;
  height: 400px;
}

.glass-panel {
  position: absolute;
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.1) 0%, rgba(255, 255, 255, 0.05) 100%);
  border: 2px solid rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(10px);
  border-radius: 20px;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
}

.glass-1 {
  width: 280px;
  height: 350px;
  top: 0;
  left: 50px;
  transform: rotate(-5deg);
  animation: float 6s ease-in-out infinite;
}

.glass-2 {
  width: 260px;
  height: 320px;
  top: 40px;
  right: 20px;
  transform: rotate(5deg);
  animation: float 6s ease-in-out infinite 1s;
}

.glass-3 {
  width: 200px;
  height: 280px;
  bottom: 20px;
  left: 120px;
  transform: rotate(-3deg);
  animation: float 6s ease-in-out infinite 2s;
}

@keyframes float {
  0%, 100% {
    transform: translateY(0) rotate(var(--rotation, 0deg));
  }
  50% {
    transform: translateY(-20px) rotate(var(--rotation, 0deg));
  }
}

/* Destaques Section */
.destaques {
  padding: 100px 0;
  background: #f8fafc;
}

.section-title {
  font-size: 2.5rem;
  font-weight: 700;
  text-align: center;
  color: #1e293b;
  margin-bottom: 4rem;
}

.destaques-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.destaque-card {
  background: white;
  padding: 3rem 2rem;
  border-radius: 20px;
  text-align: center;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  border: 1px solid #e2e8f0;
}

.destaque-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
}

.destaque-icon {
  width: 70px;
  height: 70px;
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1.5rem auto;
  font-size: 2rem;
  box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
}

.destaque-card h3 {
  font-size: 1.5rem;
  color: #1e293b;
  margin-bottom: 0.5rem;
  font-weight: 700;
}

.destaque-card p {
  color: #64748b;
  line-height: 1.6;
}

/* CTA Section */
.cta-section {
  padding: 100px 0;
  background: linear-gradient(135deg, #1e40af 0%, #1e3a8a 100%);
  color: white;
  text-align: center;
}

.cta-section h2 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.cta-section p {
  font-size: 1.25rem;
  margin-bottom: 2.5rem;
  color: rgba(255, 255, 255, 0.9);
}

.cta-buttons {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.btn-white {
  background: white;
  color: #1e40af;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.btn-white:hover {
  transform: translateY(-3px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
}

.btn-outline {
  background: transparent;
  color: white;
  border: 2px solid white;
}

.btn-outline:hover {
  background: rgba(255, 255, 255, 0.1);
}

/* Responsive */
@media (max-width: 768px) {
  .hero .container {
    grid-template-columns: 1fr;
  }
  
  .hero-title {
    font-size: 2.5rem;
  }
  
  .hero-image {
    display: none;
  }
  
  .section-title {
    font-size: 2rem;
  }
  
  .cta-section h2 {
    font-size: 2rem;
  }
}
</style>
    