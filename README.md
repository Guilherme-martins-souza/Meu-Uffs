# Guia do Calouro UFFS

Plataforma web de gestão individual e afiliação estudantil para ingressantes.

- **Curso de referência:** Ciência da Computação — Universidade Federal da Fronteira Sul (UFFS), Campus Chapecó
- **Público-alvo:** estudantes ingressantes (calouros) do ensino superior
- **Status:** Sprint 1 — conceito do projeto (ainda sem código)

## 1. Visão geral

Aplicação web simplificada e interativa para a gestão da rotina acadêmica individual e o letramento institucional de calouros. Os sistemas institucionais oficiais focam no registro burocrático de matrículas e históricos. Este sistema atua como assistente pessoal e guia de sobrevivência universitária.

O software:

- traduz normas acadêmicas densas em interfaces visuais dinâmicas;
- automatiza o cálculo preditivo de notas conforme a metodologia de cada professor;
- centraliza datas de avaliações de forma colaborativa;
- reúne informações práticas do cotidiano do campus.

## 2. Justificativa e embasamento

O ingresso na universidade pública, especialmente em Exatas e Computação, tem uma curva de adaptação íngreme. O problema não está só na complexidade técnica das disciplinas, mas na dificuldade de entender o funcionamento burocrático, logístico e avaliativo da instituição. Três pilares sustentam a proposta:

### I. Evasão no primeiro ano em Computação (INEP/MEC)

**Fonte:** INEP — Censo da Educação Superior e Indicadores de Trajetória da Educação Superior (Ministério da Educação).

Os relatórios longitudinais do INEP mostram que a área de Computação e TIC está historicamente entre as maiores taxas de evasão acumulada do país, frequentemente acima de 50% ao longo do fluxo do curso. O pico de abandono ocorre no 1º ano (dois primeiros semestres), por causa do choque de transição entre o ensino médio (tutelado) e o superior (que exige autogestão de notas, prazos e pré-requisitos).

### II. Afiliação estudantil e desconhecimento das regras (Coulon)

**Fonte:** COULON, Alain. O ofício de estudante: a entrada na vida universitária. *Educação e Pesquisa*, São Paulo (USP), v. 43, n. 4, p. 1239-1250, 2017 (SciELO).

Segundo Coulon, o sucesso do calouro depende da **Afiliação Institucional**. Muitos alunos reprovam ou evadem não por falta de capacidade cognitiva, mas por não dominarem os "códigos invisíveis" e as regras práticas da universidade: interpretar planos de ensino, gerenciar médias parciais, entender travas de grade curricular e navegar pelo espaço físico. Um sistema que explicita esses "macetes" regimentais acelera a afiliação.

### III. Logística e gestão de rotina na permanência nas IFES (ANDIFES/FONAPRACE)

**Fonte:** ANDIFES / FONAPRACE — V Pesquisa Nacional de Perfil Socioeconômico e Cultural dos(as) Graduandos(as) das IFES.

O levantamento mostra que fatores cotidianos e logísticos estão entre os principais geradores de estresse acadêmico e queda de rendimento nos semestres iniciais. Entre eles: deslocamento por transporte público até campi afastados, horários do Restaurante Universitário (RU), conciliação entre trabalho e estudo e desorganização com o calendário de provas. Centralizar essas utilidades em uma única plataforma reduz a sobrecarga cognitiva do ingressante.

## 3. Escopo funcional

O sistema se divide em quatro módulos.

### Módulo 1 — Guia dinâmico de fluxo curricular e "macetes" regimentais

Apresenta a estrutura do curso sem exigir a leitura do Projeto Pedagógico do Curso (PPC) ou do Regulamento da Graduação.

- **Mapa interativo da grade curricular:** fases/semestres, mostrando quais matérias trancam outras (pré-requisitos) e quais são livres.
- **Tradutor de regras e "macetes":** explica na prática aprovação, frequência mínima, recuperação e exceções de progressão. Ilustra cenários reais, por exemplo atingir nota 4,0 em um componente para destravar a matéria seguinte sem atrasar o fluxo.
- **Guia de horas complementares (ACCs):** como validar atividades extracurriculares, limites de horas por categoria e o que conta para a formatura.

### Módulo 2 — Motor inteligente de cálculo e predição de notas

Cada professor adota critérios diferentes (pesos, listas, trabalhos, substitutivas), então o sistema usa fórmulas adaptáveis, não uma fórmula fixa.

- **Configuração de fórmulas:** o aluno (ou o professor/líder de turma) cadastra como a nota da disciplina é calculada no semestre. O modelo fica salvo para a turma.
- **Cálculo preditivo ("Quanto eu preciso tirar?"):** o estudante informa só as notas já recebidas. O sistema calcula a média parcial e projeta a nota mínima necessária na próxima avaliação para atingir a média de aprovação (ou a nota mínima para não travar pré-requisitos).

### Módulo 3 — Agenda acadêmica colaborativa

- **Alimentação híbrida de eventos:** gestão individual (lembretes próprios) e compartilhamento por disciplina (professor ou colega cadastra a data e todos os matriculados veem no painel).
- **Alertas de gargalo ("Semanas críticas"):** indicador visual de acúmulo de provas e entregas na mesma semana.

### Módulo 4 — Hub de sobrevivência e logística do campus (UFFS Chapecó)

- **Mapa interativo do campus:** blocos (A, B, C etc.), salas, laboratórios de informática, biblioteca, auditórios, setores de atendimento (SAE, Secretaria Acadêmica) e pontos de convivência.
- **Horários e serviços essenciais:** linhas de ônibus que atendem o campus, funcionamento e cardápio do RU, horários da biblioteca e contatos úteis.
- **Mural de dicas de veteranos:** orientações curadas sobre o curso, grupos de estudo, laboratórios de pesquisa, monitorias e editais de auxílio estudantil.

## 4. Matriz resumo de requisitos (Sprint 1)

| Código | Categoria | Descrição | Prioridade (MVP) |
|--------|-----------|-----------|------------------|
| RF01 | Fluxo Acadêmico | Exibir de forma visual e interativa a grade de horários, semestres e cadeias de pré-requisitos do curso. | Alta |
| RF02 | Regras e Macetes | Simular cenários de aprovação, exame/recuperação e regras de destravamento condicional de matérias (ex.: impacto de atingir nota 4,0 vs. média final 6,0). | Alta |
| RF03 | Calculadora Inteligente | Permitir a criação e o salvamento de fórmulas personalizadas de cálculo de média por disciplina/professor. | Alta |
| RF04 | Predição de Nota | Calcular automaticamente a nota restante necessária nas avaliações futuras com base apenas nas notas parciais inseridas pelo aluno. | Alta |
| RF05 | Agenda de Provas | Permitir o cadastro individual e o compartilhamento coletivo (aluno/professor) de datas de provas e entregas de trabalhos. | Média |
| RF06 | Utilidades do Campus | Disponibilizar módulo informativo com mapa dos blocos/laboratórios, horários de ônibus, funcionamento do RU e guia de bolsas/ACCs. | Média |
| RNF01 | Usabilidade | Interface responsiva (Mobile-First), garantindo consulta rápida pelo celular nos corredores ou no ônibus. | Alta |
| RNF02 | Simplicidade | Operar de forma independente de integrações burocráticas complexas no MVP, priorizando agilidade de cadastro pelo próprio estudante. | Alta |
