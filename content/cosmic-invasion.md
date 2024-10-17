---
title: 🚀 Criei um jogo com uma experiência integrada ao celular
description: Uma experiência de jogo inovadora que transforma seu celular em um joystick para controlar uma nave espacial.
date: 2024-10-10
draft: false
tags:
  - jogos
  - backend
  - desenvolvimento
  - programação web
aliases:
  - jogo de nave espacial
  - controle via celular
  - jogo com QR code
---

![Imagem do Jogo: Cosmic Invasion](./static/images/cosmic-invasion.png)

Fala, Devs! Como estão?

Passei aqui para contar um pouco sobre um projeto pessoal que tem me animado bastante: o **Cosmic Invasion**. É um jogo de nave espacial 2D com uma pegada um pouco diferente — nele, o seu celular vira o joystick! Achei que seria interessante compartilhar um pouco dessa jornada, desde a ideia até as escolhas de tecnologia.

#### Sobre o Projeto

**Cosmic Invasion** é simples e direto: você controla uma nave e precisa derrotar os aliens antes que o tempo acabe. A diversão está em poder usar o celular como controle — para isso, é só escanear o QR code na tela inicial, e pronto! O celular se transforma no seu joystick, deixando a experiência ainda mais imersiva.

Usei **JavaScript, HTML, CSS, Node.js, Express,** e **Socket.io** para desenvolver o jogo. Uma das maiores "dores de cabeça" foi criar um sistema de ID único para conectar o jogo no PC ao joystick no celular de forma segura. Mas valeu a pena, pois o resultado foi uma jogabilidade bem fluida.

Escolhi o **Render** para hospedar o projeto. Na versão gratuita, ele tem um porém: o servidor hiberna depois de um tempo sem uso, então quando alguém acessa o jogo novamente, rola uma espera de mais ou menos um minuto para tudo voltar a funcionar. Não é o ideal, mas foi uma solução viável para colocar o jogo no ar sem custos.

#### Quer Contribuir?

O projeto está lá no [GitHub](https://github.com/CarlosEduts/Cosmic-Invasion), caso alguém queira explorar ou contribuir. E se você quiser testar o Cosmic Invasion, é só acessar: **[cosmicinvasion.onrender.com](https://cosmicinvasion.onrender.com)**.

Valeu por ler até aqui! Espero que curtam o jogo, e até a próxima!
