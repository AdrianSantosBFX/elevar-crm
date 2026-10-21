# ELEVAR.CRM 0.3.4

Protótipo local do CRM operacional da Elevar. **HTML, CSS e JavaScript**, sem servidor de aplicação.

## Executar

Abra `index.html` em um navegador moderno. Para servir por HTTP local, execute na pasta do projeto:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Acesse `http://127.0.0.1:8000/`. O Python é opcional e serve apenas os arquivos estáticos.

## Dados da versão de portfólio

A base operacional começa vazia. O usuário inicial é demonstrativo e os valores padrão do catálogo estão zerados para configuração. Os dados inseridos ficam no `localStorage` da origem e navegador utilizados. Use a exportação JSON para manter backups.

## Estrutura

`index.html` monta a página, `styles.css` define a interface e `app.js` contém a navegação, as regras e a persistência.


## Arquitetura

### Comercial
Lead → Contato → Conversa → Diagnóstico → Proposta → Negociação → Contratação → Ganha/Perdida.

Uma venda ganha pode ser convertida em projeto. Se estiver em Contratação, o CRM exige contrato assinado e entrada confirmada antes da conversão.

### Projetos
Aguardando kickoff → Kickoff → Planejamento → Desenvolvimento → Homologação → Aceite → Garantia → Encerrado.

Cada projeto possui:
- objetivo e escopo;
- fora do escopo;
- dependências e riscos;
- entregáveis;
- parcelas e recebimentos;
- documentos com status;
- Change Requests;
- atividades, histórico e notas.

## Diagnóstico Elevar
A oportunidade registra uma sessão inicial gratuita com problema, processo atual, ferramentas, frequência, horas/mês, impacto e recomendação. As classificações são ELEVAR FIT, PROCESS FIRST, PARTNER FIT, FUTURE e NO ACTION.

## Empresa / ICP
O perfil da empresa armazena carteira, equipe, ERP, outros sistemas, regimes atendidos e maturidade digital. O CRM calcula um ICP Score simples com base no perfil inicial da Elevar.

## Persistência
Esta versão ainda usa `localStorage` para funcionar sem backend. Exporte backups JSON em Configurações. A v1.0 deverá migrar para autenticação + banco de dados.

## Migração
A v0.3.0 procura automaticamente dados da v0.2.0 e versões anteriores. Oportunidades antigas que já estavam em execução são migradas para venda ganha + projeto ativo.


## Correção 0.3.3
- Corrigida a responsividade do card **Próximas atividades** no dashboard.
- O bloco agora recebe mais largura em desktop e simplifica colunas conforme a largura real do próprio card.
- O painel secundário do dashboard passa a empilhar antes de ficar comprimido.
- Melhorado o comportamento do cabeçalho e do botão **Abrir agenda** em telas pequenas.


## Contatos dependentes da empresa (v0.3.3)
- Em formulários com Empresa + Contato, o contato agora é filtrado pela empresa selecionada.
- Ao trocar a empresa, qualquer contato incompatível é removido automaticamente.
- Em Nova atividade, selecionar uma oportunidade ou projeto preenche a empresa e restringe os contatos à organização correta.
- A validação no salvamento impede gravar contato pertencente a outra empresa mesmo em caso de manipulação do formulário.


## Correção 0.3.3 — Fechamento de janelas
Os modais e drawers agora usam fechamento por backdrop sem bloquear a delegação global de eventos. Botões Cancelar, Fechar e × funcionam normalmente, e Esc permanece disponível como atalho de fechamento.


## v0.3.4 — base limpa
- Removidos todos os dados operacionais fictícios: empresas, contatos, oportunidades, projetos, atividades, parceiros, histórico e notas.
- Preservados apenas usuário responsável, equipe interna, catálogo de serviços, etapas e configurações estruturais.
- Nova chave de armazenamento local para impedir que dados demo de versões anteriores reapareçam automaticamente.
- "Restaurar demonstração" substituído por "Restaurar base vazia".
