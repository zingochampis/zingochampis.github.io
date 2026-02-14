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
            max-width: 780px;
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
        
        .verse-opening {
            font-size: 1.2em;
            color: #2a2318;
            line-height: 1.9;
            text-align: center;
            margin-bottom: 25px;
            font-style: italic;
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
        
        .offering {
            margin: 20px 0;
            line-height: 1.8;
        }
        
        .offering-text {
            font-size: 1.15em;
            color: #2a2318;
            display: block;
            padding-left: 28px;
            text-indent: -28px;
        }
        
        .offering-text .seed {
            color: #4a1259;
            font-weight: 600;
            font-size: 1.2em;
        }
        
        .response {
            font-size: 1.25em;
            color: #4a1259;
            font-weight: 600;
            text-align: right;
            margin-top: 4px;
            padding-right: 10px;
        }
        
        .foreign {
            font-weight: 600;
            font-style: italic;
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
    </style>
</head>
<body>
    <div class="pecha-wrapper">
        
        <!-- Title leaf -->
        <div class="pecha-leaf title-leaf">
            <div class="tibetan-title">RI BO BSANG MCHOD</div>
            <div class="swedish-title">Bergets Rökoffer</div>
            <div class="leaf-number">༁</div>
        </div>
        
        <!-- Leaf 1 -->
        <div class="pecha-leaf">
            <div class="verse-opening">
                I det vida lysande kärlet, sammansatt av juvelernas essens
            </div>
            
            <div class="note">
                OBS: (Läs ej följande) Den fysiska symbolen för kärlet är <span class="foreign">bSangs</span>-brännaren eller härden. Den fysiska symbolen för det som uppstår är elden och bränslet.
            </div>
            
            <div class="mantra">Om A'a: Hung:</div>
            
            <div class="offering">
                <span class="offering-text">Fenomenvärldens fasetter — var och en åtrående och åtrådd av alla andra — ses i sin egentliga natur</span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Framträdanden är frambäranden av befriad lusta</span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Manifestation är: självframburen till <span class="foreign">Lama</span>, <span class="foreign">Yidam</span>, <span class="foreign">mKha' 'gro</span> och <span class="foreign">dPa' bo</span></span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Självframburen till <span class="foreign">Ma-gZa'-Dor gSum</span></span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Självframburen till <span class="foreign">Dorje Legpa</span> och <span class="foreign">Dorje Legma</span></span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Självframburen till <span class="foreign">damcan mGar ba nagpo</span> och <span class="foreign">damcan gNod sByin 'Bar bar mezer</span></span>
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
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Självframburen till <span class="foreign">Mamoerna</span>, <span class="foreign">Chos-kyong</span> och de Åtta Klasserna</span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Självframburen till <span class="foreign">dKyil 'khor</span> av icke-duala varelser</span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Självframburen till <span class="foreign">Beskyddarna</span> i denna trakt</span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Självframburen till varelserna i de sex världarna</span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Självframburen till alla varelser — de som jag är skyldig genom min dualistiska irrfärd</span>
                <div class="response">A: Hung: Samaya Dhuma-vali Bhrum:</div>
            </div>
            
            <div class="leaf-number">ཁ</div>
        </div>
        
        <!-- Leaf 3 -->
        <div class="pecha-leaf">
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Alla skulder är betalda, uppgångna i rök i <span class="foreign">bSangs</span>-lågorna</span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Vad än någon och något, var som helst, åtrår: må det falla som strömmande regn — outtömliga samlingar av sensuell näring helgas till detta</span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Må negativa handlingar och förvillelser samlade i förflutet, nutid och framtid omvandlas i <span class="foreign">bSangs</span> vars eld fyller hela universum</span>
                <div class="response">A: Hung: Samaya Dhuma-vali Bhrum:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Må varje atom av denna eld bli <span class="foreign">Küntuzangpo</span> och <span class="foreign">Küntuzangmo</span>: ett outtömligt moln av fullkomligheter</span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Skimrande strålar av femfärgat ljus lyser upp överallt i de sex världarna, ner till djupaste helvete</span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
            <div class="offering">
                <span class="offering-text"><span class="seed">A:</span> Må splittrade varelser uppnå <span class="foreign">Ja'lü</span></span>
                <div class="response">A: Agni-vaha: Hung:</div>
            </div>
            
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
