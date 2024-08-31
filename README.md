# 💻 Desafio: POO

## 🎯 Desafio

Funcionalidades a Modelar

1. Reprodutor Musical
    - Métodos: `tocar()`, `pausar()`, `selecionarMusica(String musica)`
2. Aparelho Telefônico
    - Métodos: `ligar(String numero)`, `atender()`, `iniciarCorreioVoz()`
3. Navegador na Internet
    - Métodos: `exibirPagina(String url)`, `adicionarNovaAba()`, `atualizarPagina()`

## 📌 Diagrama (Mermaid)

```mermaid
classDiagram
    direction TB

    class iPhone {

    }

    class ReprodutorMusical {
        -boolean estaTocando
        -int volume
        -String musicaAtual
        +void tocar()
        +void pausar()
        +void aumentarVolume()
        +void diminuirVolume()
        +void mudarVolume(int volume)
        +void selecionarMusica(String musica)
        +void exibirMusicaAtual()
    }

    class AparelhoTelefonico {
        -boolean emLigacao
        -boolean estaTocando
        +void ligar(String numero)
        +void desligar()
        +void atender()
        +void recusar()
        +void iniciarCorreioVoz()
    }

    class NavegadorInternet {
        +void exibirPagina(String url)
        +void adicionarNovaAba()
        +void atualizarPagina()
    }

    iPhone --> ReprodutorMusical
    iPhone --> AparelhoTelefonico
    iPhone --> NavegadorInternet
```

## 🧱 Ferramentas utilizadas

- `Mermaid`
- `Visual Studio Code`

## 🛠️ Links úteis

- [DIO](https://www.dio.me/)
- [Repositório do desafio](https://github.com/digitalinnovationone/trilha-java-basico/tree/main/desafios/poo)
- [Documentação Mermaid](https://mermaid.js.org/syntax/classDiagram.html)
- [Direções com Mermaid](https://jojozhuang.github.io/tutorial/mermaid-cheat-sheet/)

## 📓 Anotações

### Associação simples (agregação por padrão)

Um candidato pode possuir um ou mais telefones, mas não é dependente de um telefone em sua criação.

```mermaid
    classDiagram
        direction LR
        class Candidato {
        }

        class Telefone {
        }

        Candidato --> "1..*" Telefone
```

### Agregação

Um candidato pode ter uma profissão, mas não é obrigatório em sua criação. É possível informar isso em um outro momento.

```mermaid
    classDiagram
        direction LR
        class Candidato {
        }

        class Profissao {
        }

        Candidato --o Profissao
```

### Composição

Um item de menu **deve** ter um produto vinculado para que possa fazer sentido, logo, é obrigatório.

```mermaid
    classDiagram
        direction LR
        class ItemMenu {
        }

        class Produto {
        }

        ItemMenu --* Produto
```

## 🧑🏻‍💻 Autor

- [GitHub](https://github.com/GracilianoOG)
- [LinkedIn](https://www.linkedin.com/in/gabrielgmbarros)
- [Frontend Mentor](https://www.frontendmentor.io/profile/GracilianoOG)