![cenario-passo0](https://github.com/user-attachments/assets/519f858c-aff4-47d3-84c6-b73c33812aa1)
![cenario-passo11-cidade-perdida](https://github.com/user-attachments/assets/ac29fcbb-a33b-46ae-a161-b70655ad23c8)
![cenario-passo4-voltar-casa](https://github.com/user-attachments/assets/0307340c-11d9-4fdb-8760-d32013f8fed8)

<main>
    <div class="passo ativo" id="passo-0">
        <img src="cenario-passo0.png" alt="">
        <p>Um dia desses, dentro de um livro da biblioteca da escola, eu descobri uma carta antiga sobre uma cidade
            perdida, escondida por riquezas e belezas naturais. Nessa carta, a autora deixa algumas pistas para
            encontrar essa cidade e eu decidi segui-las!</p>
        <button class="btn-proximo" data-proximo="1">Rio de Janeiro</button>
        <button class="btn-proximo" data-proximo="2">Pernambuco</button>
    </div>
    <div class="passo" id="passo-1">
        <p>Você começa sua jornada no Rio de Janeiro, subindo o Pico da Tijuca ao amanhecer para encontrar a primeira
            pista.</p>
        <button class="btn-proximo" data-proximo="3">Procurar a pista no topo do pico</button>
        <button class="btn-proximo" data-proximo="4">Desistir e voltar para casa</button>
    </div>
    <div class="passo" id="passo-2">
        <p>Em Pernambuco, você visita a histórica cidade de Olinda. Na carta, uma das pistas indica que para localizar a
            entrada para a cidade perdida você deve procurar a próxima pista em um dos pontos turísticos da cidade. Por
            qual você começa?</p>
        <button class="btn-proximo" data-proximo="5">Investigar as igrejas antigas</button>
        <button class="btn-proximo" data-proximo="6">Explorar as praias próximas</button>
    </div>
    <div class="passo" id="passo-3">
        <p>No topo do Pico da Tijuca, você encontra uma antiga inscrição apontando que a próxima pista está localizada
            no Amazonas.</p>
        <button class="btn-proximo" data-proximo="7">Seguir para o Amazonas</button>
    </div>

    <div class="passo" id="passo-4">
        <p>Você decide que a aventura é grande demais e volta para casa, mas sempre se pergunta o que teria encontrado.
        </p>
    </div>

    <div class="passo" id="passo-5">
        <p>Nas igrejas de Olinda, você descobre um mapa antigo escondido atrás de um altar, apontando que a próxima
            pista está no Amazonas.</p>
        <button class="btn-proximo" data-proximo="7">Viajar para o Amazonas</button>
    </div>

    <div class="passo" id="passo-6">
        <p>Explorando as praias, você encontra uma caverna escondida, mas ela leva a um beco sem saída.</p>
        <button class="btn-proximo" data-proximo="8">Voltar e explorar as igrejas</button>
    </div>

    <div class="passo" id="passo-7">
        <p>No Amazonas, a busca pela cidade perdida se intensifica. Você se depara com um rio bifurcado.</p>
        <button class="btn-proximo" data-proximo="9">Seguir pelo rio à esquerda</button>
        <button class="btn-proximo" data-proximo="10">Seguir pelo rio à direita</button>
    </div>

    <div class="passo" id="passo-8">
        <p>De volta às igrejas, você finalmente encontra o mapa antigo. Agora, para o Amazonas!</p>
        <button class="btn-proximo" data-proximo="7">Seguir para o Amazonas</button>
    </div>

    <div class="passo" id="passo-9">
        <p>O rio à esquerda leva você a uma cachoeira escondida com inscrições antigas que revelam a entrada da cidade
            perdida.</p>
        <button class="btn-proximo" data-proximo="11">Explorar a cidade perdida</button>
    </div>

    <div class="passo" id="passo-10">
        <p>O rio à direita termina em uma área pantanosa. Apesar de belas vistas, não há sinais da cidade perdida aqui.
        </p>
        <button class="btn-proximo" data-proximo="12">Retornar e tentar o outro rio</button>
    </div>

    <div class="passo" id="passo-11">
        <p>Dentro da cidade perdida, você descobre tesouros inimagináveis e decide se dedicar a estudar e preservar este
            lugar</p>
    </div>

    <div class="passo" id="passo-12">
        <p>Retornando e escolhendo o rio à esquerda, você finalmente encontra a cachoeira escondida e as inscrições que
            levam à cidade perdida.</p>
        <button class="btn-proximo" data-proximo="11">Explorar a cidade perdida</button>
    </div>
</main>

onst avanca = document.querySelectorAll('.btn-proximo');

avanca.forEach(button => {
    button.addEventListener('click', function(){
        const atual = document.querySelector('.ativo');
        const proximoPasso = 'passo-' + this.getAttribute('data-proximo');

        atual.classList.remove('ativo');
        document.getElementById(proximoPasso).classList.add('ativo');
    })
})

body {
    background-color: #1D4221;
    color: white;
    font-family: "Bai Jamjuree", sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 700px;
    margin: 0;
}

button {
    background-color: #64A712;
    color: white;
    font-family: "Bai Jamjuree", sans-serif;
}
img {
    max-width: 90%;
}
