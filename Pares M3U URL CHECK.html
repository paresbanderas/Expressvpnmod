<!DOCTYPE html>
<html lang="pt">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Checker</title>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <style>
        body {
            background-color: #1a1a1a;
            color: #FF0000;
        }

        .container {
            text-align: center;
            margin-top: 10px;
            padding: 20px;
            border-radius: 10px;
        }
        
        body::before {
            content: "";           
            background-size: cover; /* Adaptar a imagem ao tamanho da tela */
            opacity: 0.1; /* Ajuste a opacidade conforme necessário */
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            z-index: -1;
            pointer-events: none;
        }

        .info-container {
            margin-top: 20px;
            text-align: left;
        }

        .info-label {
            font-weight: bold;
            color: white;
        }

        .camuflado {
            color: #5bc0de;
        }

        .erro {
            color: red;
        }

        .separador {
            margin-top: 10px;
        }

        #resultados-container {
            margin-top: 20px;
            text-align: left;
        }

        #output-results {
            margin-top: 20px;
            text-align: center; /* Alinhamento centralizado */
        }

        .progress-container {
            width: 100%;
            margin-top: 20px;
        }

        .progress {
            height: 25px;
        }

        #busca-container {
            margin-top: 20px;
            text-align: center; /* Alinhamento centralizado */
        }

        #inputBusca {
            width: 100%; /* Largura total */
            margin-bottom: 10px; /* Espaçamento inferior */
        }

        #entrar {
            width: 100%; /* Largura total */
        }

        #canal-encontrado {
            margin-top: 20px;
            text-align: left;
        }
    </style>
    <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
</head>

