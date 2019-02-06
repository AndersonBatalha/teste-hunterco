<template>
  <div
    class="container"
    style="margin-top: 70px;"
  >
    <!-- seu código aqui -->
    <div v-for="(job, i) in jobs" :key="i" id='vagas'>
      
      <div class='card'>
        <img :src='job.url_banner' class='card-img-top' alt='logo-empresa'/>
        <div class='card-body'>
          <h5 class='card-title'>{{ job.nome_empresa }} - {{ job.vaga }}</h5>
          <a href='#' class='btn btn-lg btn-block'>CONHECER</a>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
import Jobs from '@/components/Jobs.js'
export default {
  data() {
    return {
      jobs: Jobs.getJobs()
    }
  },
}
</script>

<style>
</style>
