# Política de Governança de Código - Portfolio

**Documento Interno - Estritamente Confidencial**

## Visão Geral

Este documento define a governança operacional para o repositório do Portfolio Executivo B2B, incluindo papéis, responsabilidades, fluxo de trabalho e políticas de acesso a código proprietário.

## 1. Classificação e Acesso

### Nível de Classificação: **PROPRIETÁRIO**
- Código-fonte: **Restrito** (somente colaboradores autorizados)
- Documentação: **Parcialmente Pública** (README visível, detalhes internos confidenciais)
- Contratos de Licença: **Confidencial** (entre Lucas Leonardo Mosca e cliente)

### Autorização de Acesso
- **Admin**: Lucas Leonardo Mosca
- **Maintainers**: Colaboradores da equipe de desenvolvimento (quando aplicável)
- **Readers**: Não permitido para código-fonte em repositório privado

## 2. Papéis e Responsabilidades

### Owner
- **Lucas Leonardo Mosca**
- Responsabilidades:
  - Controle total do repositório
  - Aprovação final de releases
  - Gestão de contratos de licença com clientes
  - Decisões de arquitetura críticas

### Maintainer (se aplicável)
- Responsabilidades:
  - Revisar pull requests
  - Garantir qualidade de código
  - Atualizar CHANGELOG e versioning
  - Assinar commits

### Contributor (se aplicável)
- Responsabilidades:
  - Desenvolver features em branches próprias
  - Submeter PRs com descrição detalhada
  - Garantir commits assinados
  - Respeitar convenções de código

## 3. Fluxo de Trabalho de Desenvolvimento

### Branches
- **main**: Versão stable em produção. Protegida.
- **develop**: Integração (se usar Git Flow)
- **feature/*** : Branches de features (ex: feature/new-component)
- **bugfix/*** : Branches de correção (ex: bugfix/responsive-issue)

### Pull Request Workflow
1. Criar feature branch a partir de `main`
2. Implementar mudanças localmente
3. Fazer commit COM ASSINATURA (git commit -S)
4. Push para origin
5. Abrir Pull Request
6. Aguardar aprovação (mínimo 1 review)
7. Merge após aprovação
8. Deletar branch de feature
9. Atualizar CHANGELOG.md
10. Criar tag de release (vX.Y.Z)

### Políticas de Commit
```
✅ Obrigatório:
- Commits assinados com GPG/SSH (-S flag)
- Mensagens descritivas (sem "fix" genérico)
- Uma mudança por commit

❌ Proibido:
- Force push em main
- Merges sem PR
- Commits não assinados
- Large files (> 100MB)
```

## 4. Versionamento e Releases

### Semantic Versioning
```
v MAJOR . MINOR . PATCH
  ^       ^       ^
  |       |       └─ Bug fixes, no functional change
  |       └─────────  New features, backwards compatible
  └──────────────────  Breaking changes
```

### Processo de Release
1. Criar release branch: `release/v1.0.0`
2. Incrementar versão em:
   - CHANGELOG.md
   - package.json (se aplicável)
   - Tags de git
3. Criar pull request → main
4. Após merge, criar tag anotada: `git tag -a v1.0.0 -m "Release v1.0.0"`
5. Push de tag: `git push origin v1.0.0`
6. Publicar release notes no GitHub
7. Notificar cliente de nova versão (se contratado)

### Contrato de Versionamento
Cada versão liberada é ancorada a:
- Data de release
- Cliente autorizado
- Escopo de mudanças (Features, Bugfixes)
- Garantia de suporte

## 5. Segurança e Propriedade Intelectual

### Proteção de IP
- ✅ Código-fonte: **All Rights Reserved** (LICENSE)
- ✅ Branches protegidas: `main` não pode ser deletado ou reescrito
- ✅ Commits assinados: Auditoria de autoria
- ✅ Proibição explícita: IA, LLM, scraping, engenharia reversa

### Proibições Absolutas para Colaboradores
❌ **Estritamente Proibido:**
1. Clonar ou compartilhar repositório com terceiros
2. Usar código em Google AI Studio, ChatGPT, Claude ou similares
3. Fazer scraping ou análise automatizada
4. Redistribuir em qualquer formato
5. Rever-engenharia para criar similares
6. Submeter a plataformas de IA/ML
7. Usar em produtos concorrentes

### Auditoria
- Todos os commits são rastreados com assinatura GPG/SSH
- Logs de acesso ao repositório são mantidos
- Mudanças críticas requerem aprovação de 2 reviewers (se aplicável)

## 6. Uso de Ferramentas de IA

### Proibido em Desenvolvimento
❌ Ferramentas bloqueadas:
- GitHub Copilot (a menos que explicitamente autorizado)
- ChatGPT, Claude, Bard, Gemini
- Google AI Studio
- Qualquer modelo generativo de código

### Permitido com Restrições
✅ Uso autorizado:
- Geração de trechos genéricos (sem componentes críticos do projeto)
- Pesquisa de sintaxe/documentação
- **Apenas com aprovação prévia do Owner**

## 7. Conformidade Legal

### Documentos Obrigatórios
- ✅ LICENSE: Proprietário com "All Rights Reserved"
- ✅ README.md: Aviso legal explícito
- ✅ CHANGELOG.md: Registro de versões
- ✅ GOVERNANCE.md: Este documento

### Conformidade com Contratos
Cada colaborador deve ter:
1. Acordo de NDA (Non-Disclosure Agreement)
2. Contrato de Trabalho/Freelancer
3. Reconhecimento de propriedade intelectual do Owner
4. Aceituação desta política de governança

## 8. Monitoramento e Compliance

### Checklist de Governance
- [ ] Código em repositório privado
- [ ] Branch `main` protegida (PR obrigatória)
- [ ] Commits assinados obrigatórios
- [ ] Sem forking permitido
- [ ] Aviso legal em README
- [ ] LICENSE com "All Rights Reserved"
- [ ] CHANGELOG atualizado por release
- [ ] GOVERNANCE.md (este documento) comunicado

### Relatório de Conformidade
Revisar mensalmente:
- Commits não assinados
- Acessos ao repositório
- Alterações em configurações de acesso
- Atualizações de LICENSE

## 9. Contato e Perguntas

**Owner**: Lucas Leonardo Mosca  
**Email**: lucaslmosca@gmail.com  
**Política Válida**: 2024-2026

---

**Versão**: 1.0.0  
**Última Atualização**: 08/01/2026  
**Próxima Revisão**: 08/01/2027
