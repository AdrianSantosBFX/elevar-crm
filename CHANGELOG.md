# Changelog

## 0.3.4
- Base operacional zerada para testes manuais do fluxo real.
- Removidos cadastros fictícios e dados de demonstração.
- Contadores de códigos reiniciados em 1.
- Nova chave de localStorage isolada das versões demo anteriores.
- Configurações agora restauram uma base vazia, não dados fictícios.

# Changelog

## 0.3.3 — Correção de fechamento de janelas
- Corrigido o bloqueio de cliques causado por `stopPropagation()` em modais e drawers.
- Botões **Cancelar**, **Fechar** e **×** voltaram a funcionar em todas as janelas.
- Ações internas de modais/drawers passam a usar corretamente a delegação global de eventos.
- Clique no backdrop fecha a janela somente quando o clique acontece fora do conteúdo.
- `Esc` continua fechando modal, drawer comercial e drawer de projeto.

## 0.3.2 — Correção de vínculo Empresa → Contato
- Novo sistema de seleção dependente entre empresa e contato.
- Nova oportunidade mostra apenas contatos da empresa escolhida.
- Nova/edição de atividade mostra apenas contatos da empresa escolhida.
- Seleção de oportunidade ou projeto em atividade preenche o contexto empresarial automaticamente.
- Troca de empresa limpa contato incompatível.
- Validação adicional no submit impede relações Empresa/Contato inválidas.

# ELEVAR.CRM v0.3.1

## Corrigido
- Card **Próximas atividades** espremido em larguras intermediárias.
- Breakpoint do dashboard ajustado para empilhar os painéis antes da perda de legibilidade.
- Linhas de atividades agora escondem metadados secundários progressivamente conforme a largura disponível.
- Cabeçalho do card e CTA **Abrir agenda** adaptados para tablet e mobile.

---

# Changelog

## 0.3.0
- Separação definitiva entre Comercial e Projetos.
- Pipeline comercial termina em Ganha/Perdida; projetos deixam de contaminar forecast e win rate.
- Conversão Oportunidade → Projeto com código PRJ e migração automática da v0.2.0.
- Dashboard “Precisa da sua atenção” para oportunidades sem próxima ação, propostas paradas, contratos/entradas pendentes, projetos atrasados e parcelas vencidas.
- Perfil de Empresa ampliado com carteira, equipe, ERP, outros sistemas, regimes, maturidade digital e ICP Score.
- Sessão de Diagnóstico estruturada (data, participantes, ferramentas, frequência, horas/mês, impacto, recomendação, classificação e próximo passo).
- Proposta e contrato estruturados com versão, validade, status, assinatura e entrada.
- Módulo Projetos com board próprio, escopo, entregáveis, dependências, riscos, financeiro, documentos e Change Requests.
- Documentos deixam de ser booleanos e passam a ter estados operacionais.
- Contatos ganham canal preferido, papel decisório e consentimento comercial.
- Busca global passa a incluir projetos.
- Relatórios corrigidos para separar venda de execução.
