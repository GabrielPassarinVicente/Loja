<template>
  <div class="contato-page">
    <section class="page-header">
      <div class="container">
        <h1>Entre em Contato</h1>
        <p>Estamos prontos para atender você</p>
      </div>
    </section>

    <section class="contato-section">
      <div class="container">
        <div class="contato-content">
          <div class="contato-info">
            <h2>Fale Conosco</h2>
            <p>Solicite um orçamento sem compromisso ou tire suas dúvidas com nossa equipe especializada.</p>
            
            <div class="contato-items">
              <div class="contato-item">
                <div class="contato-icon">📞</div>
                <div class="contato-text">
                  <h4>Telefone</h4>
                  <a href="tel:4334220000">(43) 3422-0000</a>
                </div>
              </div>

              <div class="contato-item">
                <div class="contato-icon">📱</div>
                <div class="contato-text">
                  <h4>WhatsApp</h4>
                  <a href="https://wa.me/5543999990000" target="_blank">(43) 9 9999-0000</a>
                </div>
              </div>

              <div class="contato-item">
                <div class="contato-icon">📧</div>
                <div class="contato-text">
                  <h4>E-mail</h4>
                  <a href="mailto:contato@windglass.com.br">contato@windglass.com.br</a>
                </div>
              </div>

              <div class="contato-item">
                <div class="contato-icon">📍</div>
                <div class="contato-text">
                  <h4>Endereço</h4>
                  <p>Apucarana - PR<br>Centro</p>
                </div>
              </div>

              <div class="contato-item">
                <div class="contato-icon">🕐</div>
                <div class="contato-text">
                  <h4>Horário de Atendimento</h4>
                  <p>Segunda a Sexta: 8h às 18h<br>Sábado: 8h às 12h</p>
                </div>
              </div>
            </div>

            <div class="social-links">
              <h4>Redes Sociais</h4>
              <div class="social-buttons">
                <a href="#" class="social-btn facebook">
                  <span>f</span> Facebook
                </a>
                <a href="#" class="social-btn instagram">
                  <span>📷</span> Instagram
                </a>
              </div>
            </div>
          </div>

          <div class="contato-form-wrapper">
            <h3>Solicite seu Orçamento</h3>
            <p class="form-subtitle">Preencha o formulário e entraremos em contato em breve</p>
            
            <form @submit.prevent="enviarFormulario" class="contato-form">
              <div class="form-group">
                <label for="nome">Nome Completo *</label>
                <input 
                  type="text" 
                  id="nome"
                  v-model="form.nome" 
                  placeholder="Seu nome completo" 
                  class="form-input"
                  required
                />
              </div>

              <div class="form-row">
                <div class="form-group">
                  <label for="telefone">Telefone/WhatsApp *</label>
                  <input 
                    type="tel" 
                    id="telefone"
                    v-model="form.telefone" 
                    placeholder="(43) 9 9999-0000" 
                    class="form-input"
                    required
                  />
                </div>

                <div class="form-group">
                  <label for="email">E-mail</label>
                  <input 
                    type="email" 
                    id="email"
                    v-model="form.email" 
                    placeholder="seu@email.com" 
                    class="form-input"
                  />
                </div>
              </div>

              <div class="form-group">
                <label for="servico">Serviço de Interesse *</label>
                <select id="servico" v-model="form.servico" class="form-input" required>
                  <option value="">Selecione uma opção</option>
                  <option value="box">Box de Banheiro</option>
                  <option value="vidro-temperado">Vidro Temperado</option>
                  <option value="espelhos">Espelhos</option>
                  <option value="portas">Portas de Vidro</option>
                  <option value="guarda-corpos">Guarda-Corpos</option>
                  <option value="tampos">Tampos de Vidro</option>
                  <option value="outros">Outros</option>
                </select>
              </div>

              <div class="form-group">
                <label for="mensagem">Descreva seu Projeto *</label>
                <textarea 
                  id="mensagem"
                  v-model="form.mensagem" 
                  placeholder="Conte-nos sobre seu projeto, medidas aproximadas, prazo desejado, etc." 
                  class="form-textarea" 
                  rows="5"
                  required
                ></textarea>
              </div>

              <button type="submit" class="form-button" :disabled="enviando">
                {{ enviando ? 'Enviando...' : 'Enviar Mensagem' }}
              </button>

              <p v-if="mensagemSucesso" class="mensagem-sucesso">
                ✓ Mensagem enviada com sucesso! Entraremos em contato em breve.
              </p>
            </form>
          </div>
        </div>
      </div>
    </section>

    <section class="mapa-section">
      <div class="container">
        <h2>Nossa Localização</h2>
        <div class="mapa-placeholder">
          <div class="mapa-content">
            <span class="mapa-icon">📍</span>
            <p>Apucarana - PR</p>
            <p class="mapa-info">Estamos localizados no centro de Apucarana</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'ContatoPage',
  data() {
    return {
      form: {
        nome: '',
        telefone: '',
        email: '',
        servico: '',
        mensagem: ''
      },
      enviando: false,
      mensagemSucesso: false
    }
  },
  methods: {
    async enviarFormulario() {
      this.enviando = true
      
      // Simula envio do formulário
      await new Promise(resolve => setTimeout(resolve, 1500))
      
      console.log('Formulário enviado:', this.form)
      
      this.mensagemSucesso = true
      this.enviando = false
      
      // Limpa o formulário
      this.form = {
        nome: '',
        telefone: '',
        email: '',
        servico: '',
        mensagem: ''
      }
      
      // Remove mensagem de sucesso após 5 segundos
      setTimeout(() => {
        this.mensagemSucesso = false
      }, 5000)
    }
  },
  head() {
    return {
      title: 'Contato - Windglass Apucarana',
      meta: [
        { hid: 'description', name: 'description', content: 'Entre em contato com a Windglass Apucarana. Solicite orçamento para vidros e serviços.' }
      ]
    }
  }
}
</script>

