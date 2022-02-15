<template>
<main>
  <div class="container">
    <navbar />
    <div>
        <div class="row">
          <div class="col-md-4" v-for="item in items" :key="item.id">
            <div class="card mb-3">
              <div class="card-header">
                <img :src="item.foto" width="100%"> 
              </div>
              <div class="card-body">
                <h4>{{ item.nama }}</h4>
                <h4>Rp{{ item.harga }}</h4>
              </div>
            </div>
          </div>
        </div>
    </div>
  </div>
   <div class="container">
            <!-- Footer -->
  <footer class="page-footer font-small special-color-dark pt-4" style="background-color: #228B22;">

  <!-- Footer Elements -->
  <div class="container">
    <!--Grid row-->
    <div class="row justify-content-center">
      <div>

        <form class="form-inline my-2 my-lg-0">
            <input class="form-control mr-sm-2" type="search" placeholder="E-mail" aria-label="your_email">
            <button class="btn btn-outline-warning my-2 my-sm-0" type="submit">Langganan</button>
          </form>

      </div>
      <!--Grid column-->

    </div>
    <!--Grid row-->

  </div>
  <!-- Footer Elements -->

  <!-- Copyright -->
  <div class="footer-copyright text-center py-3">© 2020 Copyright:
    <a href="https://mdbootstrap.com/" style="color: yellow;"> MDBootstrap.com</a>
  </div>
  <!-- Copyright -->

</footer>
<!-- Footer -->
          </div>
</main>
</template>

<script>
export default {
  data() {
    return {
      items: '',
    }
  },
  mounted() {
    this.ambilData()
  },
  methods: {
    async ambilData() {
      const { data, error } = await this.$supabase
        .from('tb_produk')
        .select()
      if(data) this.items = data
      if(error) console.log(error)
    }
  }
}
</script>
