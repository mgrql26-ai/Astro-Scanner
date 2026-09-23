<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Astro Screenshare — Scanner Completo</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      background: #0a0a0a; color: #fff;
      font-family: 'Inter', sans-serif; min-height: 100vh;
      overflow-x: hidden; position: relative;
    }
    body::before {
      content: ""; position: fixed; top: 0; left: 0;
      width: 100%; height: 100%;
      background: repeating-linear-gradient(90deg, transparent, transparent 40px, rgba(255,255,255,0.015) 40px, rgba(255,255,255,0.015) 41px);
      pointer-events: none; z-index: 0;
    }
    .container { display: flex; min-height: 100vh; position: relative; z-index: 1; }
    .left-side { flex: 1; padding: 30px 20px; display: flex; flex-direction: column; width: 100%; }
    .header { margin-bottom: 25px; text-align: center; }
    .developer { font-size: 12px; letter-spacing: 2px; color: #ccc; margin-bottom: 8px; }
    .logo { font-family: 'Great Vibes', cursive; font-size: 42px; line-height: 1; }
    .subtitle { font-size: 13px; letter-spacing: 5px; color: #aaa; margin-top: 5px; }
    .status {
      display: inline-flex; align-items: center; gap: 8px;
      background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1);
      padding: 6px 14px; border-radius: 20px; font-size: 12px; margin-top: 15px;
    }
    .status-dot {
      width: 8px; height: 8px; background: #22c55e; border-radius: 50%;
      box-shadow: 0 0 8px #22c55e;
    }
    .center-content {
      flex: 1; display: flex; flex-direction: column;
      justify-content: center; align-items: center; text-align: center; padding: 10px;
      width: 100%; max-width: 550px; margin: 0 auto;
    }
    .main-title { font-family: 'Great Vibes', cursive; font-size: 36px; margin-bottom: 15px; }
    .system-title { font-size: 13px; letter-spacing: 3px; color: #bbb; margin-bottom: 20px; }

    /* LOGIN */
    .login-box {
      background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.1);
      border-radius: 15px; padding: 30px; width: 100%; max-width: 400px;
    }
    .login-title { font-size: 17px; letter-spacing: 2px; color: #aaa; margin-bottom: 20px; }
    .form-group { margin-bottom: 18px; text-align: left; }
    .form-group label { display: block; font-size: 12px; letter-spacing: 1px; color: #888; margin-bottom: 6px; }
    .form-group input {
      width: 100%; background: #1a1a1a; border: 1px solid #333; color: #fff;
      padding: 12px 14px; border-radius: 8px; font-size: 14px; outline: none;
    }
    .btn-entrar {
      width: 100%; background: linear-gradient(90deg, #4a6cf7, #7b2ffd);
      color: #fff; border: none; padding: 13px; border-radius: 8px;
      font-size: 14px; font-weight: 600; cursor: pointer; transition: transform 0.2s;
    }
    .btn-entrar:hover { transform: scale(1.03); }
    .erro { color: #ff4444; margin-top: 12px; font-size: 13px; display: none; }

    /* SCANNER */
    .area-scanner { display: none; width: 100%; }
    .tabs { display: flex; gap: 10px; margin-bottom: 25px; justify-content: center; flex-wrap: wrap; }
    .tab-btn {
      background: transparent; border: 1px solid rgba(255,255,255,0.2); color: #aaa;
      padding: 10px 18px; border-radius: 20px; cursor: pointer; transition: all 0.3s; font-size: 13px;
    }
    .tab-btn.active { background: rgba(74,108,247,0.2); border-color: #4a6cf7; color: #fff; }
    .tab-content { display: none; width: 100%; }
    .tab-content.active { display: block; }

    /* ÁREA DE ARRASTAR ARQUIVO */
    .drop-area {
      border: 2px dashed rgba(255,255,255,0.25);
      border-radius: 12px; padding: 40px 20px;
      text-align: center; cursor: pointer; transition: all 0.3s;
      margin-bottom: 20px;
      background: rgba(255,255,255,0.02);
    }
    .drop-area.highlight {
      border-color: #4a6cf7; background: rgba(74,108,247,0.08);
    }
    .drop-icon { font-size: 32px; margin-bottom: 10px; }
    .drop-text { color: #ccc; font-size: 14px; margin-bottom: 5px; }
    .drop-sub { color: #777; font-size: 12px; }
    .file-name { color: #44ff44; font-weight: bold; margin-top: 10px; word-break: break-all; }

    .btn-analisar {
      background: linear-gradient(90deg, #22c55e, #16a34a);
      color: #fff; border: none; padding: 12px 30px; border-radius: 30px;
      font-size: 14px; font-weight: 600; cursor: pointer; transition: all 0.3s;
      margin-bottom: 20px; width: 100%;
    }
    .btn-analisar:disabled { opacity: 0.4; cursor: not-allowed; }

    #resultados {
      background: rgba(255,255,255,0.05); padding: 20px; border-radius: 10px;
      border: 1px solid rgba(255,255,255,0.1); text-align: left; min-height: 100px;
      max-height: 400px; overflow-y: auto;
    }
    .safe { color: #44ff44; font-weight: bold; }
    .warning { color: #ffcc00; font-weight: bold; }
    .danger { color: #ff4444; font-weight: bold; }
    .aviso { color: #ffcc00; font-size: 12px; margin: 10px 0; font-style: italic; line-height: 1.5; }
    .verses { max-width: 480px; text-align: left; margin-top: 25px; }
    .verse { margin-bottom: 15px; }
    .verse p { font-size: 13px; color: #ccc; font-style: italic; line-height: 1.5; }
    .verse span { font-size: 11px; color: #666; letter-spacing: 1px; }

    @media (max-width: 600px) {
      .main-title { font-size: 28px; }
      .logo { font-size: 32px; }
      .left-side { padding: 15px; }
      .drop-area { padding: 30px 15px; }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="left-side">
      <div class="header">
        <div class="developer">DEVELOPED BY ASTRO ♥</div>
        <div class="logo">Astro</div>
        <div class="subtitle">SCREENSHARE ANTI-CHEAT</div>
        <div class="status">
          <div class="status-dot"></div>
          STATUS Ativo
        </div>
      </div>

      <div class="center-content">
        <!-- TELA DE LOGIN -->
        <div id="tela-login" class="login-box">
          <h2 class="login-title">🔐 ACESSO RESTRITO</h2>
          <div class="form-group">
            <label>USUÁRIO</label>
            <input type="text" id="usuario" placeholder="astro">
          </div>
          <div class="form-group">
            <label>SENHA</label>
            <input type="password" id="senha" placeholder="123">
          </div>
          <button class="btn-entrar" onclick="verificarLogin()">ENTRAR</button>
          <p id="msg-erro" class="erro">Usuário ou senha incorretos!</p>
        </div>

        <!-- TELA DO SCANNER -->
        <div id="tela-scanner" class="area-scanner">
          <h1 class="main-title">Scanner</h1>
          <p class="system-title">Análise de Arquivos do Sistema</p>

          <!-- ABAS -->
          <div class="tabs">
            <button class="tab-btn active" onclick="mudarAba('ios')">🍎 iOS — sysdiagnose</button>
            <button class="tab-btn" onclick="mudarAba('android')">🤖 Android — BugReport</button>
          </div>

          <!-- ABA iOS → ARRASTAR sysdiagnose -->
          <div id="aba-ios" class="tab-content active">
            <div 
              id="drop-ios" 
              class="drop-area"
              ondragover="event.preventDefault(); this.classList.add('highlight')"
              ondragleave="this.classList.remove('highlight')"
              ondrop="soltouArquivo(event, 'ios')"
              onclick="document.getElementById('input-ios').click()"
            >
              <div class="drop-icon">📁</div>
              <p class="drop-text">Arraste o arquivo <strong>sysdiagnose</strong> aqui</p>
              <p class="drop-sub">ou toque para selecionar</p>
              <input type="file" id="input-ios" style="display:none;" onchange="escolheuArquivo(this, 'ios')">
              <div id="nome-arquivo-ios" class="file-name"></div>
            </div>
            <button class="btn-analisar" id="btn-ios" onclick="analisarArquivo('ios')" disabled>🔍 ANALISAR SYS-DIAGNOSE</button>
            <p class="aviso">⚠️ O arquivo pode estar compactado (.tar.gz) — o sistema lê o conteúdo de texto</p>
            
            <div id="resultados-ios" style="display:none; margin-top:15px;">
              <h4 style="color:#aaa; margin-bottom:10px;">📋 Resultado da Análise:</h4>
              <div id="conteudo-ios"></div>
            </div>
          </div>

          <!-- ABA ANDROID → ARRASTAR BugReport -->
          <div id="aba-android" class="tab-content">
            <div 
              id="drop-android" 
              class="drop-area"
              ondragover="event.preventDefault(); this.classList.add('highlight')"
              ondragleave="this.classList.remove('highlight')"
              ondrop="soltouArquivo(event, 'android')"
              onclick="document.getElementById('input-android').click()"
            >
              <div class="drop-icon">📋</div>
              <p class="drop-text">Arraste o arquivo <strong>BugReport</strong> aqui</p>
              <p class="drop-sub">ou toque para selecionar</p>
              <input type="file" id="input-android" style="display:none;" onchange="escolheuArquivo(this, 'android')">
              <div id="nome-arquivo-android" class="file-name"></div>
            </div>
            <button class="btn-analisar" id="btn-android" onclick="analisarArquivo('android')" disabled>🔍 ANALISAR BUGREPORT</button>
            <p class="aviso">⚠️ Sempre gere BugReport com depuração DESATIVADA e buffer de logs no MÁXIMO</p>
            
            <div id="resultados-android" style="display:none; margin-top:15px;">
              <h4 style="color:#aaa; margin-bottom:10px;">📋 Resultado da Análise:</h4>
              <div id="conteudo-android"></div>
            </div>
          </div>

          <div class="verses">
            <div class="verse">
              <p>"Tudo posso naquele que me fortalece."</p>
              <span>FILIPENSES 4 · 13</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <script>
    // ==============================================
    // LOGIN — astro / 123
    // ==============================================
    function verificarLogin() {
      const user = document.getElementById('usuario').value.trim();
      const pass = document.getElementById('senha').value.trim();
      const erro = document.getElementById('msg-erro');

      if (user === 'astro' && pass === '123') {
        document.getElementById('tela-login').style.display = 'none';
        document.getElementById('tela-scanner').style.display = 'block';
      } else {
        erro.style.display = 'block';
      }
    }

    // ==============================================
    // MUDAR ABA
    // ==============================================
    function mudarAba(nome) {
      document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
      document.querySelectorAll('.tab-content').forEach(c => c.classList.remove('active'));
      event.target.classList.add('active');
      document.getElementById('aba-' + nome).classList.add('active');
    }

    // ==============================================
    // GERENCIAR ARQUIVO
    // ==============================================
    let arquivoAtual = { ios: null, android: null };

    function soltouArquivo(e, tipo) {
      e.preventDefault();
      document.getElementById('drop-' + tipo).classList.remove('highlight');
      const arq = e.dataTransfer.files[0];
      guardarArquivo(arq, tipo);
    }

    function escolheuArquivo(input, tipo) {
      const arq = input.files[0];
      if (arq) guardarArquivo(arq, tipo);
    }

    function guardarArquivo(arq, tipo) {
      arquivoAtual[tipo] = arq;
      document.getElementById('nome-arquivo-' + tipo).textContent = '✅ ' + arq.name;
      document.getElementById('btn-' + tipo).disabled = false;
    }

    // ==============================================
    // BANCO DE DETECÇÃO
    // ==============================================
    const palavrasIOS = [
      {n:'lockdownd',t:'Serviço de comunicação externa — possível conexão remota'},
      {n:'usbmuxd',t:'USB Multiplexing — ponte de acesso'},
      {n:'62078',t:'Porta Lockdownd aberta'},
      {n:'libimobiledevice',t:'Biblioteca de controle remoto'},
      {n:'pymobiledevice3',t:'Automação via Python'},
      {n:'TrollStore',t:'Instalação sem validação do sistema'},
      {n:'Filza',t:'Gerenciador de arquivos raiz'},
      {n:'unc0ver',t:'Jailbreak detectado'},
      {n:'checkra1n',t:'Jailbreak detectado'},
      {n:'sysdiagnose',t:'Coleta de dados do sistema — normal'},
      {n:'com-luxebypass',t:'Pacote de Bypass detectado'},
      {n:'proxy',t:'Palavra Proxy encontrada — investigar'},
      {n:'78f',t:'Código suspeito (Zeex)'},
      {n:'d14',t:'Código suspeito (Zeex)'},
      {n:'1ea',t:'Código suspeito (Fatality)'},
      {n:'authproxy',t:'Proxy de autenticação'}
    ];

    const palavrasAndroid = [
      {n:'androidboot.verifiedbootstate=orange',t:'⚠️ BootLoader DESBLOQUEADO → Aplicar W.O',tipo:'warn'},
      {n:'androidboot.verifiedbootstate=red',t:'🚩 Sistema MODIFICADO → Aplicar W.O',tipo:'danger'},
      {n:'Zygisk',t:'⚠️ Zygisk — injeção de código',tipo:'warn'},
      {n:'zygisk',t:'⚠️ Zygisk — injeção de código',tipo:'warn'},
      {n:'Magisk',t:'🚩 Magisk — Root detectado',tipo:'danger'},
      {n:'magisk',t:'🚩 Magisk — Root detectado',tipo:'danger'},
      {n:'KernelSU',t:'🚩 KernelSU — Root detectado',tipo:'danger'},
      {n:'kernelsu',t:'🚩 KernelSU — Root detectado',tipo:'danger'},
      {n:'Apatch',t:'🚩 APatch — Root detectado',tipo:'danger'},
      {n:'apatch',t:'🚩 APatch — Root detectado',tipo:'danger'},
      {n:'vbmetafix',t:'⚠️ Correção de partição — ocultação de Root',tipo:'warn'},
      {n:'tricky_store',t:'🚩 Bypass de certificados',tipo:'danger'},
      {n:'zn-daemon64',t:'⚠️ Daemon de Root rodando',tipo:'warn'},
      {n:'/data/adb/modules',t:'🚩 Diretório de módulos Root',tipo:'danger'},
      {n:'cleanerBugReport',t:'🚩 Ferramenta de limpeza de logs',tipo:'danger'},
      {n:'pm grant com.conena.logcat.reader android.permission.READ_LOGS',t:'⚠️ Permissão de leitura de logs concedida',tipo:'warn'},
      {n:'AdbEnabled',t:'⚠️ ADB ativado — verificar horário',tipo:'warn'},
      {n:'UsbDebugging',t:'⚠️ Depuração USB ativada',tipo:'warn'},
      {n:'WirelessDebugging',t:'⚠️ Depuração sem fio ativada',tipo:'warn'},
      {n:'u0_a',t:'⚠️ Usuário local — verificar se é Termux',tipo:'warn'},
      {n:'com.proxy.free',t:'🚩 Pacote Proxy Free',tipo:'danger'},
      {n:'com.proxyff.app',t:'🚩 Pacote Proxy FF',tipo:'danger'},
      {n:'delete',t:'⚠️ Evento de remoção de aplicativo',tipo:'warn'},
      {n:'uninstall',t:'⚠️ Desinstalação detectada',tipo:'warn'},
      {n:'Shell (2000)',t:'⚠️ Comando executado como root/shell',tipo:'warn'}
    ];

    // ==============================================
    // LER E ANALISAR ARQUIVO
    // ==============================================
    function analisarArquivo(tipo) {
      const arq = arquivoAtual[tipo];
      if (!arq) return;

      const leitor = new FileReader();
      leitor.onload = function(e) {
        const conteudo = e.target.result.toLowerCase();
        const lista = tipo === 'ios' ? palavrasIOS : palavrasAndroid;
        const achou = [];

        lista.forEach(item => {
          if (conteudo.includes(item.n.toLowerCase())) {
            if (!achou.find(x => x.n === item.n)) achou.push(item);
          }
        });

        const div = document.getElementById('conteudo-' + tipo);
        document.getElementById('resultados-' + tipo).style.display = 'block';

        if (achou.length === 0) {
          div.innerHTML = `<p class="safe">✅ NENHUMA AMEAÇA DETECTADA — Arquivo limpo</p>`;
        } else {
          let html = `<p class="danger">⚠️ ${achou.length} ITEM(NS) ENCONTRADO(S):</p>`;
          achou.forEach(item => {
            const classe = item.tipo === 'danger' ? 'danger' : (item.tipo === 'warn' ? 'warning' : 'safe');
            html += `<p style="margin:8px 0;" class="${classe}">• ${item.n}</p><p style="color:#aaa; font-size:12px; margin:0 0 8px 18px;">${item.t}</p>`;
          });
          div.innerHTML = html;
        }
      };
      leitor.readAsText(arq);
    }
  </script>
</body>
</html>
