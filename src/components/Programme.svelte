<script>
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    import '@splidejs/splide/dist/css/themes/splide-default.min.css';
    import imag4 from "$lib/img/img1.jpg";
    import imag5 from "$lib/img/img2.jpg";
    import imag6 from "$lib/img/img6.jpg";
    import imag7 from "$lib/img/img7.jpg";

    let images = [
        {
            src: imag4,
            title: 'image4',
            name: "PODIUM JEUNESSE",
            description: "Plongez dans l'univers de la jeunesse tous les samedis de 10h30 à 11h30.",
        },

        {
            src: imag5,
            title: 'image5',
            name: "PODIUM JEUNESSE",
            description: "Plongez dans l'univers de la jeunesse tous les samedis de 10h30 à 11h30.",
        },

        {
            src: imag6,
            title: 'image6',
            name: "PODIUM JEUNESSE",
            description: "Plongez dans l'univers de la jeunesse tous les samedis de 10h30 à 11h30.",
        },

        {
            src: imag7,
            title: 'image7',
            name: "PODIUM JEUNESSE",
            description: "Plongez dans l'univers de la jeunesse tous les samedis de 10h30 à 11h30.",
        },

        {
            src: imag7,
            title: 'image7',
            name: "PODIUM JEUNESSE",
            description: "Plongez dans l'univers de la jeunesse tous les samedis de 10h30 à 11h30.",
        },

        {
            src: imag7,
            title: 'image7',
            name: "PODIUM JEUNESSE",
            description: "Plongez dans l'univers de la jeunesse tous les samedis de 10h30 à 11h30.",
        },

        {
            src: imag7,
            title: 'image7',
            name: "PODIUM JEUNESSE",
            description: "Plongez dans l'univers de la jeunesse tous les samedis de 10h30 à 11h30.",
        },


    ];
</script>

<div class="slide-big">
<div class="slideHeader">
    <h3>
        NOS EMISSIONS
    </h3>
    <a href="/programmes">Tous nos programmes</a>
</div>
    <hr>
    <Splide  options={ { rewind: true , autoplay:true, paginationDirection: 'ltr', perPage:4, gap:20, wheel: true, releaseWheel: true, lazyLoad:'nearby'} }>

            {#each images as {src,title, name, description}}
                <SplideSlide>
            <div class="ui-card">
                <img {src} alt={title}>
                <div class="description">
                    <h3>{name}</h3>
                    <p>{description}</p>
                    <a href="/podcasts">Nos Podcasts</a>
                </div>
            </div>
                </SplideSlide>
                {/each}

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


    .ui-card{
        width: 350px;
        height: 450px;
        background: radial-gradient(#111 50%, #000 100%);
        overflow: hidden;
        position: relative;
    }

     img{
        max-width: 100%;
         height: 100%;
        object-fit: cover;
        display: block;
    }

    .ui-card img{
        transform: scale(1.3);
        transition: all .3s ease-out;
    }

    .ui-card:hover img{
        transform: scale(1.1) translateY(-20px);
        opacity: .3;
    }

    .description{
        position: absolute;
        left: 0;
        bottom: 0;
        width: 100%;
        padding: 15px;
        text-align: center;
        color: white;
        font-size: 18px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 10px;
    }

    .description h3{
        font-weight: 700;
        transform: translateY(30px);
        opacity: 0;
        transition: all .3s ease-out;
    }

    .description p{
        font-weight: 100;
        transform: translateY(30px);
        opacity: 0;
        transition: all .3s ease-out .2s;
    }

    .description a{
        color: #fff;
        background: #086ec5;
        text-decoration: none;
        display: inline-block;
        padding: 5px 10px;
        border-radius: 5px;
        transform: translateY(30px);
        opacity: 0;
        transition: all .3s ease-out .4s;
    }


.ui-card:hover .description h3{
    transform: translateY(0);
    opacity: 1;
}

    .ui-card:hover .description p{
        transform: translateY(0);
        opacity: 1;
    }

    .ui-card:hover .description a{
        transform: translateY(0);
        opacity: 1;
    }

   .slideHeader{
        display: flex;
       justify-content: space-between;
    }
</style>