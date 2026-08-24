<div align="center"> <pre> 
 _____       _   _ ___________  _____ _____ 
/  __ \     | | | |  ___| ___ \/  ___|  ___|
| /  \/_____| | | | |__ | |_/ /\ `--.| |__  
| |  |______| | | |  __||    /  `--. \  __| 
| \__/\     \ \_/ / |___| |\ \ /\__/ / |___ 
 \____/      \___/\____/\_| \_|\____/\____/ 
</pre>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=00FF9C&center=true&vCenter=true&width=440&lines=light-weight;functional;for+indie+developers.)](https://git.io/typing-svg)

</div>

## `> What is this?`

C-Verse is a lightweight, open-source physics engine being built for indie game developers.

The goal is simple:

**give a game developer the physics they need without giving them an entire universe of engine machinery they don't.**

C-Verse is being developed from scratch in C++ as an exploration of physics simulation, numerical methods, collision detection, rigid-body dynamics, and the engineering required to turn mathematical models into something a game can actually use.

It is not trying to be the biggest physics engine.

It is trying to be a useful one.

---

## `> The Idea`

A physics engine ultimately does something rather strange.

You give it a collection of objects.

You give those objects properties.

You give the world forces and constraints.

Then, repeatedly:

```text
                 WORLD
                   │
                   ▼
          ┌─────────────────┐
          │     FORCES      │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │    INTEGRATE    │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │    COLLISION    │
          │    DETECTION    │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │    COLLISION    │
          │    RESPONSE     │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │     UPDATE      │
          │      WORLD      │
          └────────┬────────┘
                   │
                   └───────────┐
                               │
                               ▼
                            NEXT STEP
```

Then you do it again.

And again.

And again.

At some point, the square stops falling through the floor.

That is the general idea.

---

## `> Design Goals`

C-Verse is being built around a few constraints.

```text
             C-VERSE
                │
       ┌────────┼────────┐
       ▼        ▼        ▼
    LIGHTWEIGHT SIMPLE  USEFUL
       │        │        │
       ▼        ▼        ▼
    small      clear    games
    runtime    API      first
```

### Lightweight

C-Verse should be practical for small games and projects where a full engine dependency would be unnecessary.

### Understandable

The implementation should remain readable enough that someone can actually study how the simulation works.

### Modular

Collision detection should not be welded permanently to rendering.

The physics world should not care which graphics API a game uses.

The engine should provide the machinery and let the game decide what to do with it.

### Game-oriented

This is ultimately a game physics engine.

Mathematical correctness matters.

So does making the API pleasant to use.

---

## `> What C-Verse Will Handle`

The engine is being developed around the fundamental pieces of a rigid-body physics system.

```text
PHYSICS
│
├── Mathematics
│   ├── Vectors
│   ├── Matrices
│   ├── Transforms
│   └── Numerical utilities
│
├── World
│   ├── Bodies
│   ├── Forces
│   ├── Gravity
│   └── Simulation
│
├── Collision
│   ├── Shapes
│   ├── Broad phase
│   ├── Narrow phase
│   ├── Contact generation
│   └── Collision response
│
├── Dynamics
│   ├── Linear motion
│   ├── Angular motion
│   ├── Mass
│   ├── Inertia
│   └── Integration
│
└── Constraints
    ├── Contacts
    ├── Friction
    └── Joints
```

The exact architecture will evolve as the implementation exposes where the mathematics and engineering disagree.

They tend to do that.

---

## `> Development`

C-Verse is being built from the bottom up.

The implementation will begin with the mathematical machinery before moving into increasingly complex simulation systems.

```text
[✓] Project structure
[ ] Vector mathematics
[ ] Transforms
[ ] Rigid bodies
[ ] Forces
[ ] Integration
[ ] Basic shapes
[ ] Collision detection
[ ] Collision response
[ ] Friction
[ ] Constraints
[ ] Broad-phase detection
[ ] Joints
[ ] Spatial partitioning
[ ] Performance optimisation
[ ] Documentation
[ ] Examples
```

The checklist will probably become more ambitious.

The laws of physics remain annoyingly indifferent to project scope.

---

## `> Why Build Another Physics Engine?`

There are already excellent physics engines.

That is not really the point.

C-Verse exists because building a physics engine is an unusually good way to understand several areas of computer science and game development at once:

* linear algebra
* numerical integration
* geometry
* collision detection
* simulation
* data structures
* performance engineering
* memory management
* API design

The objective is not to compete with mature physics middleware immediately.

The objective is to understand the machinery well enough to build one.

If it eventually becomes useful to someone else's game, even better.

---

## `> License`

C-Verse is open source and will be released under the MIT License.

---
<div align="center">

C-Verse is a work in progress.

Build the simulation.

Understand the machinery.

Then make something move.

</div>
