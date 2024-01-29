<script>

	import { fly, slide} from "svelte/transition";

</script>


<div class="menu-bloc" 

in:fly={{x:-100}}
out:slide={{x:100}}

>
  <p>ECOUTER</p>
  <a href="/live">Direct</a>
  <a href="/podcasts">Podcasts</a>

  <p>QUI SOMMES-NOUS ?</p>
  <a href="/">Notre histoire</a>
  <a href="/">Nos Programmes</a>
  <a href="/">Notre Equipe</a>
  <a href="/">Nos Videos</a>

  <p>S'INFORMER</p>
  <a href="/live">Actualites</a>
  <a href="/podcasts">Nous Contacter</a>
</div>



<style>
.menu-bloc{
  background: white;
  color: #086ec5;
  padding: 80px;
  float: left;
  z-index: 4;
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 10px;
  width: 27rem;
  box-shadow: 6px 6px 18px 0px rgba(0, 0, 0, 0.3);
  text-align: center;

animation: animation1 1s ease-in-out;
}

.menu-bloc a {
  display: block;
  color: rgba(0, 0, 0, 0.466);
  font-size: 22px;
  font-weight: 300;
  position: relative;
  
}

.menu-bloc a:hover{
  color: #086ec5;
}

.menu-bloc p {
  display: block;
  color: rgb(0, 0, 0);
  font-size: 25px;
  font-weight: 900;
  margin-top: 15px;
}



</style>
