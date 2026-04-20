# Documentação de Interface e API Visual: Demos Layout Coliv

**Versão**: 1.0.0
**Projeto**: Coliv (The Curated Sanctuary)
**Descrição**: Especificação dos módulos e interfaces (telas) de alta fidelidade para a plataforma de co-living.

---

## 1. Visão Geral do Sistema
O sistema "Coliv" é dividido estruturalmente em módulos front-end (telas) baseados no Design System *The Curated Sanctuary*.
- **Cores Principais**: Navy e Mint.
- **Estilo**: High-End Editorial, Glassmorphism.
- **Tipografia**: Plus Jakarta Sans (Títulos), Manrope (Corpo).

---

## 2. Especificação dos Endpoints Visuais (Telas)

### 2.1. Tela de Boas Vindas
- **Caminho do Recurso**: `/src/boas_vindas_coliv`
- **Ação Principal**: Apresentação e Captação de Leads.
- **Descrição**: Landing Page focada em demonstrar o conceito "Sua casa, sua tribo".

**Parâmetros de Interface (Campos)**
| Elemento | Tipo | Descrição |
| --- | --- | --- |
| Header | Navegação | Logo Coliv, Links (Sobre nós, Comunidades) e Botão ENTRAR. |
| CTAs | Botões | Ações "CRIAR CONTA" e "ENTRAR". |
| Social Proof | Componente | Avatares de moradores e contador "+500 pessoas". |
| Card de Demonstração | Componente | Imagem de unidade (ex: Vila Madalena) com rating (4.9) e reviews. |

---

### 2.2. Login
- **Caminho do Recurso**: `/src/login_coliv`
- **Ação Principal**: Autenticação de Usuário.
- **Descrição**: Ponto de acesso à plataforma para usuários registrados.

**Parâmetros de Interface (Campos)**
| Elemento | Tipo | Descrição |
| --- | --- | --- |
| E-mail | Input Text | Campo para o e-mail do usuário. |
| Senha | Input Password | Campo de senha com função de alternar visibilidade (Toggle). |
| Esqueci minha senha | Link | Redirecionamento para fluxo de recuperação. |
| Entrar na conta | Botão | Ação de submissão (Submit). |
| Social Login | Botões | Autenticação via Google e Apple. |

---

### 2.3. Cadastro
- **Caminho do Recurso**: `/src/cadastro_coliv`
- **Ação Principal**: Criação de Nova Conta.
- **Descrição**: Formulário inicial para cadastrar anfitriões ou colegas.

**Parâmetros de Interface (Campos)**
| Elemento | Tipo | Descrição |
| --- | --- | --- |
| Quem é você? | Input Radio | Cartões de seleção de perfil: "Colega" ou "Anfitrião". |
| Nome Completo | Input Text | Identificação do usuário. |
| CPF | Input Text | Com validador em tempo real (ícone verde de check). |
| E-mail | Input Email | Endereço de e-mail de cadastro. |
| Senha | Input Password | Exigência mínima de 8 caracteres. |
| Continuar | Botão | Confirmação dos dados de cadastro. |

---

### 2.4. Buscar Lares
- **Caminho do Recurso**: `/src/buscar_lares_coliv`
- **Ação Principal**: Feed e Pesquisa de Imóveis.
- **Descrição**: Interface para usuários "Colega" explorarem lares compatíveis via algoritmo de Match.

**Parâmetros de Interface (Campos)**
| Elemento | Tipo | Descrição |
| --- | --- | --- |
| Barra de Pesquisa | Input Search | Busca avançada de imóveis. |
| Card de Imóvel | Componente | Contém: Imagem, Tag "% Match", Preço (R$), Título, Distância. |
| Tags de Comodidade | Label | Indicações (ex: Pet-friendly, Energia Solar). |
| Ver Detalhes | Botão | Ação para abrir os detalhes do imóvel. |
| Bottom Nav | Navegação | Abas: Início, Chat, Gestão, Perfil. |

---

### 2.5. Cadastrar Imóvel
- **Caminho do Recurso**: `/src/cadastrar_im_vel_coliv`
- **Ação Principal**: Criação de Anúncio.
- **Descrição**: Fluxo de adição de um novo imóvel pelo "Anfitrião".

**Parâmetros de Interface (Campos)**
| Elemento | Tipo | Descrição |
| --- | --- | --- |
| Galeria de Estilo | Upload | Upload com *drag & drop* (1 a 10 fotos). |
| Manifesto do Espaço | Textarea | Descrição do ambiente e regras da casa. |
| Investimento Mensal | Input Number | Valor mensal da locação (em Reais). |
| Tipo de Vaga | Select (Dropdown) | Opções: Quarto Privativo, Suíte Master, etc. |
| Localização | Input Search | Campo conectado a componente de mapa geográfico. |
| Comodidades Premium | Toggle Buttons | Wi-Fi 5G, Academia, Coworking, etc. |
| Publicar Anúncio | Botão Primário | Efetiva a publicação do imóvel. |

