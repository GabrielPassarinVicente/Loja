<template>
  <div class="portfolio-page">
    <section class="page-header">
      <div class="container">
        <h1>Nosso Portfólio</h1>
        <p>Conheça alguns dos nossos trabalhos realizados</p>
      </div>
    </section>

    <section class="portfolio-section">
      <div class="container">
        <div class="portfolio-filters">
          <button 
            :class="['filter-btn', { active: filtroAtivo === 'todos' }]"
            @click="filtroAtivo = 'todos'"
          >
            Todos
          </button>
          <button 
            :class="['filter-btn', { active: filtroAtivo === 'box' }]"
            @click="filtroAtivo = 'box'"
          >
            Box de Banheiro
          </button>
          <button 
            :class="['filter-btn', { active: filtroAtivo === 'portas' }]"
            @click="filtroAtivo = 'portas'"
          >
            Portas
          </button>
          <button 
            :class="['filter-btn', { active: filtroAtivo === 'guarda-corpos' }]"
            @click="filtroAtivo = 'guarda-corpos'"
          >
            Guarda-Corpos
          </button>
          <button 
            :class="['filter-btn', { active: filtroAtivo === 'espelhos' }]"
            @click="filtroAtivo = 'espelhos'"
          >
            Espelhos
          </button>
        </div>

        <div class="portfolio-grid">
          <div 
            v-for="item in trabalhosFiltrados" 
            :key="item.id"
            class="portfolio-item"
            @click="abrirModal(item)"
          >
            <div class="portfolio-image">
              <div class="image-placeholder" :style="{ background: item.cor }">
                <span class="image-icon">📷</span>
              </div>
              <div class="portfolio-overlay">
                <h3>{{ item.titulo }}</h3>
                <p>{{ item.categoria }}</p>
                <span class="ver-mais">Ver Detalhes →</span>
              </div>
            </div>
          </div>
        </div>

        <div v-if="trabalhosFiltrados.length === 0" class="empty-state">
          <p>Nenhum trabalho encontrado nesta categoria</p>
        </div>
      </div>
    </section>

    <!-- Modal -->
    <div v-if="modalAberto" class="modal" @click.self="fecharModal">
      <div class="modal-content">
        <button class="modal-close" @click="fecharModal">×</button>
        <div class="modal-image" :style="{ background: trabalhoSelecionado.cor }">
          <span class="image-icon large">📷</span>
        </div>
        <div class="modal-info">
          <h2>{{ trabalhoSelecionado.titulo }}</h2>
          <span class="modal-categoria">{{ trabalhoSelecionado.categoria }}</span>
          <p>{{ trabalhoSelecionado.descricao }}</p>
          <div class="modal-detalhes">
            <div class="detalhe-item">
              <strong>Local:</strong> {{ trabalhoSelecionado.local }}
            </div>
            <div class="detalhe-item">
              <strong>Ano:</strong> {{ trabalhoSelecionado.ano }}
            </div>
          </div>
        </div>
      </div>
    </div>

    <section class="cta-portfolio">
      <div class="container">
        <h2>Gostou do nosso trabalho?</h2>
        <p>Seu projeto pode ser o próximo do nosso portfólio!</p>
        <NuxtLink to="/contato" class="btn-cta">Solicitar Orçamento</NuxtLink>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'PortfolioPage',
  data() {
    return {
      filtroAtivo: 'todos',
      modalAberto: false,
      trabalhoSelecionado: null,
      trabalhos: [
        {
          id: 1,
          titulo: 'Box de Banheiro Elegante',
          categoria: 'Box de Banheiro',
          tipo: 'box',
          descricao: 'Box de banheiro em vidro temperado 8mm com perfil de alumínio cromado. Projeto moderno e funcional para banheiro de apartamento.',
          local: 'Apucarana - PR',
          ano: '2024',
          cor: 'linear-gradient(135deg, #667eea 0%, #764ba2 100%)'
        },
        {
          id: 2,
          titulo: 'Box Frontal Minimalista',
          categoria: 'Box de Banheiro',
          tipo: 'box',
          descricao: 'Box frontal com abertura de correr, vidro temperado incolor e acabamento em alumínio preto fosco.',
          local: 'Apucarana - PR',
          ano: '2024',
          cor: 'linear-gradient(135deg, #f093fb 0%, #f5576c 100%)'
        },
        {
          id: 3,
          titulo: 'Porta de Vidro Pivotante',
          categoria: 'Portas de Vidro',
          tipo: 'portas',
          descricao: 'Porta pivotante em vidro temperado 10mm com ferragens em inox escovado. Solução elegante para entrada principal.',
          local: 'Apucarana - PR',
          ano: '2024',
          cor: 'linear-gradient(135deg, #4facfe 0%, #00f2fe 100%)'
        },
        {
          id: 4,
          titulo: 'Porta de Correr para Sala',
          categoria: 'Portas de Vidro',
          tipo: 'portas',
          descricao: 'Porta de correr em vidro temperado para integração entre sala e varanda. Sistema de trilho embutido.',
          local: 'Apucarana - PR',
          ano: '2023',
          cor: 'linear-gradient(135deg, #43e97b 0%, #38f9d7 100%)'
        },
        {
          id: 5,
          titulo: 'Guarda-Corpo para Sacada',
          categoria: 'Guarda-Corpos',
          tipo: 'guarda-corpos',
          descricao: 'Guarda-corpo em vidro temperado 10mm para sacada de apartamento. Fixação por botões de inox, seguindo normas ABNT.',
          local: 'Apucarana - PR',
          ano: '2024',
          cor: 'linear-gradient(135deg, #fa709a 0%, #fee140 100%)'
        },
        {
          id: 6,
          titulo: 'Guarda-Corpo para Escada',
          categoria: 'Guarda-Corpos',
          tipo: 'guarda-corpos',
          descricao: 'Guarda-corpo de escada interna com vidro laminado e corrimão de inox. Design moderno e seguro.',
          local: 'Apucarana - PR',
          ano: '2024',
          cor: 'linear-gradient(135deg, #30cfd0 0%, #330867 100%)'
        },
        {
          id: 7,
          titulo: 'Espelho de Parede Grande',
          categoria: 'Espelhos',
          tipo: 'espelhos',
          descricao: 'Espelho sob medida para sala de estar, bordas lapidadas e bisotê. Instalação com cola especial.',
          local: 'Apucarana - PR',
          ano: '2023',
          cor: 'linear-gradient(135deg, #a8edea 0%, #fed6e3 100%)'
        },
        {
          id: 8,
          titulo: 'Espelho para Banheiro',
          categoria: 'Espelhos',
          tipo: 'espelhos',
          descricao: 'Conjunto de espelhos para banheiro com iluminação embutida e acabamento bisotê.',
          local: 'Apucarana - PR',
          ano: '2024',
          cor: 'linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%)'
        },
        {
          id: 9,
          titulo: 'Box de Canto Personalizado',
          categoria: 'Box de Banheiro',
          tipo: 'box',
          descricao: 'Box de canto com vidro temperado fumê, ideal para banheiros menores. Otimização de espaço.',
          local: 'Apucarana - PR',
          ano: '2023',
          cor: 'linear-gradient(135deg, #ff9a9e 0%, #fecfef 100%)'
        },
        {
          id: 10,
          titulo: 'Porta de Vidro Dupla',
          categoria: 'Portas de Vidro',
          tipo: 'portas',
          descricao: 'Conjunto de portas duplas em vidro temperado para ambiente comercial. Acabamento premium.',
          local: 'Apucarana - PR',
          ano: '2023',
          cor: 'linear-gradient(135deg, #a1c4fd 0%, #c2e9fb 100%)'
        },
        {
          id: 11,
          titulo: 'Guarda-Corpo Piscina',
          categoria: 'Guarda-Corpos',
          tipo: 'guarda-corpos',
          descricao: 'Guarda-corpo para área de piscina com vidro temperado verde e fixação invisível.',
          local: 'Apucarana - PR',
          ano: '2024',
          cor: 'linear-gradient(135deg, #d299c2 0%, #fef9d7 100%)'
        },
        {
          id: 12,
          titulo: 'Espelho de Academia',
          categoria: 'Espelhos',
          tipo: 'espelhos',
          descricao: 'Espelhos grandes para academia, instalados em parede completa. Alta durabilidade.',
          local: 'Apucarana - PR',
          ano: '2023',
          cor: 'linear-gradient(135deg, #fdcbf1 0%, #e6dee9 100%)'
        }
      ]
    }
  },
  computed: {
    trabalhosFiltrados() {
      if (this.filtroAtivo === 'todos') {
        return this.trabalhos
      }
      return this.trabalhos.filter(t => t.tipo === this.filtroAtivo)
    }
  },
  methods: {
    abrirModal(trabalho) {
      this.trabalhoSelecionado = trabalho
      this.modalAberto = true
      document.body.style.overflow = 'hidden'
    },
    fecharModal() {
      this.modalAberto = false
      this.trabalhoSelecionado = null
      document.body.style.overflow = 'auto'
    }
  },
  head() {
    return {
      title: 'Portfólio - Windglass Apucarana',
      meta: [
        { hid: 'description', name: 'description', content: 'Veja nossos trabalhos realizados em vidros, box, espelhos e guarda-corpos em Apucarana.' }
      ]
    }
  },
  beforeDestroy() {
    document.body.style.overflow = 'auto'
  }
}
</script>

