# Documentação do Projeto: Demos Layout Coliv

Este documento apresenta uma análise detalhada da estrutura do projeto "Coliv", um protótipo de alta fidelidade para uma plataforma de co-living e moradias compartilhadas. O projeto possui um design system chamado "The Curated Sanctuary", focado em um estilo editorial de alto padrão (High-End Editorial), cores Navy e Mint, além de farto uso de componentes minimalistas e com glassmorphism.

## Estrutura do Projeto (Camadas)

A arquitetura do projeto é dividida basicamente em diretórios, onde cada pasta dentro de `src` representa uma tela ou um módulo específico da aplicação, contendo seu respectivo arquivo HTML (que também inclui o CSS via Tailwind).

*   **`src/`**: Diretório principal que contém o código das telas.
    *   **Pastas de Telas**: Cada tela (como `login_coliv`, `cadastro_coliv`, etc.) tem sua própria pasta contendo o código-fonte (`code.html`) e uma imagem de demonstração/preview (`screen.png`).
    *   **`habitat_modern/`**: Contém o arquivo `DESIGN.md`, que funciona como o *Design System* oficial do projeto. Ele estabelece as regras visuais, tipográficas (Plus Jakarta Sans e Manrope) e hierarquia de componentes.
*   **`documentacao/`**: Pasta reservada para arquivos e descrições técnicas gerais do projeto.

---

## Telas e Campos Disponíveis

Abaixo está a explicação detalhada de cada tela desenvolvida e os campos/elementos presentes em cada uma delas:

### 1. Boas Vindas (boas_vindas_coliv)
**Explicação**: A *Landing Page* (Página Inicial) do Coliv. Seu objetivo é apresentar o conceito da plataforma ("Sua casa, sua tribo"), gerar impacto visual e direcionar o usuário para a criação de conta ou login.
**Campos e Elementos**:
*   **Header (Cabeçalho)**: Logo "Coliv", Links de navegação ("Sobre nós", "Comunidades") e botão "ENTRAR".
*   **Hero Section**: Título de impacto, subtítulo explicativo.
*   **Botões de Ação (CTAs)**: "CRIAR CONTA" e "ENTRAR".
*   **Social Proof (Prova Social)**: Seção com fotos de avatares e o texto "+500 pessoas já vivem no Coliv".
*   **Card de Demonstração (Imagem)**: Uma unidade de exemplo (Ex: "Unidade Vila Madalena") mostrando a nota de avaliação (ex: 4.9) e a quantidade de *reviews*.

### 2. Login (login_coliv)
**Explicação**: Tela para os usuários que já possuem conta na plataforma poderem acessar o sistema.
**Campos e Elementos**:
*   **Campo "E-mail"**: Entrada de texto para o endereço de e-mail.
*   **Campo "Senha"**: Entrada de texto oculta, com ícone lateral (toggle) para exibir/ocultar a senha.
*   **Link de Recuperação**: Link "Esqueci minha senha".
*   **Botão de Ação**: Botão "Entrar na conta".
*   **Login Social**: Botões para login via contas do Google ou Apple (iOS).
*   **Link de Cadastro**: Direcionamento "Criar conta" para usuários novos.

### 3. Cadastro (cadastro_coliv)
**Explicação**: Onde ocorre a criação de uma nova conta, solicitando dados básicos e identificando o perfil do usuário.
**Campos e Elementos**:
*   **Seleção de Perfil ("Quem é você?")**: Dois botões do tipo rádio em formato de cartão: "Colega" (buscando lugar) ou "Anfitrião" (tem um lugar disponível).
*   **Campo "Nome Completo"**: Entrada de texto.
*   **Campo "CPF"**: Entrada de texto (possui um ícone de "check" e mensagem verde indicando validação do documento).
*   **Campo "E-mail"**: Entrada de texto padrão para e-mail.
*   **Campo "Senha"**: Entrada de texto (mínimo de 8 caracteres) com toggle de visibilidade.
*   **Botão de Ação**: Botão "Continuar".
*   **Rodapé Legal**: Links obrigatórios para "Termos de Uso" e "Política de Privacidade".