---

### 2.6. Dashboard do Anfitrião
- **Caminho do Recurso**: `/src/dashboard_anfitri_o_coliv`
- **Ação Principal**: Gerenciamento de Anúncios e Matches.
- **Descrição**: Visão gerencial do proprietário.

**Parâmetros de Interface (Campos)**
| Elemento | Tipo | Descrição |
| --- | --- | --- |
| Card do Imóvel | Componente | Métricas: "Interessados", "Visitas" e "Matches". |
| Próxima Visita | Widget | Informação da agenda e botão de visualização detalhada. |
| Colegas Compatíveis | Lista (Grid) | Cards dos usuários "Matches" (Imagem, Nome, Bio, % Match). |
| Aceitar/Recusar | Botões | Ações de conversão (Match/Discard) no card de candidato. |

---

### 2.7. Gestão da Moradia
- **Caminho do Recurso**: `/src/gest_o_da_moradia_coliv`
- **Ação Principal**: Administração Financeira e Rotina do Imóvel.
- **Descrição**: Central do Morador após consolidação do contrato.

**Parâmetros de Interface (Campos)**
| Elemento | Tipo | Descrição |
| --- | --- | --- |
| Resumo do Contrato | Componente | Próximo Vencimento (R$), dias restantes e status do Seguro. |
| Moradores | Carrossel | Exibição de avatares com opção de adição (+). |
| Pendência Total | Indicador | Valor (R$) da dívida global e a fatia do usuário ("Sua parte"). |
| Histórico Recente | Lista | Contas compartilhadas (Energia, Internet) com status. |
| Adicionar Despesa | Botão | Inserção de novos boletos na cota comum. |

---

### 2.8. Preferências do Anfitrião
- **Caminho do Recurso**: `/src/prefer_ncias_do_anfitri_o`
- **Ação Principal**: Configuração de Regras de Match (Lado Anfitrião).
- **Descrição**: Definição do perfil desejado de colega.

**Parâmetros de Interface (Campos)**
| Elemento | Tipo | Descrição |
| --- | --- | --- |
| Gênero Preferencial | Radio Buttons | "Qualquer", "Feminino", "Masculino". |
| Faixa Etária | Range Slider | Controle deslizante duplo para idade (ex: 22 a 32 anos). |
| Animais | Radio Buttons | Aceitação de pets (Sim, Apenas pequenos, Não). |
| Política de Limpeza | Selector | Tipos de limpeza (Escala, Profissional, Independente). |
| Política de Visitas | Checkboxes | "Visitas diurnas", "Pernoite", "FDS livre". |
| Regras Adicionais | Textarea | Espaço aberto para restrições específicas. |

---

### 2.9. Preferências do Colega
- **Caminho do Recurso**: `/src/prefer_ncias_do_colega`
- **Ação Principal**: Configuração de Regras de Match (Lado Colega).
- **Descrição**: Definição de hábitos e limites financeiros do buscador.

**Parâmetros de Interface (Campos)**
| Elemento | Tipo | Descrição |
| --- | --- | --- |
| Faixa de Investimento | Range Slider | Controle duplo para orçamento mínimo e máximo (R$). |
| Localização | Input Text | Preferência de bairros ou regiões. |
| Ritmo de Sono | Botões | "Madrugador", "Noturno", "Equilibrado". |
| Sociabilidade | Checkboxes | Nível de interação (Jantares coletivos, Equilíbrio, Meu espaço). |
| Limpeza | Checkboxes | Organização (Minimalista, Organizado, Caos criativo). |
| Animais | Toggle Switch | Indicação se possui pets. |
| Hábitos de Trabalho | Botões | "Home Office", "Híbrido", "Externo". |

---

### 2.10. Bate-Papo (Chat)
- **Caminho do Recurso**: `/src/bate_papo_coliv`
- **Ação Principal**: Troca de Mensagens (Messaging).
- **Descrição**: Interface de comunicação direta aberta apenas em caso de *Match*.

**Parâmetros de Interface (Campos)**
| Elemento | Tipo | Descrição |
| --- | --- | --- |
| Cabeçalho | Identificador | Avatar, Nome e Tag de Status do outro usuário. |
| Banner de Match | Notificação | Alerta visual do Match e botão "Enviar Convite de Moradia". |
| Área do Chat | Canvas | Balões de mensagem (Timestamp, Sistema, Leitura/Ticks). |
| Campo de Texto | Input | Área de digitação de novas mensagens. |
| Anexos (+) | Botão | Upload de imagens e arquivos. |
| Enviar | Botão | Submissão de nova mensagem. |
