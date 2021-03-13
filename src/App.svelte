<script>
    import Operador1 from './Oper1.svelte';
    import Calculo from './Calculo.svelte';

    let primero;
    let segundo;
    let operadores = ['+', '-', '*', '/'];
    let operaUsuario = '';
    let numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0];
    let punto = '.';
    let igual = '=';
    let resultado = '';
</script>

<div>
    <section class="operacion">
        <Calculo primero={primero} operaUsuario={operaUsuario} segundo={segundo}/>

        <h1>40</h1>
    </section>
    <section>
        {#each operadores as operador}
            <button class="operadores" on:click = {function(){
                operaUsuario = operador
                console.log(operaUsuario);
            }}>
                {operador}
            </button>
        {/each}
    </section>
    <section>
        {#each numeros as numero}
            <button class="numeros">
                {numero}
            </button>
        {/each}
        <button class="punto">
            {punto}
        </button>
        <button class="igual">
            {igual}
        </button>
    </section>
</div>

<style>
    div {
       background-color: crimson;
       position:central;
       width:900px;
       height:500px;
        }

</style>
