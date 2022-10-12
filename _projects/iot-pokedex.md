---
title: IoT Pokédex
layout: single
permalink: /projects/iot-pokedex/

---

This is a project for one of my classes. The goal of this project was to implement a simple puzzle, sort of like an escape room game, nothing fancy since it is a first-year project, meant to give us a taste of embedded software programming. However, my partner and I went above and beyond and implemented a pokédex, an encyclopedia for pokémon, a popular Nintendo video game franchise.

The board we used was an STM32 Nucleo board, we also used many other components, such as a Wi-Fi card, a keypad, and an LCD screen.

This device works by taking a user input and then using the value entered to send an API request to <a href="https://pokeapi.co/"> pokeapi </a>, an API containing information of all Pokémons, then parse the API response and output it to the screen. 

Since it involves API calls, naturally, we would need access to the internet, and this is the first major challenge we encountered. We had to open a second USART on the board to send and receive data from the Wi-Fi module. Once we figured that out, the next challenge is that the JSON string returned from the API is way bigger than the available memory on the STM32 board, so we end up setting up a proxy server in Python on my computer, which will handle the API call and format the string so that it could fit into our microcontroller. To do that, we created a socket to send/receive information from and to the board. 

The LCD screen is another challenge we faced, we had to do some extra hardware initialization for it to work properly on our board. Even though we found a library online to control the screen, we still had some weird bugs, for example, the text would not display properly on it. In the end, we managed to track down the issue and found a workaround. 

In general, this project was an awesome learning experience as we really challenged ourselves and forced ourselves to learn a lot more new things, such as making API calls, opening a socket, controlling LCD screens and Wi-Fi cards, etc. 

Below is a video demonstrating our project:
{% include video id="dSsDeBJaxFQ" provider="youtube" %}