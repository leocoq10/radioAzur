<script>
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    import '@splidejs/splide/dist/css/themes/splide-default.min.css';
</script>

<div class="slide-big">
<div class="slideHeader">
    <h3>
        NOS EMISSIONS
    </h3>
    <a href="/programmes">Tous nos programmes</a>

</div>
    <hr>
    <Splide  options={ { rewind: true , autoplay:true, paginationDirection: 'ltr', perPage:4, gap:15, wheel: true, releaseWheel: true, lazyLoad:'nearby'} }>
        <SplideSlide >
            <img src="https://source.unsplash.com/random/" alt="Image 1"/>
            <h5>Podium Jeunesse</h5>
            <small>Tous les Samedis</small>
            <small>11h30 - 12h30</small>
        </SplideSlide>
        <SplideSlide>
            <img src="https://source.unsplash.com/random/" alt="Image 2"/>
            <h5>Podium Jeunesse</h5>
        </SplideSlide>
        <SplideSlide>
            <img src="https://source.unsplash.com/random/" alt="Image 3"/>
            <h5>Podium Jeunesse</h5>
        </SplideSlide>
        <SplideSlide>
            <img src="https://source.unsplash.com/random" alt="Image 4"/>
            <h5>Podium Jeunesse</h5>
        </SplideSlide>
        <SplideSlide>
            <img src="https://source.unsplash.com/random" alt="Image 5"/>
            <h5>Podium Jeunesse</h5>
        </SplideSlide>
        <SplideSlide>
            <img src="https://source.unsplash.com/random" alt="Image 6"/>
            <h5>Podium Jeunesse</h5>
        </SplideSlide>
    </Splide>
</div>


<style>

    .slide-big{
        width: 75%;
        height: 550px;
        display: flex;
        flex-direction: column;
        gap: 10px;
        margin: 0 auto;
        margin-bottom: 100px;
    }

    .slide-big img{
        width: 100%;
        height: 80%;
        object-fit: cover;
    }

    .slide-big h3{
        font-size: 1.5rem;
        font-weight: 900;
        display: inline-block;
    }

    .slide-big a{
        font-size: 1rem;
        border: 1px solid #396c94;
        padding: 5px;
        border-radius: 5px;
        color: #396c94;
    }

   .slideHeader{
        display: flex;
       justify-content: space-between;
    }
</style>