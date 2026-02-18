<script>
    import FotoLeo from '$lib/assets/FotoLeo.jpg';
    import Tesi from '$lib/assets/TesiCeragioli.pdf';
</script>

<div class="container">
    <div class="img-container">
        <img src={FotoLeo} width="100%"/>
    </div>
    <div class="text">
        <h1>Research Interests:</h1>
        My work focuses on liberalizing and extending traditional proof-theoretic semantics (PTS). During my PhD, I developed novel single-assumption, single-conclusion proof systems in which logical terms can be introduced within the scope of other connectives. This research explored meaning-dependence between logical terms and investigated harmony in such systems. <a href={Tesi} download>(Download my thesis here.)</a>
        <br>
        Following my PhD, I expanded this framework to bilateral, modal, and probabilistic extensions of PTS, broadening its expressive power and applicability.
        <br>
        More recently, I have turned my attention to applying proof systems to model the behavior of machine learning (ML) systems, exploring how logical frameworks can enhance human understanding of AI.
        <br><br>
        <h1>Bio:</h1>
        I earned both my Bachelor’s and Master’s degrees in Philosophy from the University of Pisa. In 2019, I was awarded a six-month research scholarship at the University of Pisa (PRA_2018_6 “Etica, scienza, democrazia”), where I investigated the limits and possibilities of pluralist approaches to logical disagreement. In 2020, I completed my PhD in Philosophy, jointly awarded by the Universities of Pisa and Florence, with a dissertation on Pluralism in Proof-Theoretic Semantics, supervised by Prof. Enrico Moriconi.
        <br>
        Between 2020 and 2024, I worked as an assistant teacher at several high schools in Tuscany and conducted bibliographic research for the University of Pisa. In 2024, I held a postdoctoral position at the University of Rome Tor Vergata (Department of Literary, Philosophical, and Art History Studies) within the PRIN project PUMa: Proof and Understanding in Mathematics. Under the supervision of Prof. Gabriele Pulcini, I researched purity and simplicity in mathematical proofs.
        <br>
        I am currently a postdoctoral researcher at the University of Milan’s Department of Philosophy, working under Prof. Giuseppe Primiero in the PRIN project SMARTEST: Simulation of Probabilistic Systems for the Age of the Digital Twin.

        
    </div>
</div>

<style>
    .container {
        margin: 40px 50px;
        display: flex;
    }


    .text {
        margin: 0 50px;
        font-size:larger;
        width: 100%;
    }

    .img-container { height: 350px;}
    @media screen and (max-width: 540px) {
        .container {
            margin: 20px 20px;
            display: flex;
            flex-direction: column;
        }

        .img-container {
            max-width: 100%;
            max-height: 100%;
        }

        .text {
            margin: 0;
            margin-bottom: 30px;
            font-size:medium;
        }
    }
</style>