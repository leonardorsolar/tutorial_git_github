# 🧑‍💻 Exercício: 3 dias como dev — e voltando no tempo

**Nível:** Iniciante | **Tempo estimado:** 20 minutos

> Você vai simular o trabalho real de um desenvolvedor durante 3 dias, salvar cada versão, e depois **voltar para o Dia 2** — como se o Dia 3 nunca tivesse existido.

---

## 📋 O que você vai praticar

- `git init`, `git add`, `git commit`
- `git log --oneline` — ver o histórico
- `git checkout` — viajar no tempo

---

## 📁 Preparação

Crie uma pasta chamada `projeto-html-css` e abra o terminal dentro dela.

```
git init
```

---

## 📅 Dia 1 — Criar o formulário

Tarefa (Feature):
- Crie um arquivo chamado `index.html`
- Criar um título


```html
<h1>Tag Título<h1>
```

Salve o arquivo, volte ao terminal e rode:

```
git add index.html
git commit -m "dia 1: criar o título"
```

---

## 📅 Dia 2 — Melhorar o botão

Tarefa (Feature): Adicionar no `index.html` um parágrafo 

```html
<p>Esta é uma tag parágrafo<p>
```

Salve e rode:

```
git add index.html
git commit -m "dia 2: criar o parágrafo"
```

---

## 📅 Dia 3 — Adicionar estilo css

Tarefa (Feature): Adicionar no `index.html` uma cor vermelha para o título.

```html
<h1 style="color: red">Tag Título<h1>
```

Salve e rode:

```
git add index.html
git commit -m "dia 3: adicionar a cor vermelha ao título"
```

---

## 🔍 Ver o histórico completo

```
git log --oneline
```

Você verá algo assim:

```
3d8f7c5 (HEAD -> master) dia 3: adicionar a cor vermelha ao título
b963ef4 dia 2: criar o parágrafo
978a864 dia 1: criar o título
```

> **Copie o código de 7 letras do commit do Dia 2** — você vai precisar dele agora.
> No exemplo acima, seria `b963ef4`. No seu computador, o código será diferente.

---

## ⏪ Voltar para o Dia 2

Com o código do Dia 2 em mãos, rode:

```
git checkout b2f1d04
```

> ⚠️ Substitua `b963ef4` pelo código que apareceu **no seu** `git log`.

Agora abra o arquivo `index.html` e veja: **o estilo css sumiu**. O arquivo voltou exatamente como estava no Dia 2.

---

## ↩️ Voltar para o presente

Quando quiser voltar para a versão mais recente (Dia 3), rode:

```
git checkout master
```

> Se o comando acima não funcionar, tente `git checkout main`.

Abra o `index.html` — o estilo voltou. Você está no presente novamente.

---

## ✅ Checklist de conclusão

- [ ] Criei os 3 commits (um por dia)
- [ ] Rodei `git log --oneline` e vi os 3 commits na lista
- [ ] Usei `git checkout` com o código do Dia 2
- [ ] Abri o arquivo e confirmei que estilo havia sumido
- [ ] Voltei para o presente com `git checkout main`

---

## 🏆 Desafio extra

Rode `git log --oneline` e use `git checkout` para visitar o **Dia 1** também.
Confirme que o botão ainda é simples, sem estilo.
Depois volte para o presente.

---

> 💡 **O que aconteceu aqui?**
> O Git não apagou nada. O Dia 3 ainda existe no histórico. Você apenas "visitou" uma versão anterior — como folhear um álbum de fotos sem rasgar nenhuma página.