<style scoped>
.portfolio-page {
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

.portfolio-section {
  padding: 80px 0;
  background: #f8fafc;
  min-height: 60vh;
}

.portfolio-filters {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
  margin-bottom: 4rem;
}

.filter-btn {
  padding: 0.75rem 1.5rem;
  background: white;
  border: 2px solid #e2e8f0;
  border-radius: 10px;
  color: #64748b;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  font-size: 1rem;
}

.filter-btn:hover {
  border-color: #3b82f6;
  color: #3b82f6;
}

.filter-btn.active {
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  border-color: #3b82f6;
  color: white;
  box-shadow: 0 4px 15px rgba(59, 130, 246, 0.3);
}

.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
  gap: 2rem;
}

.portfolio-item {
  cursor: pointer;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  background: white;
}

.portfolio-item:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

.portfolio-image {
  position: relative;
  overflow: hidden;
}

.image-placeholder {
  width: 100%;
  height: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: transform 0.3s ease;
}

.portfolio-item:hover .image-placeholder {
  transform: scale(1.1);
}

.image-icon {
  font-size: 4rem;
  opacity: 0.5;
}

.image-icon.large {
  font-size: 6rem;
}

.portfolio-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.9), transparent);
  color: white;
  padding: 2rem;
  transform: translateY(100%);
  transition: transform 0.3s ease;
}