<body>
    <div class="container">
        <h1>𝐌𝟑𝐔 𝐋𝐈𝐍𝐊 𝐂𝐇𝐄𝐂𝐊</h1>
        <form class="form-inline" id="busca-container">
            <div class="input-group">
                <input type="text" class="form-control" id="linkLista" placeholder="M3U URL YAZINIZ" aria-label="M3U URL YAZINIZ" aria-describedby="basic-addon2">
                <div class="input-group-append">
                    <button type="button" class="btn btn-primary" id="entrar">CHECK</button>
                </div>
            </div>
        </form>
        <div id="resultados-container">
            <!-- Resultados serão exibidos aqui -->
        </div>
        <div id="output-results">
            <!-- Saída dos resultados -->
        </div>

        <div id="progress-container" class="progress-container" style="display: none;">
            <div class="progress">
                <div id="progress-bar" class="progress-bar" role="progressbar" style="width: 0%; background-color: #5bc0de;"
                    aria-valuenow="0" aria-valuemin="0" aria-valuemax="100">0%</div>
            </div>
        </div>

        <script>
            document.getElementById("entrar").addEventListener("click", async function () {
                var linksDigitados = document.getElementById("linkLista").value.split('\n');
                var liveStreamCount = 0;
                var seriesCount = 0;
                var vodStreamsCount = 0;

                document.getElementById("output-results").innerHTML = ""; // Limpa os resultados anteriores
                document.getElementById("progress-container").style.display = 'block';

                var inicioSolicitacao = new Date();

                for (let i = 0; i < linksDigitados.length; i++) {
                    const linkDigitado = linksDigitados[i];

                    if (linkDigitado.trim() !== "") {
                        var infoApiDiv = document.createElement("div");
                        infoApiDiv.classList.add("info-container");

                        try {
                            var url = new URL(linkDigitado);
                            var params = new URLSearchParams(url.search);
                            var usuario = params.get("username");
                            var senha = params.get("password");

                            if (usuario && senha) {
                                var host = url.hostname;
                                var porta = url.port || '';

                                var linkConstruido = "http://" + host + (porta ? ":" + porta : "") +
                                    "/player_api.php?username=" + usuario + "&password=" + senha;

                                var linkLiveStreams = linkConstruido + "&action=get_live_streams";
                                var linkSeries = linkConstruido + "&action=get_series";
                                var linkVodStreams = linkConstruido + "&action=get_vod_streams";

                                var response = await axios.get(linkConstruido);
                                var data = response.data;

                                var liveStreamsResponse = await axios.get(linkLiveStreams);
                                var liveStreamsData = liveStreamsResponse.data;

                                var seriesResponse = await axios.get(linkSeries);
                                var seriesData = seriesResponse.data;

                                var vodStreamsResponse = await axios.get(linkVodStreams);
                                var vodStreamsData = vodStreamsResponse.data;

                                if (data.user_info && data.user_info.status === "Active") {
                                    var userInfo = data.user_info;
                                    var serverInfo = data.server_info;

                                    var linksConstruidos = userInfo.allowed_output_formats.map(format => {
                                        return `<a href="${linkConstruido}&format=${format}" target="_blank">${format}</a>`;
                                    }).join(" | ");

                                    var infoElement = document.createElement("p");
                                    infoElement.innerHTML =
                                        `<span class="info-label">🗣𝐌𝟑𝐔 𝐔𝐑𝐋 𝐂𝐎𝐍𝐓𝐑𝐎𝐋  EDIT PARES ™️ </span><br>` +
                                        `<span class="info-label">📡 STATUS:</span> ${userInfo.status}<br>` +
                                        `<span class="info-label">📂 PROTOKOL:</span> ${serverInfo.server_protocol}<br>` +
                                        `<span class="info-label">🌐 SUNUCU:</span> ${serverInfo.url}<br>` +
                                        `<span class="info-label">🚪 PORT:</span> ${serverInfo.port}<br>` +
                                        `<span class="info-label">🚪 PORT HTTPS:</span> ${serverInfo.https_port}<br>` +
                                        `<span class="info-label">🚪 PORT RTMP:</span> ${serverInfo.rtmp_port}<br>` +
                                        `<span class="info-label">👤 USER:</span> ${usuario}<br>` +
                                        `<span class="info-label">🔑 PASS:</span> ${senha}<br>` +
                                        `<span class="info-label">📆 OLUŞUM TARİHİ:</span> ${new Date(userInfo.created_at * 1000).toLocaleString()}<br>` +
                                        `<span class="info-label">📆 BİTİS TARİHİ:</span> ${new Date(userInfo.exp_date * 1000).toLocaleString()}<br>` +
                                        `<span class="info-label">👩 AKTIF BAĞLANTI:</span> ${userInfo.active_cons}<br>` +
                                        `<span class="info-label">👪 MAX. BAĞLANTI:</span> ${userInfo.max_connections}<br>` +
                                        `<span class="info-label">🕓 ŞİMDİKİ ZAMAN:</span> ${serverInfo.time_now}<br>` +
                                        `<span class="info-label">📂 ERİŞİM:</span> <a href="http://${host}/client_area/index.php?username=${usuario}&password=${senha}&submit" target="_blank">GİRDİ 🟢</a><br>` +
                                        `<span class="info-label">📂 LİSTE FORMATI 👇</span><br>` +
                                        `<span class="info-label">🔗 LİNKLER:</span> ${linksConstruidos}<br>` +
                                        `<span class="info-label">🌍 KONUM:</span> ${serverInfo.timezone || 'N/A'}`;
                                        
                                        if (liveStreamsData) {
                                        infoElement.innerHTML += `<br><span class="info-label">📺 KANALLAR:</span> ${liveStreamsData.length}`;
                                        liveStreamCount += liveStreamsData.length;
                                        }
                                        
                                        if (vodStreamsData) {
                                        infoElement.innerHTML += `<br><span class="info-label">🎬 FİLMLER:</span> ${vodStreamsData.length}`;
                                        vodStreamsCount += vodStreamsData.length;
                                        }
                                        
                                        if (seriesData) {
                                        infoElement.innerHTML += `<br><span class="info-label">🍿 DİZİLER:</span> ${seriesData.length}`;
                                        seriesCount += seriesData.length;
                                        }
                                        
                                        var infoApiDiv = document.createElement("div");
                                        infoApiDiv.classList.add("info-container");
                                        infoApiDiv.appendChild(infoElement);
                                        document.getElementById("output-results").appendChild(infoApiDiv);
                                        } else {
                                        var erroElement = document.createElement("p");
                                        erroElement.innerHTML = `<span class="info-label erro">❌ Erro: Nenhuma informação encontrada ou conta inativa.</span>`;
                                        infoApiDiv.appendChild(erroElement);
                                        }
                                        }
                                        } catch (error) {
                                        var erroElement = document.createElement("p");
                                        erroElement.innerHTML = `<span class="info-label erro">❌ Erro: Não foi possível completar a solicitação.</span>`;
                                        infoApiDiv.appendChild(erroElement);
                                        }
                                        
                                        // Adiciona um separador
                                        var separador = document.createElement("p");
                                        separador.classList.add("separador");
                                        separador.innerHTML = `<span class="camuflado">𝐌𝟑𝐔 𝐔𝐑𝐋 𝐂𝐎𝐍𝐓𝐑𝐎𝐋 </span>`;
                                        document.getElementById("output-results").appendChild(separador);
                                        
                                        // Atualiza a barra de progresso
                                        var progresso = ((i + 1) / linksDigitados.length) * 100;
                                        document.getElementById("progress-bar").style.width = progresso + "%";
                                        document.getElementById("progress-bar").innerHTML = Math.round(progresso) + "%";
                                        }
                                        }
                                        
                                        // Calcula o tempo de solicitação
                                        var fimSolicitacao = new Date();
                                        var tempoSolicitacao = (fimSolicitacao - inicioSolicitacao) / 1000; // em segundos
                                        
                                        // Atualiza os contadores
                                        document.getElementById("liveStreamCounter").innerHTML = `Live Stream: ${liveStreamCount}`;
                                        document.getElementById("seriesCounter").innerHTML = `Séries: ${seriesCount}`;
                                        document.getElementById("vodStreamsCounter").innerHTML = `VOD Streams: ${vodStreamsCount}`;
                                        
                                        // Esconde a barra de progresso
                                        document.getElementById("progress-container").style.display = 'none';
                                        });
                                        </script>
                                        </div>
                                        </body>
                                        
                                        </html>