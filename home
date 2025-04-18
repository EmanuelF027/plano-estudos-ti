<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Plano de Estudos de Emanuel Ferreira - Transição para TI</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.8.1/font/bootstrap-icons.css">
    <style>
        :root {
            --primary-color: #4361ee;
            --secondary-color: #3a0ca3;
            --success-color: #4cc9f0;
            --info-color: #4895ef;
            --warning-color: #f72585;
            --danger-color: #7209b7;
            --light-color: #f8f9fa;
            --dark-color: #212529;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f5f7fb;
            color: #333;
        }
        .header {
            background-color: var(--primary-color);
            color: white;
            padding: 2rem 0;
            margin-bottom: 2rem;
        }
        .card {
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            margin-bottom: 2rem;
            border: none;
        }
        .card-header {
            background-color: var(--primary-color);
            color: white;
            border-radius: 10px 10px 0 0 !important;
            font-weight: 600;
        }
        .btn-primary {
            background-color: var(--primary-color);
            border-color: var(--primary-color);
        }
        .btn-primary:hover {
            background-color: var(--secondary-color);
            border-color: var(--secondary-color);
        }
        .progress-bar {
            background-color: var(--success-color);
        }
        .task-item {
            padding: 10px;
            border-radius: 5px;
            background-color: #f8f9fa;
            margin-bottom: 10px;
        }
        .text-decoration-line-through {
            text-decoration: line-through;
            color: #6c757d;
        }
        .calendar-container {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 5px;
            margin-top: 15px;
        }
        .calendar-day {
            aspect-ratio: 1/1;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: #e9ecef;
            border-radius: 5px;
            font-weight: 500;
        }
        .calendar-day.active {
            background-color: var(--primary-color);
            color: white;
        }
        .calendar-day.today {
            border: 2px solid var(--warning-color);
        }
        .calendar-day.study-day {
            background-color: var(--success-color);
            color: white;
        }
    </style>
