🚗 Frota Análise - Sistema de Gestão de Deslocamentos
O Frota Análise é uma ferramenta de automação desenvolvida para simplificar a auditoria de frotas veiculares. O sistema processa dados brutos de diferentes rastreadores (Cobli, Mzone e Carblock), identifica automaticamente deslocamentos realizados fora do horário comercial e gera relatórios estruturados prontos para envio por e-mail.
Desenvolvido por: Eng. Eric Jonas | 2026
🌟 Funcionalidades Principais
Análise Multi-Rastreador: Suporte nativo para três dos principais sistemas de rastreamento do mercado.
Filtro Inteligente de Horário: Identifica automaticamente viagens fora do padrão:
Segunda a Sexta: Antes das 08:30 e após as 18:00.
Finais de Semana: Auditoria de 100% dos deslocamentos.
Gerador de Relatórios de E-mail: Formata os dados no padrão corporativo, incluindo assunto e corpo detalhado com quilometragem e tempos acumulados.
Banco de Dados em Nuvem: Integração com Supabase para armazenamento histórico de todas as análises realizadas.
Interface Responsiva: Design moderno com suporte a Modo Escuro (Dark Mode).
Gestão de Histórico: Visualize análises passadas, copie relatórios salvos ou exclua registros indesejados.
🛠️ Como o Sistema Processa cada Rastreador
1. Mzone (Web - Trip Data)
O sistema realiza uma varredura em blocos de texto "Trip Data" copiados diretamente da interface web do Mzone. Ele identifica cada viagem individual, calcula a duração e a distância, validando o horário de cada trecho para compor o relatório analítico.
2. Cobli (Excel)
Otimizado para dados copiados de planilhas. O sistema lê as colunas de data, motorista, quilometragem e horários. Possui um Filtro de Placa Alvo: você pode colar uma planilha com diversos veículos e o sistema extrairá apenas os dados do veículo selecionado, somando o total de KM e tempo.
3. Carblock (CSV/Log de Posições)
Diferente dos outros, o Carblock foca em logs de ignição. O sistema analisa os estados de Ignição Ligada/Desligada, identifica o endereço de origem (onde o carro ligou) e o de destino (onde desligou) para cada saída fora do horário, calculando o tempo de exposição do veículo.
🚀 Tecnologias Utilizadas
Frontend: HTML5, CSS3 (Variáveis nativas para temas) e JavaScript Vanilla (ES6+).
Backend/Database: Supabase (PostgreSQL + PostgREST API).
Hospedagem: Otimizado para GitHub Pages.
📋 Pré-requisitos para Instalação
Como o sistema é um modelo Single Page Application (SPA) simples, não requer instalação de dependências.
Salve o arquivo index.html.
Certifique-se de que a imagem logo.png (sua marca) esteja na mesma pasta.
Configure sua URL e ANON_KEY do Supabase no script para conectar ao seu banco de dados privado.
📧 Estrutura do Relatório Gerado
O sistema entrega o seguinte formato pronto para cópia:
Assunto: Relatório de Movimentação fora de padrão [Técnico], [Placa], [Data], [Filial], [Rastreador]
Corpo:
Detalhamento de cada trecho (Hora inicial, final e KM).
Somatória total de tempo em movimento.
Somatória total de KM percorrido.
Campo de justificativa preenchido pelo gestor.
🛡️ Licença e Créditos
Este sistema foi desenvolvido de forma personalizada pelo Eng. Eric Jonas.
📧 erj.informatica@gmail.com