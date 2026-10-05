# projeto-ecomerce
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário Aprimorado</title>
    <style>
        /* Reset basico de box-sizing */
        *, *::before, *::after {
            box-sizing: border-box;
        }

        body {
            background-color: #f8fafc;
            font-family: system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
            margin: 0;
            padding: 32px 16px;
            color: #1e293b;
            display: flex;
            justify-content: center;
        }

        .container {
            width: 100%;
            max-width: 520px;
        }

        h1 {
            color: #0b41bc;
            font-size: 1.75rem;
            margin-top: 0;
            margin-bottom: 24px;
        }

        fieldset {
            background-color: #ffffff;
            border: 1px solid #e2e8f0;
            border-radius: 12px;
            padding: 24px;
            margin-bottom: 20px;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
        }

        legend {
            color: #d97706;
            font-weight: 600;
            font-size: 0.95rem;
            padding: 0 8px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 6px;
            margin-bottom: 16px;
        }

        .form-group:last-child {
            margin-bottom: 0;
        }

        label {
            font-size: 0.875rem;
            font-weight: 500;
            color: #475569;
        }

        /* Estilização consistente de todos os inputs */
        input[type="text"],
        input[type="email"],
        input[type="date"],
        input[type="number"],
        select,
        textarea {
            width: 100%;
            padding: 10px 12px;
            border: 1px solid #cbd5e1;
            border-radius: 6px;
            font-family: inherit;
            font-size: 0.95rem;
            color: #0f172a;
            background-color: #ffffff;
            transition: border-color 0.15s ease, box-shadow 0.15s ease;
        }

        /* Feedback visual ao focar no campo */
        input[type="text"]:focus,
        input[type="email"]:focus,
        input[type="date"]:focus,
        input[type="number"]:focus,
        select:focus,
        textarea:focus {
            outline: none;
            border-color: #0b41bc;
            box-shadow: 0 0 0 3px rgba(11, 65, 188, 0.15);
        }

        /* Agrupamento de botoes */
        .acoes-formulario {
            display: flex;
            gap: 12px;
            margin-top: 24px;
        }

        /* Botão principal */
        .botao-principal {
            background-color: #0b41bc;
            color: #ffffff;
            border: none;
            padding: 12px 20px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 0.95rem;
            font-weight: 600;
            transition: background-color 0.15s ease;
        }

        .botao-principal:hover {
            background-color: #093399;
        }

        .botao-principal:focus-visible {
            outline: 2px solid #0b41bc;
            outline-offset: 2px;
        }

        /* Botão secundário */
        .botao-secundario {
            background-color: #f1f5f9;
            color: #475569;
            border: 1px solid #cbd5e1;
            padding: 12px 20px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 0.95rem;
            font-weight: 500;
            transition: background-color 0.15s ease, border-color 0.15s ease;
        }

        .botao-secundario:hover {
            background-color: #e2e8f0;
            color: #1e293b;
        }

        /* Valor total com contraste adequado (WCAG AA) */
        #total {
            font-weight: 700;
            color: #15803d;
            font-size: 1.125rem;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Cadastro de Pedido</h1>

        <form>
            <fieldset>
                <legend>Informações Gerais</legend>
                
                <div class="form-group">
                    <label for="nome">Nome Completo</label>
                    <input type="text" id="nome" placeholder="Digite seu nome">
                </div>

                <div class="form-group">
                    <label for="email">E-mail</label>
                    <input type="email" id="email" placeholder="nome@exemplo.com">
                </div>

                <div class="form-group">
                    <label for="quantidade">Quantidade</label>
                    <input type="number" id="quantidade" min="1" value="1">
                </div>
            </fieldset>

            <fieldset>
                <legend>Resumo</legend>
                <p>Total a pagar: <span id="total">R$ 150,00</span></p>
            </fieldset>

            <div class="acoes-formulario">
                <button type="submit" class="botao-principal">Enviar</button>
                <button type="reset" class="botao-secundario">Limpar</button>
            </div>
        </form>
    </div>

</body>
</html>

