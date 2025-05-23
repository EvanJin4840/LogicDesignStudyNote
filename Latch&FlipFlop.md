# Latch
- a latch is a basic memory element that can store one bit of information.
- It is a type of sequential circuit because its output depends not only on current inputs but also on past states.

* Key Features of a Latch

| Feature             | Description                                                         |
| ------------------- | ------------------------------------------------------------------- |
| **Stores**          | 1-bit of data (0 or 1)                                              |
| **Control**         | Controlled by an **enable** signal, not a clock                     |
| **Memory**          | Yes – retains its state when inputs are inactive                    |
| **Level-sensitive** | Reacts to input when **enable is HIGH or LOW**, depending on design |

## Types of Latches
| Type                     | Description                                 |
| ------------------------ | ------------------------------------------- |
| **SR Latch** (Set-Reset) | Most basic type using NOR or NAND gates     |
| **D Latch** (Data latch) | Stores data input `D` when `Enable` is HIGH |

### SR Latch Overview
| Input         | Function                    |
| ------------- | --------------------------- |
| **Set (S)**   | Forces the output **Q = 1** |
| **Reset (R)** | Forces the output **Q = 0** |

-> The SR latch "remembers" the output until S or R is activated again.

* Basic SR Latch with NOR gates
| S | R | Q (Output)    | Q̅ (Complement) | Meaning                       |
| - | - | ------------- | --------------- | ----------------------------- |
| 0 | 0 | **No change** | No change       | Holds previous value          |
| 1 | 0 | 1             | 0               | **Set**                       |
| 0 | 1 | 0             | 1               | **Reset**                     |
| 1 | 1 | ❌ Invalid     | ❌ Invalid       | **Not allowed** (both active) |

### Sequential circuit
- A sequential circuit is a type of digital circuit in which the output depends not only on the current inputs, but also on the past history of inputs — that is, its previous state.

* Key characteristics of Sequential Circuits

| Feature    | Description                                                          |
| ---------- | -------------------------------------------------------------------- |
| **Memory** | Yes – stores past states using flip-flops or latches                 |
| **Output** | Depends on **current input + stored state**                          |
| **State**  | Changes at each clock pulse (usually)                                |
| **Timing** | Often synchronized with a clock (in synchronous sequential circuits) |

### Difference between a level and an edge

- A level = the signal is held at a constant 1 (HIGH) or 0 (LOW)

- An edge = the signal changes from 0 → 1 (rising edge) or 1 → 0 (falling edge)

# 동기 및 비동기 시스템

1. 비동기(Asynchronous) 시스템:
각 부품이 자기 멋대로 동작 시간 가짐

누군가는 빨리 반응하고, 누군가는 늦게 반응

결과적으로 타이밍 오류(glitch) 발생 가능

⏰ 2. 동기(Synchronous) 시스템:
모든 부품이 같은 clock 신호에 맞춰서 딱딱 움직임

예: 모든 flip-flop이 clock의 rising edge에만 상태 변경

→ 결과: 안정적이고 예측 가능한 동작

