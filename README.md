
# Projeto Disciplina: Requisitos de Software

Olá! Este repositório faz parte do projeto da disciplina de Requisitos de Software da UTFPR - Campus Cornélio Procópio. 

Link do Padlet: https://padlet.com/rossipoke/kanban-yzskebb8cfh8no7f

## 1. Introdução

***1.1.  Nome do Grupo***

Samuel Ribeiro da Costa - https://github.com/Sam-Ribeiro

Raphael Rossi - https://github.com/rossipoke

***1.2.  Nome do Sistema***

MindSteps

***1.3.  Propósito do Sistema***

Este documento apresenta os requisitos dos usuários a serem desenvolvidos pela **MindSteps Corporation**, fornecendo aos desenvolvedores as informações necessárias para o projeto e implementação, assim como para a realização dos testes e homologação do sistema.

O objetivo do sistema **MindSteps** é oferecer uma plataforma gamificada de apoio ao ensino universitário, permitindo que professores criem desafios de forma prática e que alunos estudem de maneira mais motivadora e recompensadora. A solução busca facilitar o acompanhamento do desempenho, estimular a disciplina nos estudos diários e transformar o aprendizado em uma experiência dinâmica.

***1.2.  Público Alvo***

O público-alvo do aplicativo são professores e estudantes universitários que buscam tornar o processo de ensino mais dinâmico e leve. Professores que precisam de ferramentas práticas para criar e acompanhar atividades, aumentando o engajamento da turma, enquanto alunos desejam métodos de estudo interativos e motivadores que facilitem a organização e a assimilação de conteúdos.

***Personas:***

![Persona Professor](2.jpg)

![Persona Aluno](3.jpg)
____

***Análise da situação atual: antes da introdução de sua solução***

*`1. O que as pessoas fazem?`*

Professores preparam listas de exercícios, trabalhos e leituras, geralmente em papel ou PDF.

Alunos recebem as atividades, muitas vezes sem prazos intermediários ou incentivos de engajamento.

O estudo costuma ser individual e pouco interativo, com baixa motivação.

A entrega das atividades ocorre por e-mail ou sistemas acadêmicos engessados.

*`2. Quais os artefatos envolvidos?`*

Apostilas, livros físicos e PDFs.

Plataformas institucionais (como Moodle ou Google Classroom).

E-mail para comunicação.

Papel e caneta para resolução de exercícios.

*`3. O que elas precisam saber?`*

Como acessar as plataformas da universidade.

Datas de provas e entregas de trabalhos.

Conteúdo das disciplinas (geralmente de forma tradicional).

Ferramentas digitais básicas (Word, Excel, PowerPoint).

____

***Análise das tarefas depois: como serão executadas as suas tarefas com sua solução:***

*`1. O que as pessoas fazem?`*

Professores criam desafios diários e atividades gamificadas diretamente no aplicativo.

Alunos acessam os desafios pelo celular ou computador e respondem de forma interativa.

O progresso é acompanhado em tempo real, com pontuações, recompensas e rankings.

Feedback é dado automaticamente ou de forma facilitada pelo professor.

*`2. Quais os artefatos envolvidos?`*

Aplicativo gamificado (plataforma web/mobile).

Sistema de pontuação, recompensas e rankings.

Relatórios automáticos de desempenho.

Conteúdo digital interativo (quizzes, simuladores, vídeos curtos, flashcards).

*`3. O que elas precisam saber?`*

Como usar o aplicativo (interface intuitiva, login, navegação básica).

Regras de pontuação e funcionamento dos desafios.

Conteúdo das disciplinas, mas agora de forma mais aplicada e prática.

Como acompanhar o próprio progresso dentro do sistema.

____

***Cenário: Antes***

Ricardo (professor) envia uma lista de exercícios em PDF por e-mail. Lucas (aluno) baixa o arquivo, resolve no papel e, muitas vezes, esquece de entregar ou deixa para última hora. A motivação é baixa e o estudo é visto apenas como obrigação. Não há acompanhamento em tempo real e o professor demora para corrigir.

***Cenário: Depois***

Ricardo cria desafios diários no aplicativo. Lucas acessa pelo celular no intervalo entre aulas, responde aos exercícios interativos e acumula pontos. Ele acompanha seu progresso no ranking da turma, recebe feedback imediato e se sente motivado a continuar. Ricardo, por sua vez, visualiza relatórios automáticos com os acertos e dificuldades da turma, podendo ajustar o conteúdo das próximas aulas.

## 2. Documentos gerais no repositório

***2.1. Requisitos Funcionais***

