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
2. Utilise o Vscode (abrir a pasta  `diario-git` e selecione no menu terminal), ou utilise o terminal (abra o terminal dentro dessa pasta)
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
Dia 1: Minha primeira tarefa como dev.
```

3. Salve o arquivo e volte ao terminal
4. Veja o status:

```
git status
```

o Git “viu mudanças, mas não foi avisado”
É como escrever algo no git e não apertar salvar.

> Você verá `diario.txt` em vermelho — ele ainda não foi salvo mas estã sendo supervisionado.

5. Marque o arquivo:

Aqui você escolheu exatamente o que quer salvar

```
git add diario.txt
```


6. Salve a primeira versão:

Agora será realmente salvo e entrará no histórico do projeto

```
git commit -m "primeira tarefa"
```

✅ **Resultado esperado:** mensagem confirmando o commit.

---

### Parte 3 — Fazer alterações e salvar mais versões

**Segunda entrada:**

1. Abra `diario.txt` e adicione uma nova linha:

```
Dia 2: Minha segunda tarefa como dev.
```

2. Salve e rode:

```
git add diario.txt
git commit -m "segunda tarefa"
```

---

**Terceira entrada:**

1. Adicione mais uma linha no arquivo:

```
Dia 3: Minha terceira tarefa como dev
```

2. Salve e rode:

```
git add diario.txt
git commit -m "terceira tarefa"
```

---

### Parte 4 — Ver o histórico

Rode o comando:

```
git log --oneline
```

✅ **Resultado esperado:** você verá algo parecido com isso:

```
a3f9c12  terceira tarefa
b1e4d08  segunda tarefa
c9a2f77  primeira tarefa
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