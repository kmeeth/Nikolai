# Nikolai
## A simple 2D game engine
### By Matija Kuprešanin

# 1. Goal
The goal of this engine is to loosely emulate the model of Gamemaker:Studio, but stripping it of redundant and/or limiting elements, with those being anything other than game objects, rooms and assets. Where GML and Gamemaker fail is the clutteredness of large projects created using them. Nikolai seeks to solve this by relying on C++ and default classes and/or namespaces to govern commonly required features such as file loading, input, collisions etc.

# 2. Dependencies
Nikolai will depend solely on SFML, as of yet. SFML will be used to play sounds, manage windows and display graphics.

# 3. The Model
There will be 4 classes essential to Nikolai. They will be absolutely required in order for Nikolai to work properly.
## 3.1. GameObject
GameObject is a virtual class that represents all entities that do something in the game. All GameObjects will have attributes, which are essentially variables of any type, including Resource references. They will also have behaviours, defining what happens in which event.
## 3.2 GameEvent
GameEvent is a virtual class that represents a certain event that causes some behaivours to happen in GameObjects. There will be default events, defined by Nikolai, and there can be custom events, defined by the user. Events are managed by Rooms.
## 3.3. Room
Room is a class that represents a virtual space where objects are located that manages their events and, therefore, behaviours. Rooms are, factually, what is being rendered when the game is rendered; rendering rooms means rendering the objects present in it.
## 3.4. Resource
Resource is a virtual class that represents anything that can be loaded from files and used in game (an asset). They can be default resources, like sounds or sprites, or they can be user defined. They can be loaded from both text and binary files.
