<script>
import { RouterLink, RouterView } from 'vue-router'

export default{
  data: function(){
    return{
      link: ''
    }
  }
}

</script>

<template>
  <header>
    <nav class="navbar navbar-expand-lg navbar-dark">
      <div class="container-fluid">
        <a class="navbar-brand" href="#"> Andrés Quesada</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
          <ul class="navbar-nav mb-2 mb-lg-0">
            <li class="nav-item ">
              <RouterLink class="nav-link " aria-current="page" to="/">Inicio</RouterLink>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                Habilidades técnicas
              </a>
              <ul class="dropdown-menu">
                <li><RouterLink class="dropdown-item" aria-current="page" to="/projects">Proyectos</RouterLink></li>
                <li><RouterLink class="dropdown-item" aria-current="page" to="/languages">Lenguajes</RouterLink></li>
              </ul>
            </li>
            <li class="nav-item">
              <RouterLink class="nav-link " aria-current="page" to="/contact">Contacto</RouterLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>

  <Transition name="fade">
    <RouterView></RouterView>
  </Transition>

  <footer class="text-center text-lg-start  text-muted">
    <section class="border-top">
      <div class="container text-center text-md-start mt-5">
        <div class="row mt-3">
          <div class="col-md-3 col-lg-4 col-xl-3 mx-auto mb-4">
            <h6 class="text-uppercase fw-bold mb-4">
              <i class="fas fa-gem me-3 text-secondary"></i>Andrés Quesada
            </h6>
            <p>
              Desarrollador en software
            </p>
          </div>
          <div class="col-md-2 col-lg-2 col-xl-2 mx-auto mb-4">
            <h6 class="text-uppercase fw-bold mb-4">
              Teléfono
            </h6>
            <p>
              <p href="#!" class="text-reset">+506 8834-0586</p>
            </p>
          </div>
          <div class="col-md-3 col-lg-2 col-xl-2 mx-auto mb-4">
            <h6 class="text-uppercase fw-bold mb-4">
              Sitios
            </h6>
            <p>
              <a href="https://github.com/AndresQuesada1234" target="_blank" class="text-reset">GitHub</a>
            </p>
            <p>
              <a href="https://www.linkedin.com/in/andr%C3%A9s-quesada-arias-881971253/" target="_blank" class="text-reset">Linkedin</a>
            </p>
          </div>
          <div class="col-md-4 col-lg-3 col-xl-3 mx-auto mb-md-0 mb-4">
            <h6 class="text-uppercase fw-bold mb-4">Contacto</h6>
            <p><i class="fas fa-home me-3 text-secondary"></i> aquesadaa1@ucenfotec.ac.cr</p>
            <p><i class="fas fa-phone me-3 text-secondary"></i> <a target="_blank" class="text-reset" href="https://wa.link/o8xrk9<">https://wa.link/o8xrk9</a></p>
          </div>
        </div>
      </div>
    </section>
  </footer>
</template>

<style scoped>

</style>
