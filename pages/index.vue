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
    <!-- Hero Section -->
    <section id="inicio" class="hero">
      <div class="container">
        <div class="hero-content">
          <h1 class="hero-title">
            <span class="highlight">Soluções em Vidro</span><br>
            com Qualidade e Elegância
          </h1>
          <p class="hero-subtitle">
            A Windglass Apucarana oferece os melhores produtos e serviços em vidros temperados,
            espelhos, box para banheiro e muito mais. Transforme seu ambiente com sofisticação.
          </p>
          <div class="hero-buttons">
            <a href="#contato" class="btn-primary">Solicitar Orçamento</a>
            <a href="#produtos" class="btn-secondary">Ver Produtos</a>
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

    <!-- Produtos Section -->
    <section id="produtos" class="produtos">
      <div class="container">
        <h2 class="section-title">Nossos Produtos</h2>
        <p class="section-subtitle">Qualidade e durabilidade em cada detalhe</p>
        
        <div class="produtos-grid">
          <div class="produto-card">
            <div class="produto-icon">
              <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect x="4" y="4" width="16" height="16" stroke="currentColor" stroke-width="2"/>
                <path d="M4 4L20 20M20 4L4 20" stroke="currentColor" stroke-width="1" opacity="0.3"/>
              </svg>
            </div>
            <h3>Vidros Temperados</h3>
            <p>Vidros de alta resistência e segurança para portas, janelas e divisórias. 5x mais resistente que vidro comum.</p>
          </div>

          <div class="produto-card">
            <div class="produto-icon">
              <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect x="6" y="4" width="12" height="16" stroke="currentColor" stroke-width="2" rx="1"/>
                <path d="M9 4V20M15 4V20" stroke="currentColor" stroke-width="1" opacity="0.4"/>
              </svg>
            </div>
            <h3>Box para Banheiro</h3>
            <p>Box personalizados com vidro temperado de 8mm, perfis de alumínio e acabamento impecável.</p>
          </div>

          <div class="produto-card">
            <div class="produto-icon">
              <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect x="4" y="4" width="16" height="16" stroke="currentColor" stroke-width="2"/>
                <circle cx="12" cy="12" r="3" stroke="currentColor" stroke-width="2"/>
              </svg>
            </div>
            <h3>Espelhos</h3>
            <p>Espelhos sob medida para banheiros, salas e ambientes corporativos com instalação profissional.</p>
          </div>

          <div class="produto-card">
            <div class="produto-icon">
              <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect x="3" y="6" width="8" height="12" stroke="currentColor" stroke-width="2"/>
                <rect x="13" y="6" width="8" height="12" stroke="currentColor" stroke-width="2"/>
              </svg>
            </div>
            <h3>Portas de Vidro</h3>
            <p>Portas de correr, pivotantes e batentes em vidro temperado para ambientes modernos.</p>
          </div>

          <div class="produto-card">
            <div class="produto-icon">
              <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <rect x="4" y="8" width="16" height="10" stroke="currentColor" stroke-width="2"/>
                <line x1="4" y1="13" x2="20" y2="13" stroke="currentColor" stroke-width="2"/>
              </svg>
            </div>
            <h3>Guarda-Corpos</h3>
            <p>Guarda-corpos de vidro temperado para sacadas, escadas e mezaninos com total segurança.</p>
          </div>

          <div class="produto-card">
            <div class="produto-icon">
              <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M4 4H20V14H4V4Z" stroke="currentColor" stroke-width="2"/>
                <rect x="7" y="14" width="10" height="6" stroke="currentColor" stroke-width="2"/>
              </svg>
            </div>
            <h3>Tampos de Vidro</h3>
            <p>Tampos para mesas, balcões e móveis planejados com bordas lapidadas e polidas.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Serviços Section -->
    <section id="servicos" class="servicos">
      <div class="container">
        <h2 class="section-title">Nossos Serviços</h2>
        <p class="section-subtitle">Do projeto à instalação, cuidamos de tudo</p>
        
        <div class="servicos-grid">
          <div class="servico-item">
            <div class="servico-number">01</div>
            <h3>Consultoria Personalizada</h3>
            <p>Atendimento especializado para escolher o melhor produto para seu projeto.</p>
          </div>

          <div class="servico-item">
            <div class="servico-number">02</div>
            <h3>Medição no Local</h3>
            <p>Profissionais qualificados realizam a medição precisa em sua residência ou empresa.</p>
          </div>

          <div class="servico-item">
            <div class="servico-number">03</div>
            <h3>Fabricação Sob Medida</h3>
            <p>Cada peça é fabricada especialmente para seu projeto com tecnologia de ponta.</p>
          </div>

          <div class="servico-item">
            <div class="servico-number">04</div>
            <h3>Instalação Profissional</h3>
            <p>Equipe técnica experiente garante instalação perfeita e segura.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Diferenciais Section -->
    <section class="diferenciais">
      <div class="container">
        <h2 class="section-title">Por que escolher a Windglass?</h2>
        
        <div class="diferenciais-grid">
          <div class="diferencial">
            <div class="diferencial-icon">✓</div>
            <h4>Mais de 15 anos</h4>
            <p>de experiência no mercado</p>
          </div>

          <div class="diferencial">
            <div class="diferencial-icon">✓</div>
            <h4>Garantia Total</h4>
            <p>em todos os produtos</p>
          </div>

          <div class="diferencial">
            <div class="diferencial-icon">✓</div>
            <h4>Atendimento Rápido</h4>
            <p>e orçamento sem compromisso</p>
          </div>

          <div class="diferencial">
            <div class="diferencial-icon">✓</div>
            <h4>Qualidade Certificada</h4>
            <p>produtos testados e aprovados</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contato Section -->
    <section id="contato" class="contato">
      <div class="container">
        <div class="contato-content">
          <div class="contato-info">
            <h2>Entre em Contato</h2>
            <p>Solicite um orçamento sem compromisso ou tire suas dúvidas com nossa equipe.</p>
            
            <div class="contato-items">
              <div class="contato-item">
                <div class="contato-icon">📞</div>
                <div>
                  <h4>Telefone</h4>
                  <p>(43) 3422-XXXX</p>
                </div>
              </div>

              <div class="contato-item">
                <div class="contato-icon">📱</div>
                <div>
                  <h4>WhatsApp</h4>
                  <p>(43) 9 9999-XXXX</p>
                </div>
              </div>

              <div class="contato-item">
                <div class="contato-icon">📍</div>
                <div>
                  <h4>Endereço</h4>
                  <p>Apucarana - PR</p>
                </div>
              </div>

              <div class="contato-item">
                <div class="contato-icon">🕐</div>
                <div>
                  <h4>Horário</h4>
                  <p>Seg-Sex: 8h-18h | Sáb: 8h-12h</p>
                </div>
              </div>
            </div>
          </div>

          <div class="contato-form">
            <h3>Solicite seu Orçamento</h3>
            <form>
              <input type="text" placeholder="Seu nome" class="form-input" />
              <input type="tel" placeholder="Telefone" class="form-input" />
              <input type="email" placeholder="E-mail" class="form-input" />
              <textarea placeholder="Descreva seu projeto" class="form-textarea" rows="4"></textarea>
              <button type="submit" class="form-button">Enviar Mensagem</button>
            </form>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="container">
        <p>&copy; 2025 Windglass Apucarana - Todos os direitos reservados</p>
        <p class="footer-tagline">Transformando ambientes com elegância e segurança</p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.windglass-page {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  overflow-x: hidden;
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

.btn-primary, .btn-secondary {
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

/* Produtos Section */
.produtos {
  padding: 100px 0;
  background: #f8fafc;
}

.section-title {
  font-size: 2.5rem;
  font-weight: 700;
  text-align: center;
  color: #1e293b;
  margin-bottom: 1rem;
}

.section-subtitle {
  font-size: 1.125rem;
  text-align: center;
  color: #64748b;
  margin-bottom: 4rem;
}

.produtos-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.produto-card {
  background: white;
  padding: 2.5rem;
  border-radius: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  border: 1px solid #e2e8f0;
}

.produto-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
}

.produto-icon {
  width: 60px;
  height: 60px;
  color: #3b82f6;
  margin-bottom: 1.5rem;
}

.produto-icon svg {
  width: 100%;
  height: 100%;
}

.produto-card h3 {
  font-size: 1.5rem;
  color: #1e293b;
  margin-bottom: 1rem;
  font-weight: 700;
}

.produto-card p {
  color: #64748b;
  line-height: 1.7;
  font-size: 1rem;
}

/* Serviços Section */
.servicos {
  padding: 100px 0;
  background: white;
}

.servicos-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 3rem;
}

