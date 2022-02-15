<template>
  <main>
    <nav class="navbar navbar-expand-lg navbar-light" style="background-color: #228B22;">
      <a class="navbar-brand" href="#" style="color: yellow;">PersebayaStore</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
                <li class="nav-item active">
                    <NuxtLink to="/" class="col-md-3" style="color: yellow;">
                        Home
                    </NuxtLink>
                </li>
                <li class="nav-item active">
                    <NuxtLink to="/product" class="cd-md-3" style="color: yellow;">
                        Product
                    </NuxtLink>
                </li>
                <li class="nav-item active">
                    <NuxtLink to="/contact" class="col-md-3" style="color: yellow;">
                        Contact
                    </NuxtLink>
                </li>
            </ul>
          </div>
          <form class="form-inline my-2 my-lg-0">
            <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
            <button class="btn btn-outline-warning my-2 my-sm-0" type="submit">Search</button>
          </form>
      </nav>
  </main>
</template>