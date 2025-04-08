📈 Order Flow Game Engine: Gamified Market Execution System

A first-of-its-kind gamified trading simulator and visualization system built in Unreal Engine 5.5, blending real-time market dynamics with shooter mechanics. The initial prototype is a shooter-based game where BID and ASK orders are visualized as interactive targets on opposing walls of a trading corridor. The player acts as a market participant, executing trades by shooting targets. This project explores a new visual and mechanical language for trading via real-time engagement and muscle-memory-based interaction.

🎯 Conceptual Theory: Gamified Market Interaction

Markets are traditionally visualized via 2D price charts or DOM/order book ladders. This project aims to reimagine these concepts in a 3D first/third-person interactive experience where:

ASK Orders are red targets on the right wall (representing open sell orders)

BID Orders are green targets on the left wall (representing open buy orders)

Shooting an ASK simulates a market buy (accepting the ask)

Shooting a BID simulates a market sell (accepting the bid)

Volume is visualized through stacked blocks (Minecraft-style), where each block represents 1 unit of volume

Stack destruction simulates liquidity depletion

All actions translate directly to trading concepts, allowing a user to intuitively understand execution timing, spread, order depth, and reaction.

🚀 Gameplay Prototypes & Modes

🔫 Phase 1 – Shooter Core (Initial Repo Build)

Engine: Unreal Engine 5.5

Template: First/Third-Person Shooter Blueprint/C++ Hybrid

Mechanics:

Left/Right Wall targets (BIDs and ASKs)

Stackable volume blocks (destroy 1 per shot)

SQLite-simulated order flow (randomized)

Score = PnL tracking (buy low, sell high)

🧠 Phase 2 – Advanced Simulation Modes

PvE Trading AI: Competing bots executing on the same field

Order Defense & Traps: Set stop limits, fake orders, hidden liquidity

Custom Orders: Shoot empty levels to place bids/asks (your color)

Market Construction: Minecraft-style block builds representing ladders

🏗 Future Game Types (Using Core Mechanics)

Tower Defense: Build order walls to defend against volatility

Trading Tetris: Execute into dynamic falling liquidity blocks

Algo Duel: Compete to fill orders and snipe each other's trades

Rogue Price Runner: Chase a price creature through obstacle order flow

📡 Data Flow Design

Primary Loop for Development:

Simulated Order Flow:

Generated & stored in SQLite local DB

Used to spawn targets in-game

Live Order Flow (Future):

API key input (crypto broker preferred)

API fetch → SQLite → Live target spawner

Gameplay Engine:

Player actions tracked (entries, exits, time, PnL)

All stored in local SQLite and pushed to cloud for analytics

Considerations:

Broker must allow for external API execution

Prefer low-latency cheap-asset crypto for eventual live testing

🔧 Repository Setup

📁 Folder Structure

OrderflowShooter/
├── Source/
├── Blueprints/
│   ├── TargetSpawner_BP/
│   ├── Wall_BP/
│   └── VolumeBlock_BP/
├── Data/
│   └── SimulatedOrderflow.sqlite
├── Scripts/
│   └── DataInjector.cpp
├── Docs/
│   └── Design_Theory.md
├── Config/
├── README.md

✅ Requirements

Unreal Engine 5.5+

C++ enabled project

SQLite integration plugin (or custom SQLite wrapper)

🛠 Development Setup

# Clone the repository
$ git clone https://github.com/yourusername/OrderflowShooter.git

# Open in Unreal Engine
Launch Unreal 5.5 and open the .uproject file

# Build the C++ project
Compile via Visual Studio (linked to Unreal)

# Run the simulation
Initial mode uses SQLite random data generator

🤖 Phase Planning

🔹 Phase 1 – MVP Prototype (Shooter)



🔹 Phase 2 – Live Data Engine



🔹 Phase 3 – Game Modes



🔹 Phase 4 – Optional Live Trade Execution



👨‍💻 Contributions & Ideas

This is an experimental open-source project. Ideas, Unreal dev contributions, or trading logic suggestions are welcome.

Let’s build the future of visual trading – one shot at a time.

📫 Contact

Lead Designer: Mark Anthony Bartholomew 