.servico-item {
  text-align: center;
}

.servico-number {
  width: 80px;
  height: 80px;
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  color: white;
  font-size: 2rem;
  font-weight: 700;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1.5rem auto;
  box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
}

.servico-item h3 {
  font-size: 1.25rem;
  color: #1e293b;
  margin-bottom: 0.75rem;
  font-weight: 700;
}

.servico-item p {
  color: #64748b;
  line-height: 1.6;
}

/* Diferenciais Section */
.diferenciais {
  padding: 100px 0;
  background: linear-gradient(135deg, #1e40af 0%, #1e3a8a 100%);
  color: white;
}

.diferenciais-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 3rem;
  margin-top: 3rem;
}

.diferencial {
  text-align: center;
}

.diferencial-icon {
  width: 60px;
  height: 60px;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1rem auto;
  font-size: 2rem;
  border: 2px solid rgba(255, 255, 255, 0.3);
}

.diferencial h4 {
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
  font-weight: 700;
}

.diferencial p {
  color: rgba(255, 255, 255, 0.8);
}

/* Contato Section */
.contato {
  padding: 100px 0;
  background: #f8fafc;
}

.contato-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
}

.contato-info h2 {
  font-size: 2.5rem;
  color: #1e293b;
  margin-bottom: 1rem;
  font-weight: 700;
}

