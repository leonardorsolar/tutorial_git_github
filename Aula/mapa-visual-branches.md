# 🗺️ Mapa Visual: o que acontece com as branches

> Este arquivo mostra **visualmente** o que o Git está fazendo em cada etapa do exercício.
> Leia junto enquanto executa os comandos.

---

## Estado 1 — Depois do primeiro commit

Você só tem a `main`. Um único ponto na linha do tempo.

```
main
 │
 ●  "versão inicial do cardápio"
    📄 cardapio.txt  ✔
    📄 sobre.txt     ✔
```

---

## Estado 2 — Depois de `git switch -c novo-prato`

O Git criou uma **cópia paralela** que parte do mesmo ponto.
Os dois arquivos existem nas duas branches — idênticos por enquanto.

```
main           novo-prato
 │               │
 ●───────────────●   (mesmo ponto de partida)
    📄 cardapio.txt  ← igual nas duas
    📄 sobre.txt     ← igual nas duas

                 ▲
           você está aqui
```

---

## Estado 3 — Depois do commit na `novo-prato`

A branch `novo-prato` avançou. A `main` ficou parada.
São duas linhas do tempo diferentes agora.

```
main           novo-prato
 │               │
 ●               ●  "adicionei lasanha ao cardápio"
                    📄 cardapio.txt  ← tem a lasanha
                    📄 sobre.txt     ← igual

 ▲
main não
mudou nada
```

---

## Estado 4 — Depois de `git switch main`

Você voltou para a `main`. O Git trocou os arquivos da pasta.

```
main           novo-prato
 │               │
 ●               ●  "adicionei lasanha ao cardápio"
 ▲
você está aqui
📄 cardapio.txt  ← SEM a lasanha
📄 sobre.txt     ← igual
```

> É por isso que a lasanha "sumiu" quando você abriu o arquivo.
> Ela não foi apagada — só está em outra linha do tempo.

---

## Estado 5 — Depois de `git merge novo-prato`

O Git **juntou** as duas linhas. A lasanha entrou na `main`.
A branch `novo-prato` ainda existe, mas já cumpriu seu papel.

```
main
 │
 ●  "versão inicial do cardápio"
 │
 │         novo-prato
 │          │
 │          ●  "adicionei lasanha"
 │          │
 └──────────┘
      │
      ●  ← merge! tudo junto agora
         📄 cardapio.txt  ← COM a lasanha
         📄 sobre.txt     ← igual
```

---

## Estado 6 — Depois de `git branch -d novo-prato`

A branch foi removida. O histórico continua intacto na `main`.

```
main
 │
 ●  "versão inicial do cardápio"
 │
 ●  "adicionei lasanha ao cardápio"  ← veio do merge
    📄 cardapio.txt  ✔
    📄 sobre.txt     ✔
```

---

## 🧠 Regra de ouro

```
┌─────────────────────────────────────────────────┐
│  Nunca trabalhe direto na main.                  │
│  Crie uma branch → experimente → merge se OK.   │
└─────────────────────────────────────────────────┘
```

Isso é exatamente o que times profissionais fazem todos os dias.

---

