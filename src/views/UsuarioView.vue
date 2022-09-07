<template>
    <div class="usuario">
        <p v-if="nome.length > 5 ">{{ nome }}</p>
        <p><input type="text" v-model="nome"><button @click="inserirUsuario()">Aplicar</button></p>
        <ul>
            <li v-for="(usuario, i) in usuarios" :key="i">{{usuario}}</li>
        </ul>
    </div>
</template>

<script>
export default {
     name: 'usuarioView',
  data() {
    return{
        nome: 'Zaion Felippe',
        usuarios: ['oi', 'tudo bem', 'como','se ta?','Eu e meus faxas']
    }
  },
  methods: {
    inserirUsuario(){
        this.usuarios.push(this.nome);
        this.nome = '';
    }
  }  
}
</script>
