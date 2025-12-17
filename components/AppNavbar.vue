<template>
  <nav class="navbar">
    <div class="container">
      <div class="navbar-content">
        <div class="logo-section">
          <svg class="logo-icon" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect x="3" y="3" width="18" height="18" stroke="currentColor" stroke-width="2" fill="none" opacity="0.3"/>
            <rect x="6" y="6" width="12" height="12" stroke="currentColor" stroke-width="2" fill="none"/>
            <path d="M12 8L12 16M8 12L16 12" stroke="currentColor" stroke-width="2"/>
          </svg>
          <h1 class="logo-text">Windglass</h1>
        </div>
        
        <div class="nav-links">
          <NuxtLink to="/" class="nav-link">Início</NuxtLink>
          <NuxtLink to="/produtos" class="nav-link">Produtos</NuxtLink>
          <NuxtLink to="/servicos" class="nav-link">Serviços</NuxtLink>
          <NuxtLink to="/portfolio" class="nav-link">Portfólio</NuxtLink>
          <NuxtLink to="/contato" class="nav-link-cta">Contato</NuxtLink>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'AppNavbar'
}
</script>

<style scoped>
.navbar {
  background: linear-gradient(135deg, #1a365d 0%, #2c5282 100%);
  padding: 1rem 0;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.navbar-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo-section {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.logo-icon {
  width: 40px;
  height: 40px;
  color: #60a5fa;
}

.logo-text {
  font-size: 1.5rem;
  font-weight: 700;
  color: white;
  margin: 0;
  letter-spacing: -0.5px;
}

.nav-links {
  display: flex;
  gap: 2rem;
  align-items: center;
}

.nav-link {
  color: rgba(255, 255, 255, 0.9);
  text-decoration: none;
  font-weight: 500;
  font-size: 1rem;
  transition: all 0.3s ease;
  position: relative;
}

.nav-link:hover {
  color: #60a5fa;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: #60a5fa;
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

.nav-link-cta {
  color: white;
  text-decoration: none;
  font-weight: 600;
  padding: 0.6rem 1.5rem;
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  border-radius: 8px;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(96, 165, 250, 0.3);
}

.nav-link-cta:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(96, 165, 250, 0.4);
}

@media (max-width: 768px) {
  .nav-links {
    display: none;
  }
  
  .logo-text {
    font-size: 1.2rem;
  }
}
</style>