.portfolio-item:hover .portfolio-overlay {
  transform: translateY(0);
}

.portfolio-overlay h3 {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  font-weight: 700;
}

.portfolio-overlay p {
  font-size: 1rem;
  margin-bottom: 1rem;
  color: rgba(255, 255, 255, 0.9);
}

.ver-mais {
  display: inline-block;
  color: #60a5fa;
  font-weight: 600;
}

.empty-state {
  text-align: center;
  padding: 4rem 0;
  color: #64748b;
  font-size: 1.125rem;
}

/* Modal */
.modal {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 2000;
  padding: 2rem;
  backdrop-filter: blur(5px);
}

.modal-content {
  background: white;
  border-radius: 20px;
  max-width: 900px;
  width: 100%;
  max-height: 90vh;
  overflow-y: auto;
  position: relative;
  animation: modalAppear 0.3s ease-out;
}

@keyframes modalAppear {
  from {
    opacity: 0;
    transform: scale(0.9);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

.modal-close {
  position: absolute;
  top: 1rem;
  right: 1rem;
  width: 40px;
  height: 40px;
  background: white;
  border: none;
  border-radius: 50%;
  font-size: 2rem;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
  z-index: 10;
  transition: all 0.3s ease;
}

.modal-close:hover {
  background: #f1f5f9;
  transform: rotate(90deg);
}

.modal-image {
  width: 100%;
  height: 400px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 20px 20px 0 0;
}

.modal-info {
  padding: 3rem;
}

.modal-info h2 {
  font-size: 2rem;
  color: #1e293b;
  margin-bottom: 0.5rem;
  font-weight: 700;
}

.modal-categoria {
  display: inline-block;
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 8px;
  font-size: 0.9rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
}

.modal-info p {
  color: #64748b;
  line-height: 1.8;
  font-size: 1.125rem;
  margin-bottom: 2rem;
}

.modal-detalhes {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  padding: 2rem;
  background: #f8fafc;
  border-radius: 15px;
}

.detalhe-item {
  color: #475569;
}

.detalhe-item strong {
  color: #1e293b;
  display: block;
  margin-bottom: 0.25rem;
  font-size: 0.9rem;
}

.cta-portfolio {
  padding: 100px 0;
  background: linear-gradient(135deg, #1e40af 0%, #1e3a8a 100%);
  color: white;
  text-align: center;
}

.cta-portfolio h2 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.cta-portfolio p {
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
  
  .portfolio-grid {
    grid-template-columns: 1fr;
  }
  
  .modal-content {
    margin: 1rem;
  }
  
  .modal-image {
    height: 250px;
  }
  
  .modal-info {
    padding: 2rem 1.5rem;
  }
  
  .modal-detalhes {
    grid-template-columns: 1fr;
  }
  
  .cta-portfolio h2 {
    font-size: 2rem;
  }
}
</style>
