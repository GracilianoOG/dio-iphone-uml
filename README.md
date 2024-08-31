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

## 🧑🏻‍💻 Autor

- [GitHub](https://github.com/GracilianoOG)
- [LinkedIn](https://www.linkedin.com/in/gabrielgmbarros)
- [Frontend Mentor](https://www.frontendmentor.io/profile/GracilianoOG)