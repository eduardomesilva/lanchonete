<template>
  <nav>
    <div class="container">
        <span class="navbar"> <h1>Monte seu lanche</h1></span>
    </div>
  </nav>
  <div class="container">
    <div class="row">
      <div class="col-md-6">
            Imagens do lanche
      </div>

      <div class="col-md-6">
          <div class="row">
            <div class="col">
              <div class="card">
                <div class="card-header"> Tipo do Pao</div>
                <div class="card-body">
                  <div class="form-check form-check-inline">
                    <input class="form-check-input" type="radio">
                    <label class="form-check-label"> Gergilim</label>
                  </div>
                  <div class="form-check form-check-inline">
                    <input class="form-check-input" type="radio">
                    <label class="form-check-label"> Australiano</label>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="row mt-2">
            <div class="col">
              <div class="card">
                <div class="card-header"> Salada</div>
                <div class="card-body">
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox">
                    <label class="form-check-label"> Alface </label>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="row mt-2">
            <div class="col">
              <div class="card">
                <div class="card-header"> Molhos</div>
                <div class="card-body">
                  <div class="form-check form-check-inline">
                    <input class="form-check-input" type="checkbox">
                    <label class="form-check-label"> Ketchup </label>
                  </div>
                  <div class="form-check form-check-inline">
                    <input class="form-check-input" type="checkbox">
                    <label class="form-check-label"> Mostarda </label>
                  </div>
                  <div class="form-check form-check-inline">
                    <input class="form-check-input" type="checkbox">
                    <label class="form-check-label"> Maionese </label>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="row mt-2">
            <div class="col">
              <div class="card">
                <div class="card-header"> Hamburger</div>
                <div class="card-body"></div>
              </div>
            </div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'Montar'
}
</script>

<style>

</style>