html
<script>
    // Estado do formulário
    let nome = '';
    let email = '';
    let senha = '';
    let mensagem = '';

    // Função para lidar com o envio
    async function handleCadastro() {
        // Validação simples
        if (senha.length < 6) {
            mensagem = 'A senha deve ter pelo menos 6 caracteres.';
            return;
        }

        // Simulação de envio para API
        console.log('Dados de cadastro:', { nome, email, senha });
        mensagem = `Cadastro de ${nome} realizado com sucesso!`;
        
        // Limpar campos
        nome = '';
        email = '';
        senha = '';
    }
</script>

<main class="container">
    <form on:submit|preventDefault={handleCadastro}>
        <h1>Cadastro</h1>

        <label for="nome">Nome:</label>
        <input type="text" id="nome" bind:value={nome} required />

        <label for="email">E-mail:</label>
        <input type="email" id="email" bind:value={email} required />

        <label for="senha">Senha:</label>
        <input type="password" id="senha" bind:value={senha} required />

        <button type="submit">Cadastrar</button>

        {#if mensagem}
            <p class="mensagem">{mensagem}</p>
        {/if}
    </form>
</main>

<style>
    .container { display: flex; justify-content: center; padding: 2rem; }
    form { display: flex; flex-direction: column; width: 300px; gap: 1rem; }
    input { padding: 0.5rem; }
    button { padding: 0.5rem; background-color: #ff3e00; color: white; border: none; cursor: pointer; }
    .mensagem { color: green; font-weight: bold; }
</style>