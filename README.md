[![Build Status](https://travis-ci.com/UNIZAR-30246-WebEngineering/lab4-websockets.svg?branch=master)](https://travis-ci.com/UNIZAR-30246-WebEngineering/lab4-websockets)
# Web Engineering 2020-2021 / Websockets
**In this assignment your PR must only modify the `README.md` file**.
Please, go to the [Wiki](https://github.com/UNIZAR-30246-WebEngineering/lab4-websockets/wiki) in order to get the instructions for this assignment.

## Historical background

The code implements the script DOCTOR of the [ELIZA](https://en.wikipedia.org/wiki/ELIZA) system and provides you a client and server that communicate each other by means of websockets. 
ELIZA is an early example of primitive natural language processing developed by [Joseph Weizenbaum](https://en.wikipedia.org/wiki/Joseph_Weizenbaum) between 1964 and 1966. 
ELIZA operated by processing users' responses to scripts, the most famous of which was DOCTOR, a simulation of a [Rogerian psychotherapist](https://en.wikipedia.org/wiki/Person-centered_therapy). 
Using almost no information about human thought or emotion, DOCTOR sometimes provided a startlingly human-like interaction.

## Primary goal

The objective is to complete `ElizaServerTest.java` by completing the test `onChat` that now is ignored. 
The `onChat` test must:
* Send a message from the client to the server that is running a Java implementation of the script DOCTOR.
* Check the client receives a DOCTOR question about your mental health (see examples in `Eliza.java`). 

You must remove `@Ignore` and place up to 6 lines of code to fulfil the task. 
The location of `Complete Me!!` is just a hint, but there are many possible solutions and locations.
`ElizaServerTest.java` includes the test `onOpen` that will provide you insights. 

## Secondary goals (:gift:)

Solutions must meet primary goals too. 

Done:

- [Turn the DOCTOR into a client of the server, so, the server acts only as message broker](https://github.com/rauljavierre/lab4-websockets/tree/test). Raul Javierre ha comprobado que cuando el servidor actua como un message broker elaborar un mini subprotocolo ayuda a la hora de organizar la comunicación y facilitar la escalabilidad :gift:
- [Replace the current implementation (Eclipse Grizzly) by a Spring Websockets implementation](https://github.com/Alvarogd6/lab4-websockets/tree/gift). Alvaro García ha podido migrar la plataforma del servidor de Grizzly a Spring usando un TextWebSocketHandler. Lección aprendida, cuando hay un marco compartido bien definido (ver [JSR 356](https://jcp.org/en/jsr/detail?id=356)) las implementaciones pueden parecer muy diferentes, pero enseguida se ve qué se relaciona con qué. : gift: 

Proposed:

- Support STOMP in the server side and create a small client that uses it
- Support SockJS in the server side and show that xhr-polling can be used as transport instead of WebSocket when needed ([additional info](https://docs.spring.io/spring-framework/docs/current/reference/html/web.html#websocket-fallback-sockjs-client))
- Use the server as a relay server to connect to an external message broker (e.g. RabbitMQ, [additional info](https://docs.spring.io/spring-framework/docs/current/reference/html/web.html#websocket-stomp-handle-broker-relay)) 

Note: unless the goal specifies o disallows a specific framework you are free to replace the framework used in the original implementation with a different framework.

Manifest your intention first by a PR updating this `README.md` with your goal.
If you desist of your goal, release it by a PR so other fellow can try it. 

| NIA    | User name | Repo | Build Status | Improvement | Score
|--------|-----------|------|--------------|-------------|--------
| 760704 |[Álvaro García](https://github.com/Alvarogd6)|[Alvarogd6/lab4-websockets](https://github.com/Alvarogd6/lab4-websockets/tree/test)|![Build Status](https://travis-ci.com/Alvarogd6/lab4-websockets.svg?branch=test)|Replace the current implementation (Eclipse Grizzly) by a [Spring Websockets](https://docs.spring.io/spring-framework/docs/current/reference/html/web.html#websocket) implementation| :gift:
| 758906 |[Raúl Javierre](https://github.com/rauljavierre)|[rauljavierre/lab4-websockets](https://github.com/rauljavierre/lab4-websockets/tree/test)|![Build Status](https://travis-ci.com/rauljavierre/lab4-websockets.svg?branch=test)|Turn the DOCTOR into a client of the server, so, the server acts only as message broker| :gift:
| 757153 |[Fran Morés](https://github.com/Fran-sw) |[Fran-sw/lab4-websockets](https://github.com/Fran-sw/lab4-websockets/tree/test)      |![Build Status](https://travis-ci.com/Fran-sw/lab4-websockets.svg?branch=test)| |                      |
| 758803 |[Daniel González](https://github.com/Uncastellum/) |[Uncastellum/lab4-websockets](https://github.com/Uncastellum/lab4-websockets/tree/test)      |![Build Status](https://travis-ci.com/Uncastellum/lab4-websockets.svg?branch=test)| |                      |
| 757715 |[Hayk kocharyan](https://github.com/hayk99) |[hayk99/lab4-websockets](https://github.com/hayk99/lab4-websockets/tree/test)      |![Build Status](https://travis-ci.com/hayk99/lab4-websockets.svg?branch=test)| |                      |
| 758267 |[Pedro Allué](https://github.com/piter1902) |[piter1902/lab4-websockets](https://github.com/piter1902/lab4-websockets/tree/test)      |![Build Status](https://travis-ci.com/piter1902/lab4-websockets.svg?branch=test)| |                      |
| 739202 |[Luis Garcia](https://github.com/luisgg98) |[luisgg98/lab4-websockets](https://github.com/luisgg98/lab4-websockets/tree/test)      |![Build Status](https://travis-ci.com/luisgg98/lab4-websockets.svg?branch=test)| |                      |
| 755742 |[Juan José Tambo](https://github.com/jtambo99) |[jtambo99/lab4-websockets](https://github.com/jtambo99/lab4-websockets/tree/test)      |![Build Status](https://www.travis-ci.com/jtambo99/lab4-websockets.svg?branch=test)| |                      |
| 761319 |[Marcos Nuez](https://github.com/Markles01) |[Markles01/lab4-websockets](https://github.com/Markles01/lab4-websockets/tree/test)      |![Build Status](https://travis-ci.com/Markles01/lab4-websockets.svg?branch=test)| |                      |
| 766685 |[Enrique Ruiz Flores](https://github.com/TheRealFreeman)|[TheRealFreeman/lab4-websockets](https://github.com/TheRealFreeman/lab4-websockets/tree/test)|![Build Status](https://travis-ci.com/TheRealFreeman/lab4-websockets.svg?branch=test)| |                      |
| 756123 |[Rogelio Lacruz](https://github.com/RogorStuff)|[RogorStuff/lab4-websockets](https://github.com/RogorStuff/lab4-websockets/tree/test) |[![Build Status](https://travis-ci.org/RogorStuff/lab4-websockets.svg)](https://travis-ci.org/RogorStuff/lab4-websockets)| |                      |
| 740491 |[José Ignacio Hernández](https://github.com/740491)|[740491/lab4-websockets](https://github.com/740491/lab4-websockets/tree/test)| ![Build Status](https://travis-ci.com/740491/lab4-websockets.svg?branch=test)|  |
| 760739 |[Alberto Calvo Rubió](https://github.com/AlbertoCalvoRubio)|[AlbertoCalvoRubio/lab4-websockets](https://github.com/AlbertoCalvoRubio/lab4-websockets/tree/test)|[![Build Status](https://travis-ci.com/AlbertoCalvoRubio/lab4-websockets.svg?branch=test)](https://travis-ci.com/AlbertoCalvoRubio/lab4-websockets)|  | |
| 738233 |[Sergio Torres](https://github.com/cul3bro)|[740491/lab4-websockets](https://github.com/cul3bro/lab4-websockets/tree/test)| ![Build Status](https://travis-ci.com/cul3bro/lab4-websockets.svg?branch=test)|  |
| 761754 |[David Alloza](https://github.com/david-AT)|[david-AT/lab4-websockets](https://github.com/david-AT/lab4-websockets/tree/test)| ![Build Status](https://travis-ci.com/david-AT/lab4-websockets.svg?branch=test)|  |
| 739324 |[Elena Morón Vidal](https://github.com/elenamv13)|[elenamv13/lab4-websockets](https://github.com/elenamv13/lab4-websockets/tree/test)| ![Build Status](https://travis-ci.com/elenamv13/lab4-websockets.svg?branch=test)|  |
| 758635 |[Daniel Huici Meseguer](https://github.com/Kifixo)|[Kifixo/lab4-websockets](https://github.com/Kifixo/lab4-websockets/tree/test)| ![Build Status](https://travis-ci.com/Kifixo/lab4-websockets.svg?branch=test)|  |
| 756308 |[Álvaro Santamaría](https://github.com/SanTa45zgz)|[SanTa45zgz/lab4-websockets](https://github.com/SanTa45zgz/lab4-websockets/tree/test)| ![Build Status](https://travis-ci.com/SanTa45zgz/lab4-websockets.svg?branch=test)|  |
| 756308 |[Eduardo Ruiz](https://github.com/eduardoRuizC)|[SanTa45zgz/lab4-websockets](https://github.com/eduardoRuizC/lab4-websockets/tree/test)| ![Build Status](https://api.travis-ci.com/eduardoRuizC/lab4-websockets.svg?branch=test)|  |
| 738845 |[Víctor Martínez](https://github.com/viriannn)|[viriannn/lab4-websockets](https://github.com/viriannn/lab4-websockets/tree/test)| ![Build Status](https://travis-ci.com/viriannn/lab4-websockets.svg?branch=test)|  |
