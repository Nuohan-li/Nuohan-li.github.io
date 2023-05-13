---
title: IoT Pokédex
layout: single
classes: wide
permalink: /projects/iot-pokedex/

---

This project was developed as part of a class assignment, aiming to implement a simple puzzle resembling an escape room game. Although it was a first-year project and not intended to be extravagant, my partner and I decided to go the extra mile and create a Pokédex—a comprehensive encyclopedia of Pokémon, a beloved Nintendo video game franchise.

To bring our project to life, we used an STM32 Nucleo board as the core component. Additionally, we incorporated various other elements, such as a Wi-Fi card, a keypad, and an LCD screen.

The device operates by taking user input, using the entered value to initiate an API request to the <a href="https://pokeapi.co/">pokeapi</a>. This API contains an extensive collection of information about all Pokémon. We then parse the API response and display the relevant details on the LCD screen.

As the project involved making API calls, a crucial requirement was access to the internet. This posed our initial major challenge. We needed to establish a secondary USART on the board to facilitate data transmission and reception with the Wi-Fi module. Once we resolved this hurdle, we encountered the issue of the JSON string returned from the API being larger than the available memory on the STM32 board. To overcome this, we devised a solution involving setting up a proxy server in Python on my computer. This server would handle the API call, format the string appropriately, and transmit it to our microcontroller via a socket connection.

Another challenge arose with the LCD screen. We encountered complications during its hardware initialization to ensure proper functionality on our board. Although we found a library online to control the screen, we encountered peculiar bugs, such as incorrect text display. After thorough investigation, we successfully identified the cause and implemented a workaround.

Overall, this project proved to be an invaluable learning experience. We pushed ourselves beyond our comfort zones and acquired new skills, including making API calls, establishing socket connections, controlling LCD screens, and integrating Wi-Fi cards.

For a demonstration of our project, please watch the video below:
{% include video id="dSsDeBJaxFQ" provider="youtube" %}