.contato-info > p {
  color: #64748b;
  font-size: 1.125rem;
  margin-bottom: 3rem;
  line-height: 1.7;
}

.contato-items {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.contato-item {
  display: flex;
  gap: 1.5rem;
  align-items: flex-start;
}

.contato-icon {
  width: 50px;
  height: 50px;
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  flex-shrink: 0;
}

.contato-item h4 {
  color: #1e293b;
  font-size: 1.125rem;
  margin-bottom: 0.25rem;
  font-weight: 700;
}

.contato-item p {
  color: #64748b;
  font-size: 1rem;
}

.contato-form {
  background: white;
  padding: 3rem;
  border-radius: 20px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
}

.contato-form h3 {
  font-size: 1.75rem;
  color: #1e293b;
  margin-bottom: 2rem;
  font-weight: 700;
}

.form-input, .form-textarea {
  width: 100%;
  padding: 1rem;
  margin-bottom: 1.5rem;
  border: 2px solid #e2e8f0;
  border-radius: 10px;
  font-size: 1rem;
  font-family: inherit;
  transition: border-color 0.3s ease;
}

.form-input:focus, .form-textarea:focus {
  outline: none;
  border-color: #3b82f6;
}

.form-textarea {
  resize: vertical;
}

.form-button {
  width: 100%;
  padding: 1rem 2rem;
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  color: white;
  border: none;
  border-radius: 10px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
}

.form-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 15px 40px rgba(59, 130, 246, 0.4);
}

/* Footer */
.footer {
  background: #1e293b;
  color: white;
  padding: 3rem 0;
  text-align: center;
}

.footer p {
  margin: 0.5rem 0;
  color: rgba(255, 255, 255, 0.8);
}

.footer-tagline {
  color: rgba(255, 255, 255, 0.6);
  font-size: 0.9rem;
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
  
  .contato-content {
    grid-template-columns: 1fr;
  }
  
  .section-title {
    font-size: 2rem;
  }
}
</style>
