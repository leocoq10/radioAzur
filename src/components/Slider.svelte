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

<div class="slidio">
    <Splide options={ {rewind:true, focus : 'center', autoWidth:true, pagination:true,  updateOnMove: true,
 type        : 'loop', perPage     : 1, perMove     : 1,  loop: true, interval: 3000, autoplay:true,} }>

        {#each images as {src, title} }
            <SplideSlide>
                <img {src} alt={title} />
            </SplideSlide>
        {/each}

    </Splide>
</div>


<style>

    .slidio {
        width: 100%;
        height: 888px;
        overflow: hidden;
        margin-bottom: 100px;
    }

    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

</style>