### 4. Buscar Lares (buscar_lares_coliv)
**Explicação**: Esta tela é o feed principal para o perfil "Colega", onde são listados os imóveis compatíveis com o usuário baseando-se no algoritmo do Coliv.
**Campos e Elementos**:
*   **Cabeçalho**: Logo, ícone de Pesquisa (lupa) e Foto de Perfil.
*   **Lista de Imóveis (Cards)**:
    *   **Imagem do Imóvel**.
    *   **Tag de Match**: Porcentagem de compatibilidade (Ex: "98% Match").
    *   **Preço**: Valor mensal do aluguel (Ex: R$ 2.450/mês).
    *   **Título**: Nome do imóvel/quarto (Ex: "Loft Pinheiros Design").
    *   **Distância**: Indicador de localização (Ex: "1.2km do seu trabalho").
    *   **Comodidades (Tags)**: Atributos do local (Ex: Pet-friendly, Silencioso, Energia Solar).
    *   **Botão "Ver Detalhes"**.
*   **Barra de Navegação Inferior**: Abas de Início, Chat, Gestão e Perfil.
*   **Botão Flutuante (FAB)**: Botão de ação "+" para novas requisições ou filtros rápidos.

### 5. Cadastrar Imóvel (cadastrar_im_vel_coliv)
**Explicação**: O formulário para que um "Anfitrião" adicione um novo imóvel na plataforma Coliv. Focado em uma experiência guiada.
**Campos e Elementos**:
*   **Galeria de Estilo**: Área de envio (upload) de 1 a 10 fotos, com suporte a arrastar e soltar (drag & drop), permitindo selecionar a foto principal de capa.
*   **Manifesto do Espaço**: Área de texto livre (textarea) para o anfitrião descrever a alma do imóvel e regras da casa.
*   **Investimento Mensal**: Campo numérico para definir o valor do aluguel em Reais (R$).
*   **Tipo de Vaga**: Menu de seleção (Dropdown) contendo opções como Quarto Privativo, Quarto Compartilhado, Suíte Master ou Studio Completo.
*   **Localização**: Campo de busca para o endereço ou CEP, acompanhado por um componente visual de mapa.
*   **Comodidades Premium**: Conjunto de botões selecionáveis (Ex: Wi-Fi 5G, Academia, Coworking, Piscina, Lavanderia, Pet Friendly, Limpeza Semanal).
*   **Card de Confiança**: Banner informando que o Anfitrião é "Verificado".
*   **Barra Inferior Fixa**: Exibe o "Status do Anúncio" e contém o botão primário "Publicar Anúncio".

### 6. Dashboard do Anfitrião (dashboard_anfitri_o_coliv)
**Explicação**: É o painel de controle do dono do imóvel para acompanhar o desempenho do seu anúncio e os interessados.
**Campos e Elementos**:
*   **Card do Imóvel**: Exibe o status (Ativo), o título do anúncio e as métricas de engajamento: "Interessados", "Visitas" e "Matches".
*   **Próxima Visita**: Widget contendo o nome e horário do próximo agendamento, além do botão "Ver Agenda Completa".
*   **Colegas Compatíveis (Matches)**: Lista de perfis compatíveis indicados pelo "Algoritmo Coliv".
    *   Cada Card de perfil possui: Foto, % de Match, Nome, Idade, Profissão, uma breve Bio/Citação e os botões "Recusar/Fechar" e "Aceitar (Match)".
*   **Filtros Avançados**: Botão no cabeçalho da lista para refinar o perfil de buscas.

### 7. Gestão da Moradia (gest_o_da_moradia_coliv)
**Explicação**: Funciona como a "Central do Morador". Tela de uso contínuo focada em administração financeira e convivência de uma república/co-living existente.
**Campos e Elementos**:
*   **Santuário (Header)**: Imagem do imóvel, nome ("Vila Madalena Collective") e badge indicando "Contrato Ativo".
*   **Resumo do Contrato**:
    *   **Próximo Vencimento**: Valor do aluguel (R$) e barra de progresso dos dias restantes.
    *   **Término**: Data (Mês e Ano) de fim do contrato.
    *   **Seguro**: Status da garantia do aluguel.
