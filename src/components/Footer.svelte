<script>
    import deco from '../lib/img/imag12.png'
</script>
<div class="deco">
    <img src={deco} alt={deco}>
</div>


<div class="w-full h-full bg-black ">
    <div class="max-w-100% p-10 flex justify-around">

        <div>
            <a href="/"><h2>AZUR FM ANIE</h2></a>
        </div>
        <div class="container1">
            <div class="ecouter">
                <h4 class="text-white font-black">ECOUTER</h4>
                <ul>
                    <li class="mb-3"><a class="text-slate-500 hover:text-blue-300" href="/live">Direct</a></li>
                    <li class="mb-3"><a class="text-slate-500 hover:text-blue-300" href="/podcasts">Replay</a></li>
                    <li><a class="text-slate-500 hover:text-blue-300" href="/podcasts">Podcasts</a></li>
                </ul>
            </div>

            <div class="decouvrir">
                <h4 class="text-white font-black">DECOUVRIR</h4>
                <ul>
                    <li class="mb-3"><a class="text-slate-500 hover:text-blue-300" href="/azur_history">AZUR FM ANIE</a>
                    </li>
                    <li class="mb-3"><a class="text-slate-500 hover:text-blue-300" href="/teams">L'Equipe</a></li>
                    <li><a class="text-slate-500 hover:text-blue-300" href="/programmes">Les Programmes</a></li>
                </ul>


            </div>
        </div>

        <div class="container2">
            <div class="informer">
                <h4 class="text-white font-black">S'INFORMER</h4>
                <ul>
                    <li class="mb-3"><a class=" inline  text-slate-500 hover:text-blue-300" href="/actus">Actualites</a>
                    </li>
                    <li class="mb-3"><a class="text-slate-500 hover:text-blue-300" href="/presse">Presse</a></li>
                    <li><a class="text-slate-500 hover:text-blue-300" href="/live">Evenement</a></li>
                </ul>
            </div>

            <div class="ecouter">
                <h4 class="text-white font-black">NOUS CONTACTER</h4>
                <ul>
                    <li class="mb-3"><h5 class="text-slate-500 hover:text-blue-300 w-15 text-wrap">Route nationale
                        n°1</h5></li>
                    <li class="mb-3"><h5 class="text-slate-500 hover:text-blue-300 ">Tel : 93960920/97827727</h5></li>
                    <li><h5 class="text-slate-500 hover:text-blue-300 ">Anie, Togo</h5></li>
                </ul>
            </div>
        </div>


        <div class="newsletter">
            <div class="input-mail">
                <h6 class="font-bold text-white mb-1">S'inscrire à la newsletter</h6>
                <input class="block w-full p-2 mb-2 rounded-md outline-0" type="email"
                       placeholder="Entrez votre email..."/>
                <button class="bg-blue-700 text-white p-1.5 rounded-md">S'inscrire</button>
            </div>
        </div>

    </div>
</div>

<style>
    h2 {
        font-size: 1.5rem;
        font-weight: 900;
        color: white;
        width: 200px;
    }

    h4 {
        font-size: 1.5rem;
        font-weight: 900;
        color: whitesmoke;
    }

    a, h5 {
        font-size: 1.1rem;
        font-weight: 300;
    }

    .container1, .container2 {
        display: flex;
        flex-direction: column;
        gap: 30px;
    }

    .informer, .decouvrir, .ecouter {
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .newsletter {
        display: flex;
        flex-direction: column;
        gap: 30px;
    }

    .deco {
        width: 100%;
        margin-bottom: -80px;
    }
</style>