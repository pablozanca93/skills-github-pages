<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadastro de CTOs</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f7fc;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
        }

        .container {
            background: #fff;
            padding: 20px;
            width: 100%;
            max-width: 500px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
        }

        h2 {
            text-align: center;
            margin-bottom: 20px;
        }

        input, button {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border-radius: 6px;
            border: 1px solid #ccc;
            font-size: 16px;
        }

        input:focus, button:hover {
            border-color: #007bff;
            outline: none;
        }

        button {
            background-color: #007bff;
            color: white;
            cursor: pointer;
        }

        button:disabled {
            background-color: #aaa;
            cursor: not-allowed;
        }

        .error {
            color: red;
            font-size: 14px;
            margin-top: -8px;
        }

        .success {
            color: green;
            margin-top: 10px;
            font-size: 14px;
        }

        .cto-list {
            margin-top: 20px;
            width: 100%;
            max-width: 500px;
        }

        .cto-item {
            background: #fff;
            padding: 15px;
            margin-bottom: 10px;
            border-radius: 8px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
        }

        .delete-btn {
            background-color: #e74c3c;
            color: white;
            padding: 5px 10px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 14px;
        }

        .delete-btn:hover {
            background-color: #c0392b;
        }

        .search-container {
            margin-top: 20px;
            width: 100%;
            max-width: 500px;
            display: flex;
            justify-content: center;
        }

        .search-container input {
            width: 80%;
            padding: 10px;
            font-size: 16px;
            border-radius: 6px;
            border: 1px solid #ccc;
        }

    </style>
</head>
<body>

    <div class="container">
        <h2>Cadastro de CTOs</h2>
        <form id="ctoForm">
            <input type="text" id="anel" placeholder="ANEL (0 a 999)" maxlength="3">
            <div class="error" id="anelError"></div>

            <input type="number" id="cto" placeholder="CTO (0 a 999)" maxlength="3">
            <div class="error" id="ctoError"></div>

            <input type="text" id="endereco" placeholder="Endereço (Exemplo: Rua 08, Parque das Camélias)">
            <div class="error" id="enderecoError"></div>

            <input type="text" id="googleMapsLink" placeholder="Link do Google Maps (https://maps.app.goo.gl/...)">
            <div class="error" id="googleMapsLinkError"></div>

            <button type="submit">Cadastrar</button>
        </form>
        <div class="success" id="successMsg"></div>
    </div>

    <div class="search-container">
        <input type="text" id="searchInput" placeholder="Buscar por ANEL, CTO, Endereço, Bairro ou Rua">
    </div>

    <div class="cto-list" id="ctoList"></div>

    <script>
        function pedirSenha() {
            let senha = prompt("Digite a senha para continuar:");
            return senha === "162614";
        }

        function loadCTOs() {
            let ctoListDiv = document.getElementById("ctoList");
            ctoListDiv.innerHTML = "";

            let ctoList = JSON.parse(localStorage.getItem("ctos")) || [];

            if (ctoList.length === 0) {
                ctoListDiv.innerHTML = "<p style='text-align: center; color: #aaa;'>Nenhuma CTO cadastrada.</p>";
            }

            ctoList.forEach((cto, index) => {
                let ctoItem = document.createElement("div");
                ctoItem.classList.add("cto-item");
                ctoItem.innerHTML = `
                    <span><strong>Anel:</strong> ${cto.anel}</span>
                    <span><strong>CTO:</strong> ${cto.cto}</span>
                    <span><strong>Endereço:</strong> ${cto.endereco}</span>
                    <a href="${cto.location}" target="_blank">Abrir Localização</a>
                    <button class="delete-btn" onclick="deleteCTO(${index})">Excluir</button>
                `;
                ctoListDiv.appendChild(ctoItem);
            });
        }

        function deleteCTO(index) {
            if (!pedirSenha()) {
                alert("Senha incorreta! Operação cancelada.");
                return;
            }

            let ctoList = JSON.parse(localStorage.getItem("ctos")) || [];
            ctoList.splice(index, 1);
            localStorage.setItem("ctos", JSON.stringify(ctoList));
            loadCTOs();
        }

        document.getElementById("ctoForm").addEventListener("submit", function(event) {
            event.preventDefault();

            let anel = document.getElementById("anel").value.trim();
            let cto = document.getElementById("cto").value.trim();
            let endereco = document.getElementById("endereco").value.trim();
            let googleMapsLink = document.getElementById("googleMapsLink").value.trim();
            let anelError = document.getElementById("anelError");
            let ctoError = document.getElementById("ctoError");
            let enderecoError = document.getElementById("enderecoError");
            let googleMapsLinkError = document.getElementById("googleMapsLinkError");
            let successMsg = document.getElementById("successMsg");

            let anelRegex = /^\d{1,3}$/;
            let ctoRegex = /^\d{1,3}$/;
            let googleMapsLinkRegex = /^https:\/\/maps\.app\.goo\.gl\/[a-zA-Z0-9-_]+$/;

            if (!anelRegex.test(anel)) {
                anelError.textContent = "ANEL deve ter de 1 a 3 dígitos.";
                return;
            } else {
                anelError.textContent = "";
            }

            if (!ctoRegex.test(cto)) {
                ctoError.textContent = "CTO deve ter de 1 a 3 dígitos.";
                return;
            } else {
                ctoError.textContent = "";
            }

            if (endereco.length === 0) {
                enderecoError.textContent = "Endereço não pode estar vazio.";
                return;
            } else {
                enderecoError.textContent = "";
            }

            if (!googleMapsLinkRegex.test(googleMapsLink)) {
                googleMapsLinkError.textContent = "O link do Google Maps deve ser no formato https://maps.app.goo.gl/...";
                return;
            } else {
                googleMapsLinkError.textContent = "";
            }

            if (!pedirSenha()) {
                alert("Senha incorreta! Operação cancelada.");
                return;
            }

            let ctoList = JSON.parse(localStorage.getItem("ctos")) || [];
            ctoList.push({ anel, cto, endereco, location: googleMapsLink });
            localStorage.setItem("ctos", JSON.stringify(ctoList));

            successMsg.textContent = "CTO cadastrada com sucesso!";
            loadCTOs();
        });

        document.getElementById("searchInput").addEventListener("input", function() {
            let query = document.getElementById("searchInput").value.toLowerCase();
            let ctoList = JSON.parse(localStorage.getItem("ctos")) || [];

            let filteredCTOs = ctoList.filter(cto => {
                return cto.anel.toString().includes(query) || 
                       cto.cto.toString().includes(query) || 
                       cto.endereco.toLowerCase().includes(query);
            });

            let ctoListDiv = document.getElementById("ctoList");
            ctoListDiv.innerHTML = "";

            if (filteredCTOs.length === 0) {
                ctoListDiv.innerHTML = "<p style='text-align: center; color: #aaa;'>Nenhuma CTO encontrada.</p>";
            } else {
                filteredCTOs.forEach((cto, index) => {
                    let ctoItem = document.createElement("div");
                    ctoItem.classList.add("cto-item");
                    ctoItem.innerHTML = `
                        <span><strong>Anel:</strong> ${cto.anel}</span>
                        <span><strong>CTO:</strong> ${cto.cto}</span>
                        <span><strong>Endereço:</strong> ${cto.endereco}</span>
                        <a href="${cto.location}" target="_blank">Abrir Localização</a>
                        <button class="delete-btn" onclick="deleteCTO(${index})">Excluir</button>
                    `;
                    ctoListDiv.appendChild(ctoItem);
                });
            }
        });

        loadCTOs();
    </script>

</body>
</html>
