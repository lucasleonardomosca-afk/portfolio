# Google Analytics Setup Guide

## Status
✅ Google Analytics GA4 tracking script has been added to `index.html`

## Next Steps - IMPORTANTE

O script do Google Analytics foi adicionado ao seu portfólio, mas você precisa configurar uma propriedade no Google Analytics e obter seu **Measurement ID** para ativar o rastreamento.

### 1. Criar uma Propriedade no Google Analytics (GA4)

1. Acesse: https://analytics.google.com
2. Clique em **"Criar" ou "New Property"**
3. Preencha as informações:
   - **Property Name:** "Lucas Leonardo Mosca - Portfolio"
   - **Timezone:** America/Sao_Paulo
   - **Currency:** BRL
4. Clique em **"Create"**

### 2. Configurar Website Stream

1. Em **Data Streams**, clique em **"Add stream"**
2. Selecione **Web**
3. Preencha:
   - **Website URL:** https://lucasleonardomosca-afk.github.io/portfolio/
   - **Stream Name:** Portfolio Analytics
4. Clique em **"Create stream"**

### 3. Obter o Measurement ID

1. Copie o **Measurement ID** (formato: G-XXXXXXXXXX)
2. Este é o valor que você precisa inserir no `index.html`

### 4. Atualizar o index.html com seu Measurement ID

1. Edite o arquivo `index.html`
2. Procure por `G-MEASUREMENT_ID` (linhas 13 e 18)
3. Substitua AMBAS as ocorrências pelo seu ID real, ex: `G-ABC123DEF45`
4. Faça commit das alterações

### 5. Verificar se está funcionando

1. Aguarde até 24 horas para que os dados começarem a aparecer no GA4
2. Acesse https://analytics.google.com
3. Vá em **Reports → Realtime** para ver visitantes em tempo real
4. Você verá pageviews, origem do tráfego, etc.

## Dados que você verá

- **Pageviews:** Quantas vezes as páginas foram visitadas
- **Users:** Visitantes únicos
- **Sessions:** Sessões de navegação
- **Traffic Source:** De onde vêm os visitantes (search, direct, referral)
- **Device Info:** Desktop, mobile, tablet
- **Geographic Data:** País, região dos visitantes

## Notas Importantes

⚠️ O `G-MEASUREMENT_ID` no arquivo é apenas um placeholder
⚠️ Analytics levará até 24 horas para começar a coletar dados
⚠️ Você precisa de uma conta Google para acessar o Google Analytics
⚠️ O script foi adicionado no `<head>` do documento para melhor performance

## Suporte

Se tiver problemas:
1. Verifique se o Measurement ID está correto (sem espaços)
2. Confirme que o site está publicado no GitHub Pages
3. Verifique a console do navegador (F12) para erros
