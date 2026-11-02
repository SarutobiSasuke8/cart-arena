# Build plan

Solo cart arena. Original IP. One match you can finish in three minutes, against bots, in the browser. Best score stays on this device.

Online play is a later project. The handling, the weapons, and the bots have to feel right before a server is worth building.

## Product rules

- One human, seven bots, one arena, 180 seconds.
- Score is knockouts. Falling off with nobody to blame does not give anyone a point.
- If you hit someone and they go out within 3 seconds, you get the knockout.
- You hold one weapon. A new tin replaces it.
- Respawn on a marked pad with a short spawn protection.
- No accounts, no shop, no battle pass, no seasons.
- A high score on this device is the only meta.

## What we take from the genre

Mechanical only:

- Closed arena, not laps.
- Accelerate, brake, steer, slide.
- Pickups.
- Knockout, respawn, score.
- A short clock and a results board.
- Bots so the room is never empty.
- A chase camera behind the cart.

## What we do not take

- Characters, names, maps, UI layout, sounds, or weapon roster from Smash Karts or any other kart game.
- Question-mark item boxes, if the locked IP has its own pickup (tins, parcels, lanterns, slag pots).
- Real weapons, real companies, real cities.
- Multiplayer of any kind in v1. No rooms, no links, no accounts.

## Phases

### 0. Lock the IP

Owner: you.

Delivered in this repo: five themes, a recommendation (Gutter Prix), match rules, this plan.

Done when you pick a base theme. After that, the name, palette, driver silhouette, three weapons, and first arena stop moving.

### 1. Drive slice

The cart moves on the arena and stays on it.

- Chase camera. A turns left, D turns right, while moving forward.
- Accelerate, brake, and a slide that is strong enough to matter.
- Walls and a fall-off respawn.
- A clock on screen, even if nothing else scores yet.
- Keyboard on desktop. A thumb stick and a brake on a phone.

Done when you can drive the whole arena for three minutes without falling through the floor or getting the steer backwards.

### 2. Combat

- Three weapons from the locked IP. One light, one heavy, one area denial.
- Pickups respawn a few seconds after they are taken.
- A hit shoves or spins. A strong hit, or a hit near the edge, knocks you out.
- Respawn protection so you are not farmed on the pad.
- Score and a results board.

Done when a human can knock out a parked dummy cart and see the point.

### 3. Bots

Seven carts. Three behaviors, assigned unevenly:

- **Hunt** — drive at the player or the nearest cart and fire when roughly lined up.
- **Tin** — prefer pickups, then fire.
- **Wander** — follow the arena's racing line and fire late.

They miss on purpose. They do not perfect-track. They respawn on the same rules as you.

Done when a full three-minute match finishes, the results board ranks everyone, and the winner is not always the same bot.

### 4. Feel

- Skid marks or their IP equivalent.
- A short hit pause and a small camera shake on a knockout. Not on every graze.
- Pickup and knockout barks in the IP voice. A few lines, not a narrator.
- Best score saved on this device.
- Touch controls that do not cover the cart.

Done when a match is readable with the sound off and playable on a phone.

### 5. Only after 1–4

One extra mode, still solo: hold an objective (the tin hat, the parcel, the lantern) for a running score. Or a second arena in the same IP.

Not in this phase: online, accounts, cosmetics, a second IP.

## Suggested build order inside a phase

1. Simulation (positions, hits, score).
2. Camera and controls.
3. Arena dressing.
4. HUD.
5. Juice.

Juice before the hit exists is how the game starts lying.

## Tech

- The browser build is a React app with three.js for the arena.
- Physics stays simple and owned by us: a cart on a plane, rays or boxes for walls, no ragdolls.
- Fixed simulation step so a hiccup does not tunnel the cart through a wall.
- Best score in local storage, with a version number so we can change the shape later.
- No database and no sign-in.

## v1 is done when

- You can finish a three-minute match against bots.
- The results board is correct.
- Steer matches the chase camera on both a laptop and a phone.
- The theme is obvious without a paragraph of text.
- Nothing on screen is borrowed from an existing kart game.

## Explicitly later

Authoritative online play, private rooms, and regions. That work starts only after a solo match is fun with the network cable pulled out.
