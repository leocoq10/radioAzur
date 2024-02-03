<script>
import { Splide, SplideSlide } from '@splidejs/svelte-splide';
import '@splidejs/splide/dist/css/themes/splide-default.min.css';
</script>

<div class="slide-big">
    <Splide  options={ { rewind: true , autoplay:true, paginationDirection: 'ltr', wheel: true, releaseWheel: true, lazyLoad:'nearby'} }>
        <SplideSlide >
          <img src="https://source.unsplash.com/random/800x450/" alt="Image 1"/>
        </SplideSlide>
        <SplideSlide>
          <img src="https://source.unsplash.com/random/800x450/" alt="Image 2"/>
        </SplideSlide>
      </Splide>
</div>


  <style>

   .slide-big{
    width: 100%;
    height: 100%;
       margin-bottom: 100px;
   }

   .slide-big img{
        width: 100%;
        height: 100%;
     object-fit: cover;
    }
  </style>