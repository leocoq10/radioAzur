<script>
    import {Splide, SplideSlide} from '@splidejs/svelte-splide';
    import '@splidejs/splide/dist/css/themes/splide-default.min.css';
    import imag1 from '../lib/img/img1.jpg'
    import imag2 from '../lib/img/img2.jpg'
    import imag3 from '../lib/img/img3.jpg'

    let images = [
        {
            src: imag1,
            title: 'image1'
        },

        {
            src: imag2,
            title: 'image2'
        },

        {
            src: imag3,
            title: 'image3'
        },


    ];

</script>

<div class="slide-big">
    <Splide options={ { rewind: true , autoplay:true, autoWidth:true, paginationDirection: 'ltr', wheel: true, releaseWheel: true} }>

        {#each images as {src, title} }
            <SplideSlide>
                <img {src} alt={title} />
            </SplideSlide>
        {/each}

    </Splide>
</div>


<style>

    .slide-big {
        width: 100%;
        margin-bottom: 100px;
    }

</style>