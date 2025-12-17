<template>
  <div class="servicos-page">
    <section class="page-header">
      <div class="container">
        <h1>Nossos Serviços</h1>
        <p>Do projeto à instalação, cuidamos de tudo</p>
      </div>
    </section>

    <section class="servicos-section">
      <div class="container">
        <div class="servicos-grid">
          <div class="servico-card">
            <div class="servico-number">01</div>
            <h3>Consultoria Personalizada</h3>
            <p>Atendimento especializado para escolher o melhor produto para seu projeto. Nossa equipe analisa suas necessidades e sugere as melhores soluções em vidro.</p>
            <ul class="servico-items">
              <li>Análise do ambiente</li>
              <li>Sugestões técnicas</li>
              <li>Escolha de materiais</li>
              <li>Orçamento detalhado</li>
            </ul>
          </div>

          <div class="servico-card">
            <div class="servico-number">02</div>
            <h3>Medição no Local</h3>
            <p>Profissionais qualificados realizam a medição precisa em sua residência ou empresa. Garantimos precisão milimétrica para um encaixe perfeito.</p>
            <ul class="servico-items">
              <li>Visita técnica gratuita</li>
              <li>Medição precisa</li>
              <li>Avaliação estrutural</li>
              <li>Planejamento da instalação</li>
            </ul>
          </div>

          <div class="servico-card">
            <div class="servico-number">03</div>
            <h3>Fabricação Sob Medida</h3>
            <p>Cada peça é fabricada especialmente para seu projeto com tecnologia de ponta. Processos industriais modernos garantem qualidade superior.</p>
            <ul class="servico-items">
              <li>Equipamentos modernos</li>
              <li>Controle de qualidade</li>
              <li>Tempera certificada</li>
              <li>Acabamento perfeito</li>
            </ul>
          </div>

          <div class="servico-card">
            <div class="servico-number">04</div>
            <h3>Instalação Profissional</h3>
            <p>Equipe técnica experiente garante instalação perfeita e segura. Cuidamos de cada detalhe para entregar um trabalho impecável.</p>
            <ul class="servico-items">
              <li>Equipe treinada</li>
              <li>Ferramentas adequadas</li>
              <li>Limpeza do local</li>
              <li>Garantia de serviço</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section class="diferenciais-section">
      <div class="container">
        <h2>Nossos Diferenciais</h2>
        <div class="diferenciais-grid">
          <div class="diferencial-item">
            <div class="diferencial-icon">🏆</div>
            <h4>Experiência Comprovada</h4>
            <p>Mais de 15 anos no mercado vidreiro de Apucarana</p>
          </div>

          <div class="diferencial-item">
            <div class="diferencial-icon">✓</div>
            <h4>Garantia Total</h4>
            <p>Todos os produtos e serviços com garantia completa</p>
          </div>

          <div class="diferencial-item">
            <div class="diferencial-icon">⚡</div>
            <h4>Agilidade</h4>
            <p>Prazos cumpridos e atendimento rápido</p>
          </div>

          <div class="diferencial-item">
            <div class="diferencial-icon">💎</div>
            <h4>Qualidade Premium</h4>
            <p>Produtos certificados e testados</p>
          </div>

          <div class="diferencial-item">
            <div class="diferencial-icon">👷</div>
            <h4>Equipe Especializada</h4>
            <p>Profissionais treinados e capacitados</p>
          </div>

          <div class="diferencial-item">
            <div class="diferencial-icon">💰</div>
            <h4>Melhor Custo-Benefício</h4>
            <p>Preços justos sem comprometer a qualidade</p>
          </div>
        </div>
      </div>
    </section>

    <section class="processo-section">
      <div class="container">
        <h2>Como Funciona</h2>
        <p class="processo-subtitle">Processo simples e transparente</p>
        
        <div class="processo-timeline">
          <div class="timeline-item">
            <div class="timeline-marker">1</div>
            <div class="timeline-content">
              <h4>Entre em Contato</h4>
              <p>Solicite um orçamento por telefone, WhatsApp ou pelo formulário</p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-marker">2</div>
            <div class="timeline-content">
              <h4>Agendamos a Visita</h4>
              <p>Marcamos uma visita técnica no melhor dia e horário para você</p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-marker">3</div>
            <div class="timeline-content">
              <h4>Medição e Orçamento</h4>
              <p>Realizamos a medição e enviamos o orçamento detalhado</p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-marker">4</div>
            <div class="timeline-content">
              <h4>Fabricação</h4>
              <p>Iniciamos a produção assim que aprovado o orçamento</p>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-marker">5</div>
            <div class="timeline-content">
              <h4>Instalação</h4>
              <p>Instalamos seu produto com qualidade e cuidado</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="cta-servicos">
      <div class="container">
        <h2>Pronto para começar seu projeto?</h2>
        <p>Solicite uma visita técnica gratuita</p>
        <NuxtLink to="/contato" class="btn-cta">Agendar Visita</NuxtLink>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'ServicosPage',
  head() {
    return {
      title: 'Serviços - Windglass Apucarana',
      meta: [
        { hid: 'description', name: 'description', content: 'Consultoria, medição, fabricação e instalação de vidros. Serviço completo e garantido.' }
      ]
    }
  }
}
</script>