*   **Moradores**: Lista visual em formato carrossel mostrando os avatares dos colegas de quarto e um botão "+" para adicionar.
*   **Despesas do Grupo**:
    *   **Pendência Total e Sua Parte**: Valores (R$) referentes à dívida atual.
    *   **Histórico Recente**: Lista de contas e boletos (ex: Energia Elétrica, Limpeza, Internet), informando o valor, o vencimento e os status (Dividido, Finalizado, Aguardando).
    *   **Botão Adicionar**: Para cadastrar novas despesas compartilhadas.

### 8. Preferências do Anfitrião (prefer_ncias_do_anfitri_o)
**Explicação**: Tela onde o dono da casa personaliza o perfil ideal da pessoa com quem deseja dividir o teto.
**Campos e Elementos**:
*   **Perfil Demográfico**:
    *   **Gênero Preferencial**: Botões de seleção única (Qualquer, Feminino, Masculino).
    *   **Faixa Etária**: Slider (barra de controle) de dois pontos para definir o intervalo de idades desejado (ex: 22 a 32 anos).
*   **Animais**: Três opções radiais (Sim, Apenas pequenos, Não aceito).
*   **Política de Limpeza**: Escolha interativa entre: Escala Semanal, Serviço Profissional Contratado ou Independente.
*   **Política de Visitas**: Conjunto de caixas de seleção (Checkboxes) para: "Permitido visitas diurnas", "Pernoite permitido", "Final de semana livre".
*   **Regras Adicionais**: Área de texto longa (Textarea) para redigir obrigações e proibições específicas da casa.
*   **Botão de Ação**: "Salvar Preferências".

### 9. Preferências do Colega (prefer_ncias_do_colega)
**Explicação**: Formulário equivalente ao do anfitrião, porém preenchido pelo morador que está buscando vaga.
**Campos e Elementos**:
*   **Faixa de Investimento**: Slider duplo para definir o valor mínimo e máximo que deseja pagar mensalmente (ex: R$ 2.400 - R$ 4.500).
*   **Localização**: Campo de texto livre para digitar o bairro/cidade (ex: Pinheiros, SP).
*   **Ritmo de Sono**: Seleção de botões (Madrugador, Noturno, Equilibrado).
*   **Sociabilidade**: Três opções de estilo de convivência (Amo jantares coletivos, Equilíbrio é tudo, Prefiro meu espaço).
*   **Limpeza**: Opções sobre organização (Minimalista & Impecável, Organizado na medida, Caos criativo).
*   **Animais**: Chave tipo Toggle Switch (Liga/Desliga) indicando se tem ou aceita pets.
*   **Hábitos de Trabalho**: Seleção de formato de trabalho (Home Office, Híbrido, Trabalho Externo).
*   **Botão de Ação**: "Salvar Preferências".

### 10. Bate-Papo / Chat (bate_papo_coliv)
**Explicação**: Tela de mensagens instantâneas habilitada somente após o sistema identificar e aprovar um "Match" mútuo entre anfitrião e candidato.
**Campos e Elementos**:
*   **Cabeçalho da Conversa**: Foto, Nome da pessoa e status de perfil (ex: Anfitrião Verificado).
*   **Banner de Ação**: Destaque topo ("Novo Match com Lucas!") e um botão "Enviar Convite de Moradia".
*   **Área de Conversa (Canvas)**:
    *   Linhas de divisão temporais (ex: "Hoje, 14:32").
    *   Mensagens automáticas do sistema explicando o match.
    *   Balões de mensagens do remetente e do destinatário, contendo horário e símbolo de "lido" (ticks).
    *   Feedback de digitação ("Ricardo está digitando").
*   **Dock de Digitação (Rodapé)**:
    *   Botão "+": Para envio de mídias ou anexos.
    *   **Campo de Texto**: Área central para digitar a mensagem.
    *   **Botão Enviar**: Ícone de avião de papel para submeter a mensagem.
