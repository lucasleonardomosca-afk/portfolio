# Como Usar seu Measurement ID Real no Google Analytics

## Status Atual

✅ **GA4 está configurado no site com Measurement ID de teste:** `G-DUMMYTEST123`

⚠️ **Este ID é apenas um placeholder para testes**

---

## 3 Passos para Ativar o Google Analytics com seu ID Real

### 1️⃣ Criar Propriedade no Google Analytics (5 minutos)

```
1. Acesse: https://analytics.google.com
2. Clique em "Criar" ou "+ Create Property"
3. Preencha:
   - Property Name: "Lucas Leonardo Mosca - Portfolio"
   - Timezone: America/Sao_Paulo
   - Currency: BRL
4. Clique em "Create"
```

### 2️⃣ Configurar Web Stream (3 minutos)

```
1. Em "Data Streams", clique "+ Add stream"
2. Selecione "Web"
3. Preencha:
   - Website URL: https://lucasleonardomosca-afk.github.io/portfolio/
   - Stream name: Portfolio Analytics
4. Clique em "Create stream"
```

### 3️⃣ Copiar seu Measurement ID e Atualizar no Site (2 minutos)

**Na tela do Google Analytics:**
1. Você verá o "Measurement ID" (formato: `G-XXXXXXXXXX`)
2. Copie esse ID

**No GitHub (seu repositório):**
1. Abra o arquivo `index.html`
2. Clique no lápis para editar
3. Pressione `Cmd+F` (Mac) ou `Ctrl+H` (Windows)
4. Digite: `G-DUMMYTEST123`
5. Substitua por: `G-SEU-ID-REAL-AQUI` (ex: `G-ABC123DEF45`)
6. Clique "Replace All"
7. Clique em "Commit changes"
8. Escreva a mensagem: "Update Measurement ID with production value"
9. Clique em "Commit changes"

---

## ✅ Pronto!

Após fazer commit, seu site começará a coletar dados em:

- ⏱️ **Realtime:** Acesse `Reports → Realtime` no Google Analytics
- 📊 **Próximas 24h:** Dados completos começarão a aparecer

---

## 📝 Checklist

- [ ] Criei propriedade no Google Analytics
- [ ] Configurei Web Stream
- [ ] Copiei o Measurement ID
- [ ] Atualizei o `index.html` com o ID real
- [ ] Fiz commit das alterações
- [ ] Aguardei 24h para dados aparecerem
- [ ] Acessei `Reports → Realtime` para ver visitantes

---

## 🔍 Como Verificar se Está Funcionando

1. Acesse seu site: https://lucasleonardomosca-afk.github.io/portfolio/
2. Abra uma nova aba e vá para Google Analytics
3. Clique em `Reports → Realtime`
4. Você deve ver a si mesmo visitando em tempo real

---

## 🆘 Troubleshooting

**"Nenhum dado aparecendo no GA4?"**

1. ✅ Verifique se o Measurement ID está correto (sem espaços)
2. ✅ Certifique-se que atualizou AMBAS as ocorrências no `index.html` (linhas 13 e 18)
3. ✅ Aguarde 24 horas - GA4 não mostra dados instantaneamente
4. ✅ Abra o Console do navegador (F12) e procure por erros
5. ✅ Confirme que está visitando a URL correta do site

---

## 📚 Arquivos Relacionados

- `index.html` - Seu site (contém o script GA4)
- `ANALYTICS_SETUP.md` - Guia detalhado de setup
- `GA4_IMPLEMENTATION_SUMMARY.md` - Resumo da implementação

---

## 🎉 Sucesso!

Uma vez configurado, você terá acesso a:

- Pageviews por página
- Visitantes únicos
- Origem do tráfego
- Dispositivos utilizados
- Localização dos visitantes
- E muito mais!

**Seu portfólio agora está pronto para análise de tráfego!** 🚀
