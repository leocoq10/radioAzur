<script>
    import { Carousel } from 'flowbite-svelte';
    export const images = [
        {
            alt: 'Cosmic timetraveler',
            src: 'https://images.unsplash.com/photo-1706125356139-bf3c727c6a95?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
            title: 'cosmic'
        },
        {
            alt: 'Cristina Gottardi',
            src: '../img/carousel/img2.jpg',

        },
        {
            alt: 'Johannes Plenio',
            src: '../img/carousel/img3.jpg',
            title: 'johannes'
        },
    ]
</script>



<div class="w-full">
    <Carousel class="w-full h-[720px]" {images} imgClass="w-full"  let:Indicators >
        <Indicators />
    </Carousel>
</div>