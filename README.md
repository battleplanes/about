What is this?
=============

Battleplanes is a game similar to battleships, but more challenging on
several fronts.

The Battleplanes Project
========================

The purpose of the battleplanes project is to serve as:

* a playground for learning new languages and technology stacks
* a template for other projects
* evaluating programming languages and technology stacks

It was chosen because the game is simple enough to be programmed in a short
timespan by an experienced programmer, and in a manageable time by novice
programmers under guidance.

At the same time, the game poses some interesting challenges both in terms of
algorithms, as well as software design and using the ecosystem around an
existing technology stack.

There are various implementations of battleplanes, in different programming
languages, using different frameworks and libraries.

The battleplanes/about Project
==============================

This `about` project serves as a coordination hub among all other projects,
making sure that they all implement the same game, and keeping track of common
issues across all implementations.

This project will also outline in a standardized format some differences
between languages and technology stacks, statistics like bugs / tickets, etc.

How the Game is Played
======================

The aim is to kill your opponent's planes first. Each player positions three
planes on his board. Planes can be oriented in any of the four directions, but
they are not allowed to overlap or to fall even partially off the map.

A plane is considered killed when its cockpit is hit. When aiming at a tile,
your opponent tells you whether you have a *hit*, a *miss* or a *kill*. No
other information is exchanged.

Once a plane has been killed, the tiles where the killed plane used to be count
now as *misses*.

[Detailed game play](Gameplay.md)

Development
===========

Anyone can write an implementation of battleplanes using any technology she/he
wants. There are several non-functional criterias which must be fulfilled by
all implementations:

* the core of the game, containing the logic, must be isolated in its own
  module, using tools and techniques specific to the language / ecosystem
  chosen for implementation (a C/C++ .dll/.so, a Java .jar, a Rust crate,
  a PSR-4 compliant PHP composer module in its own namespace, etc)
* There are different interfaces to the game, which are packaged separately:
  console, web, native GUIs, OpenGL interfaces, etc.
* For web interfaces, the implementation is split in two separate programs: the
  frontend and the backend
* The backend for a web deployment implements REST endpoints for all
  operations, and provides a basic UI for playing the game
* Any frontend web program can be paired with any backend server, with no or
  minimal modifications
* Other features like persistence should be modular and easily swappable

Further non-functional criterias will be identified over time. They may include
features like documentation, testing, performance, high availability
/ distributed systems, security, etc.

Some functional features may include:

* AI levels
* human agains human
* tournaments

Implementation Roadmap
----------------------

All battleplanes implementations follow a certain development timeline: at each
tagged version (`v0.2`, `v0.4`, `v0.6`, `v0.8`, `v1.0`, ...).

License
=======

Public Domain

All battleplanes implementations are licensed under the public domain.
