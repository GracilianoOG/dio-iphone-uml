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
        -Musica musicaAtual
        -List~Musica~ listaMusicas

        +void tocar()
        +void pausar()
        +void continuar()
        +void aumentarVolume()
        +void diminuirVolume()
        +void mudarVolume(int volume)
        +void adicionarMusica(Musica musica)
        +void deletarMusica(String titulo)
        +void selecionarMusica(String titulo)
        +void exibirMusicaAtual()
    }

    class AparelhoTelefonico {
        -boolean emLigacao
        -boolean estaTocando
        -List~Contato~ contatos

        +void ligar(String numero)
        +void desligar()
        +void atender()
        +void recusar()
        +void adicionarContato(Contato contato)
        +void deletarContato(String numero)
        +void iniciarCorreioVoz()
    }

    class NavegadorInternet {
        -Aba abaAtual
        -List~Aba~ abas

        +void exibirPagina(String url)
        +void adicionarNovaAba()
        +void atualizarPagina()
        +void exibirAbas()
    }

    class Musica {
        -String titulo
        -String artista
        -int duracao
    }

    class Contato {
        -String nome
        -String email
        -List~String~ telefones
    }

    class Aba {
        -String titulo
        -String url
    }

    iPhone --> ReprodutorMusical
    iPhone --> AparelhoTelefonico
    iPhone --> NavegadorInternet
    ReprodutorMusical --> Musica : tem
    AparelhoTelefonico --> Contato : tem
    NavegadorInternet --> Aba : tem
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

Um candidato pode possuir um ou mais telefones, mas não é dependente de um telefone em sua criação. Essa é uma forma mais simples de representação.

```mermaid
    classDiagram
        direction LR
        class Candidato {
        }

        class Telefone {
        }

        Candidato --> "1..*" Telefone : tem
```

### Agregação

Um candidato pode ter uma profissão, mas não é obrigatório em sua criação. É possível informar isso em um outro momento. Um podem existir sem a necessidade do outro ser criado. A destruição de um não afeta o outro.

```mermaid
    classDiagram
        direction LR
        class Candidato {
        }

        class Profissao {
        }

        Candidato o--> Profissao : tem
```

### Composição

Uma casa (todo) é composta por um ou mais quartos (partes). Os quartos só podem existir dentro da Casa. A destruição da casa resulta também na destruição dos quartos.

```mermaid
    classDiagram
        direction LR
        class Casa {
        }

        class Quarto {
        }

        Casa "1" *--> "1..*" Quarto : possui
```

## 🧑🏻‍💻 Autor

- [GitHub](https://github.com/GracilianoOG)
- [LinkedIn](https://www.linkedin.com/in/gabrielgmbarros)
- [Frontend Mentor](https://www.frontendmentor.io/profile/GracilianoOG)