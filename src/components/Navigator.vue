<template>
  <!-- Navbar -->
  <nav class="navbar navbar-dark bg-dark navbar-expand-sm sticky-top">
    <div class="container-fluid">
      <a href="#" class="navbar-brand dance-font"
        >Delicious <span class="text-warning">Restaurant</span></a
      >
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#restaurant-navbar"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="restaurant-navbar">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item px-3">
            <a href="#" class="nav-link">Home</a>
          </li>
          <li class="nav-item px-3">
            <a href="#specials" class="nav-link">Specials</a>
          </li>
          <li class="nav-item px-3">
            <a href="#chefs" class="nav-link">Chefs</a>
          </li>
          <li class="nav-item px-3">
            <a href="#menus" class="nav-link">Menus</a>
          </li>
          <li class="nav-item px-3">
            <a href="#contact" class="nav-link">Contact</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>