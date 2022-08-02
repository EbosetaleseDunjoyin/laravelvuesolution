<template>
  <!-- Header -->
  <div id="header">
    <div class="container-fluid">
      <nav class="navbar navbar-expand-lg  ">
        <div class="container-fluid">
          <div class="row logo">
            <div class="col-4">
              <div class="logo-square">
                <div class="logo-inside"></div>
              </div>
            </div>
            <div class="col-6">
              <a class="navbar-brand" href="#">Adilo</a>
            </div>

          </div>

          <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
            data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
            aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav first mx-auto  mb-2 mb-lg-0">

              <li class="nav-item">
                <a class="nav-link" href="#">Projects</a>
              </li>
              <li class="nav-item dropdown active">
                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                  aria-expanded="false">
                  Tools & App
                </a>
                <ul class="dropdown-menu ">
                  <li><router-link class="dropdown-item activity d-flex justify-content-center" to="/">Snapbyte Recorder</router-link>
                  </li>
                  <li>
                    <hr class="dropdown-divider">
                  </li>
                  <li><a class="dropdown-item d-flex justify-content-center" href="#">AudioBounce</a></li>
                  <li>
                    <hr class="dropdown-divider">
                  </li>
                  <li><a class="dropdown-item d-flex justify-content-center" href="#">Sugar Voice</a></li>
                </ul>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Channels</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Contacts</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Analytcs</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Settings</a>
              </li>
            </ul>
            <ul class="navbar-nav second mb-2 mb-lg-0">
              <li class="nav-item br">
                <a class="nav-link active" aria-current="page" href="#">Help</a>
              </li>

              <li class="nav-item">
                <div class="d-flex align-items-center">
                  <div class="avatar avatar-xl">
                    <img src="./assets/assets/1.jpg" alt="Face 1">
                  </div>
                  <div class="ms-3 name">
                    <h5 class="font-bold">John Duck</h5>
                    <h6 class="text-muted mb-0">@johnducky</h6>
                  </div>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
  </div>
  <!-- Header -->
  <router-view  />
</template>

<script>

</script>
