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

Crie uma pasta chamada `projeto-formulario` e abra o terminal dentro dela.

```
git init
```

---

## 📅 Dia 1 — Criar o formulário

Crie um arquivo chamado `index.html` e cole o conteúdo abaixo:

```html
<form>
  <input type="text" placeholder="Seu nome" />
  <button>Enviar</button>
</form>
```

Salve o arquivo, volte ao terminal e rode:

```
git add index.html
git commit -m "dia 1: criei o formulário"
```

---

## 📅 Dia 2 — Melhorar o botão

Abra `index.html` e **substitua** o conteúdo pelo texto abaixo:

```html
<form>
  <input type="text" placeholder="Seu nome" />
  <button style="background: blue; color: white; padding: 8px 16px;">
    Enviar agora
  </button>
</form>
```

Salve e rode:

```
git add index.html
git commit -m "dia 2: melhorei o botão do formulário"
```

---

## 📅 Dia 3 — Adicionar uma logo

Abra `index.html` e **substitua** o conteúdo pelo texto abaixo:

```html
<img src="logo.png" alt="Logo da empresa" />

<form>
  <input type="text" placeholder="Seu nome" />
  <button style="background: blue; color: white; padding: 8px 16px;">
    Enviar agora
  </button>
</form>
```

Salve e rode:

```
git add index.html
git commit -m "dia 3: adicionei a logo"
```

---

## 🔍 Ver o histórico completo

```
git log --oneline
```

Você verá algo assim:

```
e7c3a91  dia 3: adicionei a logo
b2f1d04  dia 2: melhorei o botão do formulário
a9e8c12  dia 1: criei o formulário
```

> **Copie o código de 7 letras do commit do Dia 2** — você vai precisar dele agora.
> No exemplo acima, seria `b2f1d04`. No seu computador, o código será diferente.

---

## ⏪ Voltar para o Dia 2

Com o código do Dia 2 em mãos, rode:

```
git checkout b2f1d04
```

> ⚠️ Substitua `b2f1d04` pelo código que apareceu **no seu** `git log`.

Agora abra o arquivo `index.html` e veja: **a logo sumiu**. O arquivo voltou exatamente como estava no Dia 2, com o botão melhorado mas sem a logo.

---

## ↩️ Voltar para o presente

Quando quiser voltar para a versão mais recente (Dia 3), rode:

```
git checkout master
```

> Se o comando acima não funcionar, tente `git checkout main`.

Abra o `index.html` — a logo voltou. Você está no presente novamente.

---

## ✅ Checklist de conclusão

- [ ] Criei os 3 commits (um por dia)
- [ ] Rodei `git log --oneline` e vi os 3 commits na lista
- [ ] Usei `git checkout` com o código do Dia 2
- [ ] Abri o arquivo e confirmei que a logo havia sumido
- [ ] Voltei para o presente com `git checkout main`

---

## 🏆 Desafio extra

Rode `git log --oneline` e use `git checkout` para visitar o **Dia 1** também.
Confirme que o botão ainda é simples, sem estilo.
Depois volte para o presente.

---

> 💡 **O que aconteceu aqui?**
> O Git não apagou nada. O Dia 3 ainda existe no histórico. Você apenas "visitou" uma versão anterior — como folhear um álbum de fotos sem rasgar nenhuma página.