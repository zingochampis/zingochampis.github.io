<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ri bo bSang mChod — Bergets Rökoffer</title>
    <link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500;1,600;1,700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            background: #3d3225;
            min-height: 100vh;
            padding: 50px 20px;
            font-family: 'EB Garamond', serif;
        }
        
        .pecha-wrapper {
            max-width: 820px;
            margin: 0 auto;
        }
        
        .pecha-leaf {
            background: #f4edd8;
            background-image: 
                linear-gradient(90deg, transparent 0%, rgba(0,0,0,0.02) 50%, transparent 100%),
                linear-gradient(0deg, 
                    #efe6ce 0%, 
                    #f4edd8 3%, 
                    #f7f0dc 50%, 
                    #f4edd8 97%, 
                    #efe6ce 100%);
            border-radius: 3px;
            padding: 45px 70px;
            margin-bottom: 40px;
            position: relative;
            box-shadow: 
                0 1px 3px rgba(0,0,0,0.2),
                0 8px 20px rgba(0,0,0,0.15);
            min-height: 200px;
        }
        
        .pecha-leaf::before,
        .pecha-leaf::after {
            content: '';
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            width: 18px;
            height: 18px;
            background: #3d3225;
            border-radius: 50%;
            box-shadow: inset 0 1px 3px rgba(0,0,0,0.4);
        }
        
        .pecha-leaf::before {
            left: 22px;
        }
        
        .pecha-leaf::after {
            right: 22px;
        }
        
        .title-leaf {
            text-align: center;
            padding: 60px 70px;
        }
        
        .tibetan-title {
            font-size: 1.1em;
            color: #7a6a52;
            letter-spacing: 3px;
            margin-bottom: 12px;
            font-weight: 400;
        }
        
        .swedish-title {
            font-size: 2.4em;
            color: #2a2318;
            font-weight: 500;
            letter-spacing: 1px;
        }
        
        .mantra {
            text-align: center;
            font-size: 1.4em;
            color: #4a1259;
            font-weight: 600;
            margin: 22px 0;
            letter-spacing: 0.5px;
        }
        
        .mantra-cluster {
            text-align: center;
            margin: 35px 0;
            padding: 20px 0;
            border-top: 1px solid #d4c9b0;
            border-bottom: 1px solid #d4c9b0;
        }
        
        .mantra-cluster .mantra {
            margin: 8px 0;
            font-size: 1.3em;
        }
        
        .note {
            font-size: 0.9em;
            color: #8a7a65;
            font-style: italic;
            margin: 20px 0;
            padding: 12px 18px;
            background: rgba(0,0,0,0.025);
            border-left: 2px solid #c4b89a;
        }
        
        .foreign {
            font-weight: 600;
            font-style: italic;
        }
        
        .response {
            font-size: 1.25em;
            color: #4a1259;
            font-weight: 600;
            text-align: right;
            margin-top: 8px;
            margin-bottom: 15px;
            padding-right: 10px;
        }
        
        .final-a {
            text-align: center;
            font-size: 1.8em;
            color: #4a1259;
            font-weight: 600;
            letter-spacing: 8px;
            margin: 35px 0 25px 0;
        }
        
        .closing-mantras {
            text-align: center;
            color: #4a1259;
            font-size: 1.25em;
            font-weight: 600;
            line-height: 2.2;
            padding-top: 25px;
            border-top: 1px solid #d4c9b0;
        }
        
        .colophon {
            text-align: center;
            font-size: 0.85em;
            color: #9a8a72;
            margin-top: 30px;
            font-style: italic;
        }
        
        .leaf-number {
            position: absolute;
            bottom: 15px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 0.8em;
            color: #b0a48c;
        }
        
        /* Flip Card Styles */
        .flip-card {
            perspective: 1000px;
            margin: 18px 0;
            cursor: pointer;
        }
        
        .flip-card-inner {
            position: relative;
            transition: transform 0.6s;
            transform-style: preserve-3d;
        }
        
        .flip-card.flipped .flip-card-inner {
            transform: rotateX(180deg);
        }
        
        .flip-card-front,
        .flip-card-back {
            backface-visibility: hidden;
            -webkit-backface-visibility: hidden;
            border-radius: 4px;
        }
        
        .flip-card-front {
            background: linear-gradient(135deg, #faf6e8 0%, #f0e8d0 100%);
            box-shadow: 
                0 2px 8px rgba(0,0,0,0.08),
                0 1px 2px rgba(0,0,0,0.05),
                inset 0 1px 0 rgba(255,255,255,0.6);
            padding: 18px 22px;
            position: relative;
        }
        
        .flip-card-front::after {
            content: '↻';
            position: absolute;
            top: 8px;
            right: 12px;
            font-size: 0.8em;
            color: #c4b89a;
            opacity: 0.6;
        }
        
        .flip-card-back {
            background: linear-gradient(135deg, #e8e0c8 0%, #d8ceb0 100%);
            box-shadow: 
                0 2px 8px rgba(0,0,0,0.1),
                inset 0 1px 0 rgba(255,255,255,0.3);
            padding: 18px 22px;
            transform: rotateX(180deg);
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
        }
        
        .card-text {
            font-size: 1.15em;
            color: #2a2318;
            line-height: 1.7;
        }
        
        .card-text .seed {
            color: #4a1259;
            font-weight: 600;
            font-size: 1.15em;
        }
        
        .explanation {
            font-size: 1em;
            color: #4a3d2a;
            line-height: 1.7;
            font-style: italic;
        }
        
        .flip-card:hover .flip-card-front {
            box-shadow: 
                0 4px 12px rgba(0,0,0,0.12),
                0 2px 4px rgba(0,0,0,0.08),
                inset 0 1px 0 rgba(255,255,255,0.6);
        }

        .instructions {
            text-align: center;
            font-size: 0.85em;
            color: #9a8a72;
            margin-bottom: 8px;
            font-style: italic;
        }
    </style>
</head>
<body>
    <div class="pecha-wrapper">
        
        <!-- Title leaf -->
        <div class="pecha-leaf title-leaf">
            <div class="tibetan-title">RI BO BSANG MCHOD</div>
            <div class="swedish-title">Bergets Rökoffer</div>
            <div class="instructions">Klicka på texten för förklaring</div>
            <div class="leaf-number">༁</div>
        </div>
        
        <!-- Leaf 1 -->
        <div class="pecha-leaf">
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text" style="text-align: center; font-style: italic;">
                            I det vida lysande kärlet, sammansatt av juvelernas essens
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Kärlet är dharmakaya-grunden: den lysande urbasen. Juveler är de fem elementen — redan närvarande i det som är.
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="note">
                OBS: (Läs ej följande) Den fysiska symbolen för kärlet är <span class="foreign">bSangs</span>-brännaren eller härden. Den fysiska symbolen för det som uppstår är elden och bränslet.
            </div>
            
            <div class="mantra">Om A'a: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            Fenomenvärldens fasetter — var och en åtrående och åtrådd av alla andra — ses i sin egentliga natur
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Allting och alla i ömsesidig uppskattning utan subjekt-objekt. Begär, fri från obsessivitet, är kommunikation — verkligheten som älskar sig själv.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Framträdanden är frambäranden av befriad lusta
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Form erbjuder sig själv. Lusta utan tvång blir uppskattning — medkänslans energi i sin nakna glans.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Manifestation är: självframburen till <span class="foreign">Lama</span>, <span class="foreign">Yidam</span>, <span class="foreign">mKha' 'gro</span> och <span class="foreign">dPa' bo</span>
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            De tre rötterna: Lama (transmission), Yidam (metod), mKha' 'gro/dPa' bo (visdomsvarelser). Självframburen = ingen givare, ingen mottagare, non-action.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Självframburen till <span class="foreign">Ma-gZa'-Dor gSum</span>
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Ma = Mamo Ekajati, gZa' = Za Rahula, Dor = Dorje Legpa. Sum = "de tre". Edsvurna beskyddare.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Självframburen till <span class="foreign">Dorje Legpa</span> och <span class="foreign">Dorje Legma</span>
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Aro gTérs huvudbeskyddare i manlig och kvinnlig form. Vild visdom — skydd genom oförutsägbarhet.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Självframburen till <span class="foreign">damcan mGar ba nagpo</span> och <span class="foreign">damcan gNod sByin 'Bar bar mezer</span>
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Edsvurna: den Svarte Smeden och den Flammande Yaksha. Bundna av Padmasambhava att skydda dharma.
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="leaf-number">ཀ</div>
        </div>
        
        <!-- Leaf 2 -->
        <div class="pecha-leaf">
            <div class="mantra-cluster">
                <div class="mantra">Dza Hung Bam Ho:</div>
                <div class="mantra">Bendzra Sadhu Samaya:</div>
                <div class="mantra">rDo rJe 'Bar ba Hyé-dza Hyé-dza:</div>
                <div class="mantra">Len-gyé jé-jé Len-gyé jé-jé:</div>
                <div class="mantra">Ta-sur jön Ta-sur jön:</div>
                <div class="mantra">Bendzra Angushar: Dza Dza Ho:</div>
            </div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Självframburen till <span class="foreign">Mamoerna</span>, <span class="foreign">Chos-kyong</span> och de Åtta Klasserna
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Mamo = verklighetens vreda feminina kraft. Chos-kyong = dharmaväktare. Åtta klasser = lha, klu, gnod sbyin, etc. — icke-mänskliga varelser.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Självframburen till <span class="foreign">dKyil 'khor</span> av icke-duala varelser
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Ett buddharåd, en samling av de Segervissa — de som ser genom splittringens illusion. Sangha bortom form.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Självframburen till <span class="foreign">Beskyddarna</span> i denna trakt
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Genius loci — platsens andar. Praktik förankras lokalt; vi hedrar territoriet.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Självframburen till varelserna i de sex världarna
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Gudar, titaner, människor, djur, hungriga andar, helvetesvarelser. Röken når alla.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Självframburen till alla varelser — de som jag är skyldig genom min dualistiska irrfärd
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Karmiska fordringsägare. Genom förvillelse har vi skapat skulder till oräkneliga varelser. Vi erkänner och betalar.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Hung: Samaya Dhuma-vali Bhrum:</div>
            
            <div class="leaf-number">ཁ</div>
        </div>
        
        <!-- Leaf 3 -->
        <div class="pecha-leaf">
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Alla skulder är betalda, uppgångna i rök i <span class="foreign">bSangs</span>-lågorna
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Skulderna upplöses — inte genom transaktion utan genom igenkännande av deras tomma natur. Rök = transformation.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Vad än någon och något, var som helst, åtrår: må det falla som strömmande regn — outtömliga samlingar av sensuell näring helgas till detta
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Gränslös generositet. Varje önskan uppfylld. Sensuell näring = alla sinnen mättas. Ingenting undanhålls.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Må negativa handlingar och förvillelser samlade i förflutet, nutid och framtid omvandlas i <span class="foreign">bSangs</span> vars eld fyller hela universum
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Karma och avidya från alla tre tider bränns i visdomselden. Transformation, inte utplåning.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Hung: Samaya Dhuma-vali Bhrum:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Må varje atom av denna eld bli <span class="foreign">Küntuzangpo</span> och <span class="foreign">Küntuzangmo</span>: ett outtömligt moln av fullkomligheter
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Samantabhadra/i — urbuddha-paret: tomhetens och formens enhet. Varje partikel är redan uppvaknad.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Skimrande strålar av femfärgat ljus lyser upp överallt i de sex världarna, ner till djupaste helvete
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Fem färger = fem element befriade. Ljuset når även djupaste helvete. Ingen utesluts.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="flip-card" onclick="this.classList.toggle('flipped')">
                <div class="flip-card-inner">
                    <div class="flip-card-front">
                        <div class="card-text">
                            <span class="seed">A:</span> Må splittrade varelser uppnå <span class="foreign">Ja'lü</span>
                        </div>
                    </div>
                    <div class="flip-card-back">
                        <div class="explanation">
                            Regnbågskroppen: Dzogchens högsta förverkligande. Kroppen löses upp i de fem elementens ljus. Materiell form återvänder till sin källa och blir tillgänglig för allting och alla, överallt.
                        </div>
                    </div>
                </div>
            </div>
            <div class="response">A: Agni-vaha: Hung:</div>
            
            <div class="final-a">A: A: A:</div>
            
            <div class="closing-mantras">
                Om A'a: Hung:<br>
                Ho-nga-dhuma Bhrum:<br>
                Dhuma-rakta Bhrum: Dhuma-yoni Bhrum:<br>
                Samaya Dhuma-vali Bhrum:<br>
                Ram Yam Kham: Om A'a: Hung:<br>
                Adhu-maya Arcad-dhuma Agni-vaha: Hung
            </div>
            
            <div class="colophon">
                Svensk översättning baserad på <span class="foreign">Aro gTér</span>
            </div>
            
            <div class="leaf-number">ག</div>
        </div>
        
    </div>
</body>
</html>
