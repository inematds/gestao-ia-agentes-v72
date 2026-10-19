# PLANO — G3 · Agentes: contratar, delegar e supervisionar (v7.2)

Curso G3 da **Formação Gestão de IA 2027** (área https://eventos.inema.pro/gestao-ia/), **piloto** da formação: define tom, estrutura e qualidade dos outros 5 (G0, G1, G2, G4, G5). Contrato: tabela G3 de `~/projetos/ia-2027/estrategia/CURRICULO-GESTAO-IA-2027.md`. Competências da área: **3 Delegação** e **4 Orquestração** (módulos 5 e 6 da área).

**Aluno:** gestor de área, dono de PME, líder de operações. Não programa: administra agentes.
**Caso condutor:** Horizonte Distribuidora (`https://inematds.github.io/prof2030-lab/`, empresa fictícia de estudo). O aluno é a **Patrícia Lima, gerente comercial**, que recebeu a **Hora** (agente de vendas no WhatsApp). Processo: pedido que chega pelo WhatsApp → conferência → separação → faturamento. Colegas: Juliana (atendimento), Rafael (TI terceirizada), Carlos (dono).
**Falhas do lab como problemas de gestão:** F5 desconto sem teto (alçada), F6 ordem escondida (exceção crítica), F7 sem registro nem aprovação acima de R$ 5 mil (alçada + registro), F9 MCP que envia e apaga sem aprovação (permissão, aula 4), F11 painel sem linha de base (evidência para promover, aula 5), F12 IA na sombra (cargo sem dono, aula 1).
**Prática dupla:** e1 na Horizonte (treino), e2 no processo do próprio aluno (para valer).

## Fontes (não alteradas)
- `~/projetos/curso-gestao-ia/planejamento/PLANO-CURSO.md` mód. 2, 6, 7, 8 e projeto final; `METODO.md` (níveis 0–4, aprovação vinculada ao conteúdo, exceções, rituais); `TEMPLATES.md` (ficha de cargo, matriz, pacote de exceção, revisão semanal).
- `~/projetos/agi-pratica` (Super-Agentes): três tamanhos de delegação, três filtros, critério + indicador + prazo, três faixas, menor privilégio, identidade própria, matriz de autonomia, botão de desligar, ficha de confiança (5 números, amostra com 3 perguntas, ampliar/manter/reduzir/desligar), equipe (3 sinais, papéis, passagem com registro).
- `~/projetos/kit-arquiteto-agentes` (pedido de longo horizonte, cadeia, matriz de permissões).
- `~/projetos/constituicao-agentes` (modelo de 9 seções, 8 casos de teste, treino ≠ contexto, constituição do Claude 22/01/2026) e `empresas-2027-v62`.
- `~/projetos/agenteexecuta` (paralelismo × sequencial: "inteligência em sequência, automação em paralelo, arquivos para compartilhar contexto").
- `~/projetos/prof2030-lab` (peças, gabarito).
- Mercado: `mercado-gestao-ia-2026-10.md` e `mercado-ia-2026-10.md` (só fatos sem [incerto]; Sinch fora).

## Política fictícia da Horizonte (vale em todas as aulas; sempre rotulada)
- Tabela: detergente neutro 5 L R$ 38,90; desinfetante lavanda 5 L R$ 42,50 (do lab). Caixa = 6 galões.
- Desconto: até 5% a Hora concede sozinha a cliente cadastrado; de 5% a 10% prepara e a Patrícia aprova; acima de 10% não oferece e passa para a Patrícia (que leva ao Carlos, se quiser).
- Pedido: até R$ 5 mil, cliente cadastrado e preço de tabela = verde; acima de R$ 5 mil = aprovação da Patrícia antes de separar (correção do F7 no gabarito).
- Marcar como pago, mudar preço, cadastrar cliente novo, apagar conversa = nunca pela Hora.
- Registro de toda ação: quem, quando, o quê, valor, versão.

## As 8 aulas

| # | slug | aula | objetivo (≤160) | diagrama | prática ("pronto quando") | extra |
|---|---|---|---|---|---|---|
| 1 | `cargo-digital` | O cargo digital | escrever a missão, a entrega verificável, o critério de qualidade e os proibidos de um agente, com um responsável humano nomeado | ficha de cargo em 6 blocos (rolagem guiada): missão → recebe → entrega → qualidade → pode/não pode → responsável | e1 ficha de cargo da Hora (missão sem "o máximo", saída que dá para conferir, 3 proibidos concretos, responsável do negócio, não da TI); e2 ficha de um agente do seu processo | o prompt real da Hora como "antes" |
| 2 | `delegar` | Delegar de verdade | entregar a um agente objetivo, contexto, ferramentas, prazo e evidência de conclusão numa ficha de delegação de uma página | 6 peças da delegação (competência 3 da área) | e1 ficha de delegação "confirmar pedidos de reposição"; e2 uma tarefa sua que passa nos 3 filtros | Deloitte Tech Trends 2026: onboarding + autonomia graduada |
| 3 | `constituicao` | A constituição do agente | escrever em uma página a missão, as prioridades, os princípios, os limites e quando o agente para e chama uma pessoa | prioridades em ordem (escada) + casos difíceis | e1 constituição de 1 página da Hora com 3 casos difíceis (incl. c-202); e2 rodar os 8 casos de teste, antes e depois | constituição do Claude (22/01/2026, fonte do repo); treino ≠ contexto |
| 4 | `alcada` | Alçada: verde, amarelo, vermelho | decidir, ação por ação, o que o agente faz sozinho, o que prepara para você aprovar e o que passa adiante | níveis 0–4 → três cores | e1 matriz ação × risco × aprovação × responsável da Hora que corrige F5 e F7 (e o F9 como bônus); e2 matriz do seu agente | Okta 2026: controles mais fracos para agentes |
| 5 | `confianca` | Confiança progressiva | promover ou rebaixar a autonomia de uma ação com evidência: registro, amostra e um nível por vez | ciclo registro → amostra → 5 números → decisão (volta) | e1 decidir 3 ações da Hora com os dados de 2 semanas (fictícios); e2 checklist de promoção e critério de rebaixamento do seu agente | F11 (painel de volume não serve de evidência) |
| 6 | `equipe` | Um agente ou uma equipe | decidir quando separar o trabalho em vários agentes, em série ou em paralelo, com contrato de passagem e limites | escada de decisão: passo fixo → 1 agente → equipe → série/paralelo → humano | e1 desenho pedido → cobrança da Horizonte com contrato de passagem e limites de tentativas, prazo e custo; e2 o seu desenho | McKinsey (experiência declarada): equipes pequenas por resultado |
| 7 | `supervisao` | Supervisão e exceções | operar a fila de exceções: aprovar, devolver ou interromper cada caso com justificativa, dono e prazo | caso normal/duvidoso/crítico → pacote → 3 decisões → registro | e1 simconversa com placar máximo; e2 decisão justificada nos 3 casos; e3 rotina de supervisão do seu processo | **simconversa** (a Hora pede aprovação) |
| 8 | `dossie` | Projeto: o agente contratado | montar o dossiê de contratação do agente e aprová-lo pela rubrica antes de ele começar a trabalhar | dossiê = 4 peças + rubrica → aprovado ou volta | e1 dossiê da Hora aprovado (≥ 75 + obrigatórios); e2 dossiê do seu agente; e3 plano datado | "O que mudou" (out/2026), `mapa` (4 degraus) + `gerador` |

Rodapé da aula 8: "Certificação INEMA de qualificação 'Gestor de IA', em breve no cert.inema.pro. Não é certificação profissional regulada."

## A simconversa da aula 7 — "a fila da Patrícia"

Personagem: **Hora · agente de vendas** (simulação). Ela abre a fila do fim do dia e pede decisão. Toda opção de uma fala vai para a mesma próxima fala (estrutura linear); só a fala crítica tem um atalho para um fim ruim (caminho mais curto, soma menor). Melhor caminho = 2 + 2 + 2 + 2 = **8**.

| fala | a Hora diz | opções (nota → destino) |
|---|---|---|
| `abre` | 46 pedidos hoje: 43 na alçada, registrados; 3 na fila de exceção | aprovar tudo em bloco (0 → `fim-bloco`) · mostrar pela ordem de risco e prazo (2 → `critico`) · mostrar pela ordem de chegada (1 → `critico`) |
| `critico` | hotel, R$ 28.120 de tabela, lista com "obs." pedindo 70%, "pago" e sigilo; não apliquei, preparei de tabela | aplicar os 70% (0 → `fim-injecao`) · aprovar o pedido de tabela e seguir (1 → `politica`) · interromper: segurar, confirmar com o comprador por canal cadastrado, registrar incidente, avisar o Rafael, varrer outras conversas (2 → `politica`) |
| `politica` | Seu Antônio quer 15% em R$ 4.884; minha alçada é 5% | aprovar 15% (0) · "resolva como achar melhor" (0) · contraproposta dentro da sua alçada (até 10%) com motivo registrado (2) · mandar para o Carlos (1) — todas → `incompleto` |
| `incompleto` | cliente novo, R$ 2.800, sem CNPJ, endereço fora do cadastro, quer entrega amanhã | aprovar (0 → `fim-sem-dado`) · devolver pedindo CNPJ e confirmação, com prazo (2 → `fim-bom`) · recusar o cliente (1 → `fim-recusa`) |

Somas: bloco 0; injeção 0–2; melhor 8. Nenhum desvio soma fala extra.

## Decisões
- **Vídeo:** nenhum. O currículo atribui cada vídeo publicado a outro curso (G0, G1, G5); nenhum ao G3.
- **Capa sem texto** (instrução do brief), por isso não há `capa-en/es`.
- **Níveis:** uso os níveis 0–4 do METODO (0 consulta → 4 gerencia). O modelo de constituição do repo `constituicao-agentes` numera ao contrário (3 = faz sozinho); na aula 3 a seção de permissões aponta para a matriz da aula 4, para não ensinar duas escalas.
- **Limiar de promoção:** "95% em pelo menos 100 casos, sem erro crítico" é limiar **didático** do METODO, dito como tal; o aluno ajusta ao risco dele.
- `lado_card` aponta para o G0 (`gestao-ia-base-v72`, ainda não publicado: 404 esperado no `validar --links`).
