<script>
        


    let nome = '';
    let email = '';
    let senha = '';
    let mensagem = '';
    let erro = '';

    async function handleCadastro() {
        mensagem = '';
        erro = '';

        // Validação
        if (senha.length < 6) {
            erro = 'A senha deve ter pelo menos 6 caracteres.';
            return;
        }

        try {
            // Simulação de API
            console.log('Dados enviados:', {
                nome,
                email,
                senha
            });

            mensagem = `Cadastro de ${nome} realizado com sucesso!`;

            // Limpar formulário
            nome = '';
            email = '';
            senha = '';

        } catch (e) {
            erro = 'Erro ao realizar cadastro.';
        }
    }
</script>

<main class="container">
    <form on:submit|preventDefault={handleCadastro}>
        <h1>Cadastro</h1>

        <label for="nome">Nome</label>
        <input
            type="text"
            id="nome"
            bind:value={nome}
            placeholder="Digite seu nome"
            required
        />

        <label for="email">E-mail</label>
        <input
            type="email"
            id="email"
            bind:value={email}
            placeholder="Digite seu e-mail"
            required
        />

        <label for="senha">Senha</label>
        <input
            type="password"
            id="senha"
            bind:value={senha}
            placeholder="Mínimo 6 caracteres"
            required
        />

        <button type="submit">
            Cadastrar
        </button>

        {#if mensagem}
            <p class="sucesso">{mensagem}</p>
            
        {/if}

        {#if erro}
            <p class="erro">{erro}</p>
        {/if}
    </form>
</main>

<style>
    .container {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        background: #f5f5f5;
    }

    form {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        width: 320px;
        padding: 2rem;
        background: white;
        border-radius: 10px;
        box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    h1 {
        text-align: center;
        margin-bottom: 1rem;
    }

    input {
        padding: 0.75rem;
        border: 1px solid #ccc;
        border-radius: 6px;
    }

    button {
        padding: 0.75rem;
        border: none;
        border-radius: 6px;
        background: #ff3e00;
        color: white;
        font-weight: bold;
        cursor: pointer;
        transition: 0.2s;
    }

    button:hover {
        background: #e63700;
    }

    .sucesso {
        color: green;
        font-weight: bold;
        text-align: center;
    }

    .erro {
        color: red;
        font-weight: bold;
        text-align: center;
    }
</style>