<style scoped>
.servicos-page {
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

.servicos-section {
  padding: 80px 0;
  background: #f8fafc;
}

.servicos-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2.5rem;
}

.servico-card {
  background: white;
  padding: 3rem 2.5rem;
  border-radius: 20px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  border: 1px solid #e2e8f0;
}

.servico-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
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
  margin: 0 0 1.5rem 0;
  box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
}

.servico-card h3 {
  font-size: 1.5rem;
  color: #1e293b;
  margin-bottom: 1rem;
  font-weight: 700;
}

.servico-card > p {
  color: #64748b;
  line-height: 1.7;
  margin-bottom: 1.5rem;
}

.servico-items {
  list-style: none;
  padding: 0;
  margin: 0;
}

.servico-items li {
  color: #475569;
  padding: 0.5rem 0;
  padding-left: 1.5rem;
  position: relative;
}

.servico-items li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: #3b82f6;
  font-weight: bold;
}

.diferenciais-section {
  padding: 80px 0;
  background: white;
}

.diferenciais-section h2 {
  font-size: 2.5rem;
  font-weight: 700;
  text-align: center;
  color: #1e293b;
  margin-bottom: 4rem;
}

.diferenciais-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.diferencial-item {
  text-align: center;
  padding: 2rem;
  background: #f8fafc;
  border-radius: 15px;
  transition: all 0.3s ease;
}

.diferencial-item:hover {
  background: white;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  transform: translateY(-5px);
}

.diferencial-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.diferencial-item h4 {
  font-size: 1.25rem;
  color: #1e293b;
  margin-bottom: 0.5rem;
  font-weight: 700;
}

.diferencial-item p {
  color: #64748b;
  font-size: 0.95rem;
}

.processo-section {
  padding: 80px 0;
  background: #f8fafc;
}

.processo-section h2 {
  font-size: 2.5rem;
  font-weight: 700;
  text-align: center;
  color: #1e293b;
  margin-bottom: 1rem;
}

.processo-subtitle {
  text-align: center;
  color: #64748b;
  font-size: 1.125rem;
  margin-bottom: 4rem;
}

.processo-timeline {
  max-width: 800px;
  margin: 0 auto;
}

.timeline-item {
  display: flex;
  gap: 2rem;
  margin-bottom: 3rem;
  align-items: flex-start;
}

.timeline-marker {
  width: 60px;
  height: 60px;
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  font-weight: 700;
  flex-shrink: 0;
  box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
}

.timeline-content {
  flex: 1;
  padding-top: 0.5rem;
}

.timeline-content h4 {
  font-size: 1.5rem;
  color: #1e293b;
  margin-bottom: 0.5rem;
  font-weight: 700;
}

.timeline-content p {
  color: #64748b;
  line-height: 1.6;
}

.cta-servicos {
  padding: 100px 0;
  background: linear-gradient(135deg, #1e40af 0%, #1e3a8a 100%);
  color: white;
  text-align: center;
}

.cta-servicos h2 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.cta-servicos p {
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
  
  .servicos-grid {
    grid-template-columns: 1fr;
  }
  
  .diferenciais-section h2,
  .processo-section h2,
  .cta-servicos h2 {
    font-size: 2rem;
  }
  
  .timeline-item {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
}
</style>
