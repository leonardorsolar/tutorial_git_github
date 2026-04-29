# 🧪 Exercício: Seu Primeiro Repositório Git

**Nível:** Iniciante | **Tempo estimado:** 15 minutos

---

## 🎯 Objetivo

Criar um projeto do zero, salvar três versões diferentes e ver o histórico de alterações.

---

## 📋 O que você vai praticar

- `git init` — iniciar um repositório
- `git add` — marcar arquivos
- `git commit` — salvar uma versão
- `git log` — ver o histórico

---

## 🚶 Passo a passo

### Parte 1 — Criar o projeto

1. Crie uma pasta chamada `diario-git` em qualquer lugar do seu computador
2. Abra o terminal dentro dessa pasta
3. Rode o comando abaixo para iniciar o repositório:

```
git init
```

✅ **Resultado esperado:** uma mensagem dizendo que o repositório foi criado.

---

### Parte 2 — Criar o primeiro arquivo

1. Dentro da pasta, crie um arquivo chamado `diario.txt`
2. Escreva dentro dele:

```
Dia 1: Aprendi a usar o Git hoje!
```

3. Salve o arquivo e volte ao terminal
4. Veja o status:

```
git status
```

> Você verá `diario.txt` em vermelho — ele ainda não foi marcado.

5. Marque o arquivo:

```
git add diario.txt
```

6. Salve a primeira versão:

```
git commit -m "criei o diário"
```

✅ **Resultado esperado:** mensagem confirmando o commit.

---

### Parte 3 — Fazer alterações e salvar mais versões

**Segunda entrada:**

1. Abra `diario.txt` e adicione uma nova linha:

```
Dia 2: Aprendi o comando git add e git commit.
```

2. Salve e rode:

```
git add diario.txt
git commit -m "adicionei o dia 2"
```

---

**Terceira entrada:**

1. Adicione mais uma linha no arquivo:

```
Dia 3: Agora sei ver o histórico com git log!
```

2. Salve e rode:

```
git add diario.txt
git commit -m "adicionei o dia 3"
```

---

### Parte 4 — Ver o histórico

Rode o comando:

```
git log --oneline
```

✅ **Resultado esperado:** você verá algo parecido com isso:

```
a3f9c12  adicionei o dia 3
b1e4d08  adicionei o dia 2
c9a2f77  criei o diário
```

Cada linha é uma versão salva, da mais recente para a mais antiga.

---

## 🏆 Desafio extra

Adicione um segundo arquivo chamado `notas.txt` com qualquer conteúdo, marque e salve com a mensagem `"adicionei arquivo de notas"`.

Depois rode `git log --oneline` e confirme que aparecem 4 commits no total.

---

## ✅ Checklist de conclusão

- [ ] Rodei `git init` e o repositório foi criado
- [ ] Criei `diario.txt` e fiz o primeiro commit
- [ ] Fiz mais dois commits com novas entradas
- [ ] Rodei `git log --oneline` e vi os 3 commits
- [ ] (Extra) Adicionei `notas.txt` e fiz o 4º commit

---

> 💡 **Dica:** se travar em qualquer etapa, rode `git status` — ele sempre te diz o que está acontecendo e o que fazer a seguir.