</head>
<body>
    <!-- Verificação de autenticação -->
    <script>
        // Este script será substituído pelo código de verificação do Firebase
    </script>

    <header class="header text-center">
        <div class="container">
            <h1>Plano de Estudos de Emanuel Ferreira</h1>
            <p class="lead">Transição para TI & Crescimento Pessoal</p>
            <!-- Botão de logout (será adicionado depois) -->
            <button id="logoutBtn" class="btn btn-sm btn-outline-light position-absolute top-0 end-0 mt-3 me-3" style="display: none;">Sair</button>
        </div>
    </header>

    <div class="container">
        <div class="row">
            <!-- Perfil Pessoal -->
            <div class="col-lg-4">
                <div class="card">
                    <div class="card-header">
                        Perfil Pessoal
                    </div>
                    <div class="card-body">
                        <div class="text-center mb-3">
                            <img src="https://via.placeholder.com/150" class="rounded-circle" alt="Foto de perfil">
                            <h4 class="mt-2">Emanuel Ferreira da Silva</h4>
                            <p class="text-muted">23 anos • Nascido em 08/03/2002</p>
                        </div>
                        <div class="mb-3">
                            <h5>Situação Atual</h5>
                            <ul class="list-group list-group-flush">
                                <li class="list-group-item">Comprador na Sabor Vitória Alimentação</li>
                                <li class="list-group-item">Salário atual: R$ 3.000,00</li>
                                <li class="list-group-item">Noivo, comprando apartamento na planta</li>
                            </ul>
                        </div>
                        <div id="objetivos-container">
                            <h5>Objetivos</h5>
                            <ul class="list-group list-group-flush" id="listaObjetivos">
                                <li class="list-group-item">Transição para carreira em TI até 2026</li>
                                <li class="list-group-item">Aumento salarial de pelo menos 30%</li>
                                <li class="list-group-item">Melhorar saúde física com exercícios regulares</li>
                            </ul>
                            <!-- Formulário para adicionar objetivos (será implementado com Firebase) -->
                            <div class="mt-3">
                                <div class="input-group">
                                    <input type="text" id="novoObjetivo" class="form-control" placeholder="Novo objetivo...">
                                    <button class="btn btn-primary" id="btnAdicionarObjetivo">Adicionar</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Calendário e Progresso -->
            <div class="col-lg-8">
                <div class="card">
                    <div class="card-header">
                        Calendário de Estudos
                    </div>
                    <div class="card-body">
                        <p>Acompanhe seus dias de estudo e mantenha a consistência</p>
                        <h5 id="mesAnoAtual">Abril 2025</h5>
                        <div class="d-flex justify-content-between mb-2">
                            <div>Dom</div>
                            <div>Seg</div>
                            <div>Ter</div>
                            <div>Qua</div>
                            <div>Qui</div>
                            <div>Sex</div>
                            <div>Sáb</div>
                        </div>
                        <div class="calendar-container" id="calendario">
                            <!-- Calendário será preenchido via JavaScript -->
                        </div>
                    </div>
                </div>

                <div class="card mt-4">
                    <div class="card-header">
                        Acompanhamento de Tarefas
                    </div>
                    <div class="card-body">
                        <p>Mantenha o controle das suas atividades de estudo</p>
                        <div class="progress mb-3">
                            <div class="progress-bar" id="progressoTarefas" role="progressbar" style="width: 0%;" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100">0%</div>
                        </div>
                        
                        <div id="listaTarefas">
                            <!-- As tarefas serão carregadas do Firebase aqui -->
                        </div>
                        
                        <form id="formNovaTarefa" class="mt-3">
                            <div class="input-group">
                                <input type="text" id="novaTarefa" class="form-control" placeholder="Nova tarefa...">
                                <input type="date" id="dataTarefa" class="form-control">
                                <select id="duracaoTarefa" class="form-select">
                                    <option value="15">15 min</option>
                                    <option value="30" selected>30 min</option>
                                    <option value="45">45 min</option>
                                    <option value="60">60 min</option>
                                </select>
                                <button class="btn btn-primary" type="submit">Adicionar</button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>

        <!-- Cronograma Semanal -->
        <div class="row mt-4">
            <div class="col-12">
                <div class="card">
                    <div class="card-header">
                        Seu Cronograma Semanal
                    </div>
                    <div class="card-body">
                        <p>Planejamento otimizado para sua rotina de trabalho</p>
                        <div class="table-responsive">
                            <table class="table table-bordered">
                                <thead>
                                    <tr>
                                        <th>Dia</th>
                                        <th>Manhã</th>
                                        <th>Trabalho</th>
                                        <th>Noite</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr>
                                        <td>Segunda</td>
                                        <td>7:00 - Saída para trabalho</td>
                                        <td>8:00 - 18:00</td>
                                        <td>
                                            19:30 - 20:00 Jantar<br>
                                            20:00 - 20:45 Estudo principal<br>
                                            20:45 - 21:00 Pausa<br>
                                            21:00 - 21:30 Revisão e prática<br>
                                            21:30 - 22:00 Exercícios físicos
                                        </td>
                                    </tr>
                                    <tr>
                                        <td>Terça</td>
                                        <td>7:00 - Saída para trabalho</td>
                                        <td>8:00 - 18:00</td>
                                        <td>
                                            19:30 - 20:00 Jantar<br>
                                            20:00 - 20:45 Estudo principal<br>
                                            20:45 - 21:00 Pausa<br>
                                            21:00 - 21:30 Revisão e prática<br>
                                            21:30 - 22:00 Exercícios físicos
                                        </td>
                                    </tr>
                                    <tr>
                                        <td>Quarta</td>
                                        <td>7:00 - Saída para trabalho</td>
                                        <td>8:00 - 18:00</td>
                                        <td>
                                            19:30 - 20:00 Jantar<br>
                                            20:00 - 20:45 Estudo principal<br>
                                            20:45 - 21:00 Pausa<br>
                                            21:00 - 21:30 Revisão e prática<br>
                                            21:30 - 22:00 Exercícios físicos
                                        </td>
                                    </tr>
                                    <tr>
                                        <td>Quinta</td>
                                        <td>7:00 - Saída para trabalho</td>
                                        <td>8:00 - 18:00</td>
                                        <td>
                                            19:30 - 20:00 Jantar<br>
                                            20:00 - 20:45 Estudo principal<br>
                                            20:45 - 21:00 Pausa<br>
                                            21:00 - 21:30 Revisão e prática<br>
                                            21:30 - 22:00 Exercícios físicos
                                        </td>
                                    </tr>
                                    <tr>
                                        <td>Sexta</td>
                                        <td>7:00 - Saída para trabalho</td>
                                        <td>8:00 - 17:00</td>
                                        <td>
                                            19:00 - 19:30 Descanso<br>
                                            19:30 - 20:30 Planejamento semanal<br>
                                            20:30 - 21:00 Exercícios físicos
                                        </td>
                                    </tr>
                                    <tr>
                                        <td>Sábado</td>
                                        <td>9:00 - 9:30 Exercícios físicos</td>
                                        <td>10:00 - 12:00 Estudo principal</td>
                                        <td>19:00 - 20:00 Projeto prático (opcional)</td>
                                    </tr>
                                    <tr>
                                        <td>Domingo</td>
                                        <td>9:00 - 9:30 Exercícios físicos</td>
                                        <td>10:00 - 11:30 Revisão semanal</td>
                                        <td>Preparação para a semana</td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer class="bg-dark text-white text-center py-4 mt-5">
        <div class="container">
            <p>Plano de Estudos de Emanuel Ferreira - Transição para TI & Crescimento Pessoal</p>
            <p>Iniciando em 21 de abril de 2025</p>
        </div>
    </footer>

    <!-- Firebase App SDK -->
    <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-app-compat.js"></script>
    <!-- Firebase Auth SDK -->
    <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-auth-compat.js"></script>
    <!-- Firebase Firestore SDK -->
    <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-firestore-compat.js"></script>

    <script>
        // Inicialização do Firebase (você preencherá com sua configuração)
        const firebaseConfig = {
            // VOCÊ PREENCHERÁ ISTO COM SUA CONFIGURAÇÃO DO FIREBASE
            apiKey: "",
            authDomain: "",
            projectId: "",
            storageBucket: "",
            messagingSenderId: "",
            appId: ""
        };

        // Inicializar Firebase
        firebase.initializeApp(firebaseConfig);
        
        // Referências para serviços do Firebase
        const auth = firebase.auth();
        const db = firebase.firestore();

        // Verificar autenticação
        document.addEventListener('DOMContentLoaded', function() {
            auth.onAuthStateChanged(function(user) {
                if (!user) {
                    // Usuário não está logado, redirecionar para página de login
                    // Descomente quando tiver criado a página de login
                    // window.location.href = 'login.html';
                } else {
                    // Mostrar botão de logout
                    document.getElementById('logoutBtn').style.display = 'block';
                    
                    // Carregar dados
                    carregarTarefas();
                    carregarObjetivos();
                }
            });
        });

        // Função para o botão de logout
        document.getElementById('logoutBtn').addEventListener('click', function() {
            auth.signOut().then(function() {
                // Redirecionar para login após logout
                // window.location.href = 'login.html';
            }).catch(function(error) {
                console.error('Erro ao fazer logout', error);
            });
        });

        // Renderizar calendário
        function renderizarCalendario() {
            const calendario = document.getElementById('calendario');
            calendario.innerHTML = '';
            
            const hoje = new Date();
            const mes = hoje.getMonth();
            const ano = hoje.getFullYear();
            
            // Atualizar título do mês/ano
            const meses = ['Janeiro', 'Fevereiro', 'Março', 'Abril', 'Maio', 'Junho', 'Julho', 'Agosto', 'Setembro', 'Outubro', 'Novembro', 'Dezembro'];
            document.getElementById('mesAnoAtual').textContent = `${meses[mes]} ${ano}`;
            
            // Primeiro dia do mês
            const primeiroDia = new Date(ano, mes, 1);
            // Último dia do mês
            const ultimoDia = new Date(ano, mes + 1, 0);
            
            // Dia da semana em que começa o mês (0 = Domingo, 6 = Sábado)
            const iniciaMes = primeiroDia.getDay();
            
            // Adicionar dias vazios até o primeiro dia do mês
            for (let i = 0; i < iniciaMes; i++) {
                const diaVazio = document.createElement('div');
                diaVazio.className = 'calendar-day empty';
                calendario.appendChild(diaVazio);
            }
            
            // Adicionar os dias do mês
            for (let i = 1; i <= ultimoDia.getDate(); i++) {
                const dia = document.createElement('div');
                dia.className = 'calendar-day';
                dia.textContent = i;
                
                // Verificar se é hoje
                if (i === hoje.getDate() && mes === hoje.getMonth() && ano === hoje.getFullYear()) {
                    dia.classList.add('today');
                }
                
                // Verificar se é um dia de estudo programado
                // Isso será integrado com o Firebase posteriormente
                
                calendario.appendChild(dia);
            }
        }

        // Funções para manipular tarefas (serão implementadas com Firebase)
        function carregarTarefas() {
            // Esta função será implementada quando o Firebase estiver configurado
            console.log("Função carregarTarefas - será implementada com Firebase");
        }

        function adicionarTarefa() {
            // Esta função será implementada quando o Firebase estiver configurado
            console.log("Função adicionarTarefa - será implementada com Firebase");
        }

        function atualizarStatusTarefa(tarefaId, concluida) {
            // Esta função será implementada quando o Firebase estiver configurado
            console.log("Função atualizarStatusTarefa - será implementada com Firebase");
        }

        function excluirTarefa(tarefaId) {
            // Esta função será implementada quando o Firebase estiver configurado
            console.log("Função excluirTarefa - será implementada com Firebase");
        }

        function atualizarProgresso() {
            // Esta função será implementada quando o Firebase estiver configurado
            console.log("Função atualizarProgresso - será implementada com Firebase");
        }

        // Funções para manipular objetivos
        function carregarObjetivos() {
            // Esta função será implementada quando o Firebase estiver configurado
            console.log("Função carregarObjetivos - será implementada com Firebase");
        }

        function adicionarObjetivo() {
            // Esta função será implementada quando o Firebase estiver configurado
            console.log("Função adicionarObjetivo - será implementada com Firebase");
        }

        // Eventos
        document.getElementById('formNovaTarefa').addEventListener('submit', function(e) {
            e.preventDefault();
            adicionarTarefa();
        });

        document.getElementById('btnAdicionarObjetivo').addEventListener('click', function() {
            adicionarObjetivo();
        });

        // Inicialização
        renderizarCalendario();
    </script>
</body>
</html>
