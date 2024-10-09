### Reagan’s Stock Sim

#### Concept:
Reagan’s Stock Sim will start as an online-only stock trading game. Players begin with $500 and aim to grow their portfolio to $1 million.

#### Core Modes:
- **Realism Mode:** Trades based on real-life stock market data.
- **Arcade Mode:** Players influence the stock market, creating a more dynamic and fun experience.

#### Multiplayer First:
- Launch with **multiplayer-only gameplay** for both Realism and Arcade modes.
- **Offline solo mode** will be added later, allowing players to engage in modded gameplay without an internet connection.

#### Structure:
- **Multiplayer (Launch Focus):**
  - **Realism Mode:**
    - Utilizes real stock data from APIs (e.g., Alpha Vantage, Yahoo Finance).
    - Real-time trades during actual market hours (9:30 AM - 4:00 PM ET).
    - Focus on learning to trade in a real-world environment without player influence on stock prices.

  - **Arcade Mode:**
    - Simulated market where player actions can alter prices.
    - Players can adjust volatility and other stock settings.
    - Encourage player interaction, causing intentional market booms or crashes.

#### Future Goal: Offline Solo Mode
- **Offline Play:**
  - Full freedom with mods and custom stock behavior.
  
- **Modding Support:**
  - Players can add stocks, companies, and tweak the simulation freely.

- **Realism & Arcade Modes in Solo:**
  - Downloadable past stock data for simulating trades.

#### Core Systems (Multiplayer):
- **Player Profiles & Authentication:**
  - Firebase Authentication for login/accounts, with data stored in Firebase Firestore for real-time syncing.

- **Real-Time Stock Data (Realism Mode):**
  - Regularly fetch stock data from an API and cache locally.

- **Simulated Stock Market (Arcade Mode):**
  - Stock simulation algorithm to reflect player actions in real-time.

- **Networking & Syncing:**
  - Use Firebase Firestore for data syncing, possibly integrating cURL or Boost.Asio for HTTP requests.

#### How Multiplayer Will Work:
- **Login:** 
  - Players authenticate via Firebase, loading their profile data.
  
- **Trading in Realism Mode:**
  - Real-time API data used for trades based on available balance.

- **Arcade Mode Simulation:**
  - Stock prices change dynamically based on player actions, with sync across all players.

- **Data Syncing:**
  - Player data syncs after major transactions.

#### Plans for Future Features:
- **Offline Solo Mode:** Full offline functionality with modding.
  
- **Multiplayer Company Creation:** Allow players to create investable companies.

- **More Stock Options:** Expand from 15 stocks to 50-100 in future updates.

### Testing Layout:
- **Folder Structure:**

```
[WealthSim] 
    [1.1]
        [source]
            wealthSimMain.cpp
            cmake.txt
        [binaries]
    [1.2]
        [source]
            wealthSimMain.cpp
            cmake.txt
        [binaries]
    [1.3]... Repeat for each version
```

### To-Do List:
1. **Create Base Game Functionality:**
 - Basic window, audio, user input classes.
 - Script functionality with minimal bugs/errors and cleaner UI.

2. **Firebase Integration:**
 - Set up authentication and Firestore for data syncing.

3. **Real-Time API Data:**
 - Integrate stock data APIs and cache for performance.

4. **Stock Market Simulation:**
 - Build the algorithm for Arcade Mode pricing.

5. **Networking & HTTP:**
 - Use cURL/Boost.Asio for data syncing and API calls.

6. **Offline Mode Plans:**
 - Start planning for offline mode and modding support for future updates.
