<script></script>
<template>
  <nav class="navbar is-primary" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <img
        src="../assets/eventos.png"
        class="navbar-item"
        width="112"
        height="28"
      />

      <a
        role="button"
        class="navbar-burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasicExample"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div id="navbarBasicExample" class="navbar-menu">
      <div class="navbar-start">
        <a class="navbar-item"> Início </a>
        <RouterLink class="navbar-item" to="eventos"> Eventos </RouterLink>
        <RouterLink class="navbar-item" to="/contato"> Contato </RouterLink>
        <RouterLink class="navbar-item" to="/sobre-nos"> Sobre-nós </RouterLink>
      </div>

      <div class="navbar-end">
        <div class="navbar-item">
          <div class="buttons">
            <a class="button is-light"> Log in </a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<style></style>
