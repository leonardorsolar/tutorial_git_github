# 🌿 Exercício: Branches — duas versões ao mesmo tempo

**Nível:** Iniciante | **Tempo estimado:** 20 minutos

> Você vai trabalhar num site de cardápio. A versão principal está pronta.
> Você quer testar uma mudança **sem arriscar** o que já funciona.
> Para isso, vai criar uma **branch** — uma linha paralela do projeto.

---

## 💡 O que é uma branch?

Imagine que seu projeto é um livro.
A branch `main` é o livro original.
Quando você cria uma nova branch, é como fazer uma **fotocópia** do livro para rabiscar à vontade — sem tocar no original.

Se gostar do que fez: cola as páginas no original (`merge`).
Se não gostar: joga a cópia fora e o original continua intacto.

---

## 📁 Preparação

Crie uma pasta chamada `cardapio` e abra o terminal dentro dela.

```
git init
```

e depois 

```
git switch -c main
```
O que faz?
Cria uma nova branch chamada main e já entra nela.

switch = trocar de branch
-c = criar branch nova

comando versão nova: git switch -c main
Comando com versão antiga: git checkout -b main


---

## 📄 Criando os arquivos iniciais

Crie dois arquivos dentro da pasta:

**`cardapio.txt`**
```
=== Cardápio ===

- Pizza Margherita  R$ 35
- Hambúrguer Clássico  R$ 28
- Suco de Laranja  R$ 10
```

**`sobre.txt`**
```
Restaurante Bella Vista
Aberto de segunda a sábado, das 11h às 23h.
```

Agora salve tudo no Git:

```
git add cardapio.txt sobre.txt
git commit -m "versão inicial do cardápio"
```

✅ Você está na branch `main` com a versão oficial do site.

---

## 🌿 Criando uma branch para experimentar

Você quer adicionar um **prato novo** ao cardápio, mas não tem certeza ainda.
Crie uma branch separada para isso:


```
git switch -c novo-prato
```
ou versao antiga
```
git checkout -b novo-prato
```

> Isso cria a branch `novo-prato` **e já entra nela**.
> Pense que você acabou de abrir a fotocópia do livro.

Confirme em qual branch você está:

```
git branch
```

Você verá:

```
  main
* novo-prato
```

O `*` indica onde você está agora.

---

## ✏️ Fazendo mudanças na branch

Abra `cardapio.txt` e adicione uma linha no final:

```
=== Cardápio ===

- Pizza Margherita  R$ 35
- Hambúrguer Clássico  R$ 28
- Suco de Laranja  R$ 10
- Lasanha da Casa  R$ 42
```

Salve e faça o commit:

```
git add cardapio.txt
git commit -m "adicionei lasanha ao cardápio"
```

---

## 👀 Veja a mágica acontecer

Agora abra o arquivo `cardapio.txt` — a lasanha está lá.

Volte para a branch `main`:

```
git switch main
```
ou versao antiga

```
git checkout main
```

Abra `cardapio.txt` novamente.

**A lasanha sumiu.** O arquivo voltou exatamente como estava antes.
Você não perdeu nada — a lasanha ainda existe na branch `novo-prato`.

---

## 🔀 Decidiu? Faça o merge

Você gostou da lasanha e quer colocar na versão oficial.
Estando na branch `main`, rode:

```
git merge novo-prato
```

Abra `cardapio.txt` — a lasanha está de volta, agora na versão oficial.

---

## 🗑️ Limpeza (opcional)

Depois do merge, a branch `novo-prato` cumpriu seu papel.
Você pode apagá-la sem perder nada:

```
git branch -d novo-prato
```

---

## ✅ Checklist de conclusão

- [ ] Criei os dois arquivos e fiz o commit inicial na `main`
- [ ] Criei a branch `novo-prato` com `git checkout -b`
- [ ] Adicionei a lasanha e fiz o commit na nova branch
- [ ] Voltei para `main` e confirmei que a lasanha **não aparecia**
- [ ] Fiz o `git merge` e confirmei que a lasanha **voltou**

---

## 🏆 Desafio extra

Crie uma branch chamada `horario-novo`, abra `sobre.txt` e mude o horário para:

```
Aberto todos os dias, das 10h às 00h.
```

Faça o commit, volte para `main`, confirme que o horário antigo ainda está lá —
e aí decida: faz o merge ou descarta a branch?

Para descartar sem fazer merge:
```
git branch -D horario-novo
```

---

> 💡 **Resumo mental:**
> `main` = versão oficial |
> nova branch = espaço seguro para experimentar |
> `merge` = juntar de volta |
> `-d` = apagar branch usada

---

➡️ Veja também: [`mapa-visual-branches.md`](./mapa-visual-branches.md) para entender o que acontece por baixo dos panos.