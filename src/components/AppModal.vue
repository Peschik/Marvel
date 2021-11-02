<template>
    <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">{{character.name}}</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">

          
          <img :src="character.thumbnail"
            alt="character.name" style=max-width:100%>
        </div>
        <p class="text-muted container">{{character.modified}}</p>
        <div class="container">
            <h5>Описание:</h5>
            <p>{{character.description}}</p>
        </div>
        <h5 class="container">Комиксы:</h5>
        <div class="container">
            <ul>
                <li v-for="elComics in character.comics">{{elComics.name}}</li>
            </ul>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Закрыть</button>
        </div>
      </div>
    </div>
  </div>
        </div>
</template>

<script>
    export default {
        name: "AppModal",
        props: ["character"], 
    }
</script>

<style scoped>

</style>