<style scoped>
.contato-page {
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

.contato-section {
  padding: 80px 0;
  background: #f8fafc;
}

.contato-content {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
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
  margin-bottom: 3rem;
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

.contato-text h4 {
  color: #1e293b;
  font-size: 1.125rem;
  margin-bottom: 0.5rem;
  font-weight: 700;
}

.contato-text p,
.contato-text a {
  color: #64748b;
  font-size: 1rem;
  line-height: 1.6;
  text-decoration: none;
}

.contato-text a:hover {
  color: #3b82f6;
}

.social-links {
  margin-top: 3rem;
}

.social-links h4 {
  color: #1e293b;
  font-size: 1.125rem;
  margin-bottom: 1rem;
  font-weight: 700;
}

.social-buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.social-btn {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  border-radius: 10px;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
}

.social-btn.facebook {
  background: #1877f2;
  color: white;
}

.social-btn.instagram {
  background: linear-gradient(135deg, #833ab4 0%, #fd1d1d 50%, #fcb045 100%);
  color: white;
}

.social-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
}

.contato-form-wrapper {
  background: white;
  padding: 3rem;
  border-radius: 20px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
}

.contato-form-wrapper h3 {
  font-size: 1.75rem;
  color: #1e293b;
  margin-bottom: 0.5rem;
  font-weight: 700;
}

.form-subtitle {
  color: #64748b;
  margin-bottom: 2rem;
}

.contato-form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

.form-group {
  display: flex;
  flex-direction: column;
}

.form-group label {
  color: #1e293b;
  font-weight: 600;
  margin-bottom: 0.5rem;
  font-size: 0.95rem;
}

.form-input,
.form-textarea {
  width: 100%;
  padding: 1rem;
  border: 2px solid #e2e8f0;
  border-radius: 10px;
  font-size: 1rem;
  font-family: inherit;
  transition: border-color 0.3s ease;
  background: #f8fafc;
}

.form-input:focus,
.form-textarea:focus {
  outline: none;
  border-color: #3b82f6;
  background: white;
}

.form-textarea {
  resize: vertical;
  min-height: 120px;
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

.form-button:hover:not(:disabled) {
  transform: translateY(-2px);
  box-shadow: 0 15px 40px rgba(59, 130, 246, 0.4);
}

.form-button:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.mensagem-sucesso {
  background: #10b981;
  color: white;
  padding: 1rem;
  border-radius: 10px;
  text-align: center;
  font-weight: 600;
  animation: slideDown 0.3s ease-out;
}

@keyframes slideDown {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.mapa-section {
  padding: 80px 0;
  background: white;
}

.mapa-section h2 {
  font-size: 2.5rem;
  color: #1e293b;
  text-align: center;
  margin-bottom: 3rem;
  font-weight: 700;
}

.mapa-placeholder {
  width: 100%;
  height: 400px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
}

.mapa-content {
  text-align: center;
  color: white;
}

.mapa-icon {
  font-size: 4rem;
  display: block;
  margin-bottom: 1rem;
}

.mapa-content p {
  font-size: 1.5rem;
  font-weight: 600;
  margin: 0.5rem 0;
}

.mapa-info {
  font-size: 1.125rem !important;
  opacity: 0.9;
}

@media (max-width: 968px) {
  .contato-content {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
  
  .form-row {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .page-header h1 {
    font-size: 2rem;
  }
  
  .contato-info h2 {
    font-size: 2rem;
  }
  
  .contato-form-wrapper {
    padding: 2rem 1.5rem;
  }
  
  .mapa-section h2 {
    font-size: 2rem;
  }
  
  .mapa-placeholder {
    height: 300px;
  }
}
</style>
