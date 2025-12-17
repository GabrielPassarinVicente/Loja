<template>
  <div class="produtos-page">
    <section class="page-header">
      <div class="container">
        <h1>Nossos Produtos</h1>
        <p>Qualidade e durabilidade em cada detalhe</p>
      </div>
    </section>

    <section class="produtos-section">
      <div class="container">
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
            <ul class="produto-features">
              <li>✓ Alta resistência</li>
              <li>✓ Segurança garantida</li>
              <li>✓ Vários tamanhos</li>
              <li>✓ Acabamento perfeito</li>
            </ul>
            <NuxtLink to="/contato" class="produto-btn">Solicitar Orçamento</NuxtLink>
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
            <ul class="produto-features">
              <li>✓ Vidro 8mm temperado</li>
              <li>✓ Perfis de alumínio</li>
              <li>✓ Várias cores</li>
              <li>✓ Sob medida</li>
            </ul>
            <NuxtLink to="/contato" class="produto-btn">Solicitar Orçamento</NuxtLink>
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
            <ul class="produto-features">
              <li>✓ Sob medida</li>
              <li>✓ Bordas lapidadas</li>
              <li>✓ Instalação incluída</li>
              <li>✓ Alta qualidade</li>
            </ul>
            <NuxtLink to="/contato" class="produto-btn">Solicitar Orçamento</NuxtLink>
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
            <ul class="produto-features">
              <li>✓ Correr ou pivotante</li>
              <li>✓ Vidro temperado</li>
              <li>✓ Design moderno</li>
              <li>✓ Várias espessuras</li>
            </ul>
            <NuxtLink to="/contato" class="produto-btn">Solicitar Orçamento</NuxtLink>
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
            <ul class="produto-features">
              <li>✓ Segurança total</li>
              <li>✓ Normas ABNT</li>
              <li>✓ Visual elegante</li>
              <li>✓ Fácil manutenção</li>
            </ul>
            <NuxtLink to="/contato" class="produto-btn">Solicitar Orçamento</NuxtLink>
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
            <ul class="produto-features">
              <li>✓ Bordas lapidadas</li>
              <li>✓ Várias espessuras</li>
              <li>✓ Medidas personalizadas</li>
              <li>✓ Acabamento premium</li>
            </ul>
            <NuxtLink to="/contato" class="produto-btn">Solicitar Orçamento</NuxtLink>
          </div>
        </div>
      </div>
    </section>

    <section class="cta-produtos">
      <div class="container">
        <h2>Não encontrou o que procura?</h2>
        <p>Entre em contato conosco para produtos personalizados</p>
        <NuxtLink to="/contato" class="btn-cta">Falar com Especialista</NuxtLink>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'ProdutosPage',
  head() {
    return {
      title: 'Produtos - Windglass Apucarana',
      meta: [
        { hid: 'description', name: 'description', content: 'Vidros temperados, box, espelhos, portas de vidro e muito mais. Qualidade garantida.' }
      ]
    }
  }
}
</script>

<style scoped>
.produtos-page {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.page-header {
  background: linear-gradient(135deg, #1a365d 0%, #2c5282 100%);
  padding: 140px 0 80px 0;
  color: white;
  text-align: center;
}

.page-header h1 {
  font-size: 3rem;
  font-weight: 800;
  margin-bottom: 1rem;
}

.page-header p {
  font-size: 1.25rem;
  color: rgba(255, 255, 255, 0.9);
}

.produtos-section {
  padding: 80px 0;
  background: #f8fafc;
}

.produtos-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2.5rem;
}

.produto-card {
  background: white;
  padding: 2.5rem;
  border-radius: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  border: 1px solid #e2e8f0;
  display: flex;
  flex-direction: column;
}

.produto-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
}

.produto-icon {
  width: 70px;
  height: 70px;
  color: #3b82f6;
  margin-bottom: 1.5rem;
}

.produto-icon svg {
  width: 100%;
  height: 100%;
}

.produto-card h3 {
  font-size: 1.75rem;
  color: #1e293b;
  margin-bottom: 1rem;
  font-weight: 700;
}

.produto-card > p {
  color: #64748b;
  line-height: 1.7;
  font-size: 1rem;
  margin-bottom: 1.5rem;
}

.produto-features {
  list-style: none;
  padding: 0;
  margin: 0 0 2rem 0;
  flex-grow: 1;
}

.produto-features li {
  color: #475569;
  padding: 0.5rem 0;
  font-size: 0.95rem;
}

.produto-btn {
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  color: white;
  text-decoration: none;
  padding: 1rem 2rem;
  border-radius: 10px;
  font-weight: 600;
  text-align: center;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(59, 130, 246, 0.3);
}

.produto-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(59, 130, 246, 0.4);
}

.cta-produtos {
  padding: 100px 0;
  background: linear-gradient(135deg, #1e40af 0%, #1e3a8a 100%);
  color: white;
  text-align: center;
}

.cta-produtos h2 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.cta-produtos p {
  font-size: 1.25rem;
  margin-bottom: 2.5rem;
  color: rgba(255, 255, 255, 0.9);
}

.btn-cta {
  background: white;
  color: #1e40af;
  padding: 1rem 2.5rem;
  text-decoration: none;
  border-radius: 10px;
  font-weight: 600;
  font-size: 1rem;
  display: inline-block;
  transition: all 0.3s ease;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.btn-cta:hover {
  transform: translateY(-3px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
}

@media (max-width: 768px) {
  .page-header h1 {
    font-size: 2rem;
  }
  
  .produtos-grid {
    grid-template-columns: 1fr;
  }
  
  .cta-produtos h2 {
    font-size: 2rem;
  }
}
</style>