| Código  | Nome | Descrição | Prioridade | MoSCoW | Dependencia |
| ------- | ---- | --------- | ---------- | ------ | ----------- |
| RF01 | Busca básica  | O sistema deve permitir buscar por nome de professor, questqao especifica, disciplina, ou termo genérico. Resultado com cards resumidos (professor, disciplina, conteudo abordado e previa da questao). | Média | M |
| RF02 | Perfil do professor / local | Ao abrir um resultado, exibir: foto/nome, departamento/faculdade, disciplinas que ministra, contato (email/ramal), banco de questoes do professor. | Alta | M |
| RF03 | Pontuacao e Score | A depender do tempo de resposta e da resposta escolhida o usuario ganhara pontos para a conta, onde ele pode comparar com os amigos e colegas | Baixa | S |
| RF04 | Considerar conflitos | Se uma questao tiver 3 ou mais pedidos de atualização por resposta errada/etc... a questao fica temporariamente desativada da plataforma ate a correção do professor responsavel. | Média | M |
| RF05 | Modo professor | Permitir modo de criacao de questoes, avaliacao e edição de questoes criadas pelo proprio professor, referente ao login | Alta | M |
| RF06 | Favoritos e histórico | Salvar questoes/professores favoritos e histórico de questões | Média | S |
| RF07 | Modos de preferências | O aluno pode escolher por preferencias de conteudos ou disciplinas, podendo se tornar tambem preparatorio para provas ou atividades | Média | S |
| RF08 | Autenticação e níveis de acesso | Login via conta institucional (SSO) para acessar funcionalidades restritas (ex.: Perguntas apenas de professores da sua instituição). | Alta | M |
| RF09 | Feedback/Relatar problema | Usuários podem reportar erros nas respostas diretamente ao professor que a fez ou problemas de acessibilidade entre outros para o suporte de desenvolvimento | Média | M |
| RF10 | Banco de dados | Banco relacional (ex.: PostgreSQL) para dados relacionais (professores, disciplinas, conteudos, questoes). | Alta | M |

***2.2. Requisitos Não Funcionais***

| Código  | Nome | Descrição | Prioridade | MoSCoW | Dependencia |
| ------- | ---- | --------- | ---------- | ------ | ----------- |
| RNF01 | Tempo de resposta | Tempo de resposta para busca simples ≤ 5s | Baixa | M |
| RNF02 | Escalabilidade | Suportar crescimento até 3000 usuários ativos simultâneos | Alta | M |
| RNF03 | Autenticação de senhas | Autenticação via SSO; senhas não armazenadas localmente. Controle de acesso baseado em papéis; logs de auditoria | Média | S |
| RNF04 | Segurança | Conformidade com LGPD (Brasil) — consentimento para uso de dados pessoais, direito de acesso, exclusão à pedido. Criptografia de senhas. | Média | M |
| RNF05 | Usabilidade | UX mobile-first; telas com tempo de aprendizado ≤ 5 min para usuário novo; suporte a acessibilidade WCAG AA (contraste, leitor de tela, navegação por teclado) | Média | M |
| RNF06 | Localização/Internacionalização | Texto configurável para PT-BR (padrão); suporte para EN e ES opcional. | Baixa | C |
| RNF07 | Autenticação via google | Suporte com login OAuth com o google do e-mail universitário ou credenciais do portal do aluno. | Média | S |
| RNF08 | Atualização de dados em tempo real | Webhooks ou sockets para receber notificações de alteração de questoes do sistema. | Alta | M |
| RNF09 | Logs e auditoria | Registrar eventos importantes (login, busca, questoes respondidas, pontos recebidos por questao, alteração de dados) para monitoramento e debugging | Baixa | S |
| RNF10 | Backend e API | REST/GraphQL API para app (endpoints para busca, perfil, favoritos). Autorização baseada em roles. | Alta | M |
| RNF11 | Integração com base institucional | API ou ETL para sincronizar dados: cadastro de professores, alunos, turmas, grade horária. | Média | S |

***2.3. Perguntas***

*<Arquivo com as perguntas realizadas na entrevista .>*

***2.4. Entrevista***

*<Arquivo com as respostas do indivíduo entrevistado e link do drive com upload da gravação.>*

***2.5. Histórias do Usuário***

*<Imagem, arquivo (PDF), link com as Histórias de Usuário.>*

***2.6. Diagramas de Caso de Uso e Especificações***

*<Imagem, arquivo (PDF), link com Diagrama de Caso de Uso.>*

***2.7. Diagramas de Atividades***

*<Imagem, arquivo (PDF), link com Diagrama de Atividades.>*

***2.8. Protótipos***

*<Imagem, arquivo (PDF), link com Protótipo.>*

## Referências

*<Esta seção é destinada à descrição das referências utilizadas pelo documento, como por exemplo, URLs e livros. Ver exemplo a seguir:>*

[1] “Glossário da _USina_”, <_id_doc glossário_>, Versão <_versão_>. Localização: <_localização_>.
