<template>
    <nav class="navbar navbar-light bg-light">
        <div class="container">
            <span class="navbar-brand mb-0 h1">Monte o seu lanche</span>
        </div>
    </nav>
    <div class="container">
        <div class="row">
            <div class="col-md-6">
                <div class="row mt-2">
                    <div class="col">
                        <img :src="pao[0]">
                        <img :src="alface">
                        <img :src="ketchup">
                        <img :src="maionese">
                        <img :src="mostarda">
                        <img :src="hamburguer">
                        <img :src="pao[1]">
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <div class="row mt-2">
                    <div class="col">
                        <div class="card">
                            <div class="card-header">TIPO DO PÃO</div>
                            <div class="card-body">
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="radio" value="gergilim" v-model="inputTipoPao">
                                    <label class="form-check-label">Gergilim</label>
                                </div>
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="radio" value="australiano" v-model="inputTipoPao">
                                    <label class="form-check-label">Australiano</label>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="row mt-2">
                    <div class="col">
                        <div class="card">
                            <div class="card-header">SALADAS</div>
                            <div class="card-body">
                                <div class="form-check">
                                    <input class="form-check-input" type="checkbox" value="alface" v-model="inputSalada">
                                    <label class="form-check-label">Alface</label>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="row mt-2">
                    <div class="col">
                        <div class="card">
                            <div class="card-header">MOLHOS</div>
                            <div class="card-body">
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="checkbox" value="ketchup" v-model="inputMolhos">
                                    <label class="form-check-label">Ketchup</label>
                                </div>
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="checkbox" value="mostarda" v-model="inputMolhos">
                                    <label class="form-check-label">Mostarda</label>
                                </div>
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="checkbox" value="maionese" v-model="inputMolhos">
                                    <label class="form-check-label">Maionese</label>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="row mt-2">
                    <div class="col">
                        <div class="card">
                            <div class="card-header">TIPO DE HAMBURGER</div>
                            <div class="card-body">
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="radio" value="bovino" v-model="inputHamburguer">
                                    <label class="form-check-label">Bovino</label>
                                </div>
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="radio" value="frango" v-model="inputHamburguer">
                                    <label class="form-check-label">Frango</label>
                                </div>
                                 <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="radio" value="soja" v-model="inputHamburguer">
                                    <label class="form-check-label">Soja</label>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Montar',
    data(){
        return{
          inputTipoPao: '',
          inputSalada: [],
          inputMolhos: [],
          inputHamburguer: ''
        }
    },
    computed:{
        pao(){
          switch(this.inputTipoPao){
            case 'gergilim':
              return [require('../assets/pao_gergelim_superior.png'), require('../assets/pao_gergelim_inferior.png') ]
            case 'australiano':
               return [require('../assets/pao_australiano_superior.png'), require('../assets/pao_australiano_inferior.png') ]
            default:
              let ar = [require('../assets/pao_superior.png'), require('../assets/pao_inferior.png')]
              return ar
          }
        },
        alface(){
          if(this.inputSalada.includes('alface')){
            return require('../assets/alface1.png')
          }
          return require('../assets/alface.png')
        },
         ketchup(){
           if(this.inputMolhos.includes('ketchup')){
              return require('../assets/ketchup.png')
             }
            return require('../assets/molho.png')
        },
         maionese(){
          if(this.inputMolhos.includes('maionese')){
              return require('../assets/maionese.png')
             }
          return require('../assets/molho.png')
        },
         mostarda(){
          if(this.inputMolhos.includes('mostarda')){
              return require('../assets/mostarda.png')
             }
          return require('../assets/molho.png')
        },
        hamburguer(){
          switch(this.inputHamburguer){
            case 'bovino':
              return require('../assets/bovino.png')
            case 'frango':
              return require('../assets/frango.png')
            case 'soja':
              return require('../assets/soja.png')
          }
          return require('../assets/hamburguer.png')
        }
    }
}
</script>

<style>

</style>