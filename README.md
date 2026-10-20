# Ding-Ding Ride

A 3D bike ride through a little Polish town, for young kids (around age 5), made for phones and tablets. You see the rider from behind. Each ride goes somewhere fun, and each new ride adds one road rule. It follows the Polish rules for a child under 10: ride on the sidewalk, and get off and walk the bike across every zebra.

It's practice for riding alone later. In real life, Polish law lets a child under 10 ride on the sidewalk only with an adult nearby.

Play it at https://tb-x.github.io/ding-ding-ride/.

## How it plays

- **Hold the big green button to ride. Let go to stop.** The bike follows the sidewalk by itself (no steering) and slows down for corners on its own.
- **🔔 Bell.** Someone walking in the middle of the sidewalk goes first. The bike stays behind them; ring the bell and they step aside, wave, and a 💛 pops up. If you just wait, they notice you after a moment anyway.
- **🚶 Get off / 🚲 get back on.** At a zebra you have to get off and walk the bike across. Getting off is a little animation: left foot down, right leg over the back wheel, step beside the bike (and the same backwards to get on). On the other side the button wiggles to say "back on your bike".
- **👀 Look.** The camera turns with the rider's head: left, right, and left again (cars on the near side come from the left in Poland).
- **💡 Light** (on the evening ride): turn it on before you can ride.
- At every stop, round to-do chips appear at the top: 🚶 get off, 👀 look, the little red/green man, 🚗 cars stopped. Each one gets a green tick when it's done, and the next one to do bobs. While something isn't done yet, a red ✋ sits on the pedal button.
- **Mistakes are gentle.** If you go too early (on the bike onto the zebra, without looking, on the red man, while a car is still moving, before the ducks have crossed…), the car honks and stops in time, a big bubble shows what was missed, a voice says what to do, and the rider rolls back a few metres to try again. Nobody ever gets hit. Cars always stop for a rider on the zebra.
- **Cars stop for you** at a zebra without lights once you're standing at the kerb off your bike. The ones too close to stop drive past first, so "wait until the cars stop" is the lesson. A car still far enough back to stop doesn't count; it slows down and waits for you when you step out. The 🚗 chip only ticks once the road has stayed clear for a second.
- **Traffic lights** look like the real Polish ones. The pedestrian light has a red standing man and a green walking man on round lenses, with a countdown of the seconds left under it and a push-button box with a hand on the pole. The tick-tick sound gets fast on green. Arriving at the kerb while the green man blinks is still fine. The car lights hang over each lane on an arm and glow when lit; they run both roads at the junction, so the cross street goes while the green man shows.
- **Stars:** 3 for no mistakes, 2 for one or two, 1 otherwise. You get a sticker of the place you rode to. The next ride unlocks when you finish one. The strip at the top shows the rider moving towards the place, with a dot for each stop (yellow if done right first time).
- 🎨 on the start screen changes the bike, helmet and shirt colours (it starts with a yellow bike and a red helmet). 🏠 goes back to the list of all games.

## Seasons and weather

Every time a ride starts it gets a season and a weather, picked at random (never the same twice in a row). The streets and the stops stay the same, so a ride can be learned, but it looks different each time. The rules don't change with the weather.

- **Spring**: fresh green trees, some in pink blossom, flowers in the grass, petals drifting down. Sometimes showers with a rainbow, rain or fog.
- **Summer**: deep green, sun hats, the rider in shorts. Sometimes a windy day or a shower.
- **Autumn**: orange and red trees, leaves on the ground and blowing about, coats. Often rain, fog or wind.
- **Winter**: snow on the ground, the roofs and the cars, bare trees, snowy fir trees, snowmen in the parks and gardens, everyone in hats and scarves (the rider gets a scarf and gloves). Snowing, crisp and sunny, or foggy.
- **Rain**: wet dark paving, puddles with raindrops rippling in them, umbrellas. Riding through a puddle on the path splashes. Cars drive with their lights on in rain, fog and snow, and the windows glow.
- The duck pond is only in spring and summer (ducklings), the ice cream shop and the evening beach ride only in summer, and the evening ride is always dry.

## The town

The town is built in code from four kinds of block, so each ride passes different streets: old town houses (2–7 floors, pitched roofs with dormers, balconies with flowers, shops with striped awnings, Polish name boards like PIEKARNIA or APTEKA and round picture signs), family houses with gardens, fences or hedges, letterboxes and the odd garden gnome, blocks of flats with coloured balconies, a parking strip and a carpet-beater in the yard, and parks with a fountain, a playground, a flower bed, a football pitch or a church. Along the sidewalks there are benches, bins, post boxes, fire hydrants, bike racks, planters and advertising columns, and the trees are round, birch, poplar or fir. Cars come in eight shapes (hatchback, saloon, estate, SUV, coupé, a little Maluch, a van, a taxi) with Polish number plates, wheels that turn, and see-through windows with seats and a driver inside.

The first ride is all park: gravel paths with stone edging and old-style lanterns, benches, flower beds, meadows and avenues of trees between the paths, joggers and dog walkers, a kid flying a kite, butterflies on sunny days, and signposts with pictures. It ends at a duck pond with an island and a duck house, lily pads, reeds, a pier with a rowing boat, a willow, swans and ducklings.

## The eight rides

| # | To | New rule |
| --- | --- | --- |
| 1 | 🦆 the duck pond (in the park, no cars) | Hold to go, let go to stop: stop at the red flags, wait for the ducks to cross |
| 2 | 🥐 the bakery | People walking go first: ring the bell (one walks a dog) |
| 3 | 🎠 the playground | Zebra crossing: stop at the kerb, get off, look left-right-left, wait for the cars to stop, walk across |
| 4 | 🏫 school | Traffic lights: wait for the green man |
| 5 | 🍦 the ice cream shop | Cars coming out of a gate across the sidewalk: stop and wait |
| 6 | 📚 the library | The bus stop: let the people getting off the bus cross first |
| 7 | 🚒 the fire station | Sirens: a fire engine (at lights) and an ambulance (at a zebra). Wait even when it's green |
| 8 | 🏖️ the beach | Everything together, in the evening, with the bike light on |

## Run it

It's one page plus the sound clips in `assets/`. Serve the folder (for example `python -m http.server 5216`) and open it in a browser; it needs an internet connection the first time for the 3D library and the title font. No build step. Opening it straight from disk also works.

Built with [three.js](https://threejs.org/). Every model (the town, the rider, cars, people, ducks) is built in code; there are no picture files apart from the icons. Parts of each model that don't move are merged into one mesh with its colours stored per vertex, and every kind and colour of car is built once and shared, so the detailed town still draws in about 200–300 draw calls.

## Play offline (add to Home Screen)

On iPhone or iPad, open the game in Safari, tap **Share → Add to Home Screen**, then open it once from the new icon while online. After that it starts full screen and works without internet. Changes arrive on their own: the next online launch downloads them and the one after shows them.

(How: `manifest.webmanifest` gives the icon and full-screen mode; `sw.js`, a service worker, keeps a copy of every file the game uses. The icons `icon-180.png` and `icon-512.png` are rendered from `icon.svg` in headless Chrome.)

## Tuning knobs

At the top of the script in `index.html`:

- `RIDE_SPEED`, `WALK_SPEED`: how fast the bike goes, and walking with it (metres a second).
- `PEDAL_ACCEL`, `BRAKE`: how quickly it speeds up while the button is held, and slows down when it's let go.
- `TURN_GRIP`: how much it slows for corners by itself.
- `ZONE`: how far before a stop the to-do chips appear.
- `REWIND_BACK`: how far back the rider rolls after a mistake.
- `CAR_SPEED`, `CAR_ACCEL`, `CAR_DECEL`: the cars.
- `SAFE_DIST`: cars further than this from the zebra never count. Closer ones count while they're moving and too close to stop for you (less than their braking distance plus 6 m, and at least 10 m).
- `SIREN_SPEED`: the fire engine and the ambulance.
- `LIGHT_TIMES`: how long each traffic-light phase lasts. When the rider is waiting at the kerb (off the bike, having looked), the cars' green is cut short so the wait isn't long.
- `LOOK_TIME`: how long one look left-right-left takes.
- `CAM_DIST`, `CAM_HEIGHT`: where the camera sits behind the rider.
- `RIDES`: one row per ride. The route is written as moves from street corner to street corner (E/W/N/S), with what happens on each: `zebra` or `lights` for a crossing (plus `siren`), and `flag`, `ducks`, `people`, `dog`, `driveway`, `bus` along a block. `traffic` is the average seconds between cars in each lane.
- `COLOURS`: the colour sets 🎨 cycles through.
- `SEASONS`, `WEATHER`: the seasons, and how likely each weather is in each one. A ride's `seasons` in `RIDES` limits which seasons it can have.
- `WIND`, `RAIN_SPEED`, `SNOW_SPEED`: how hard the wind blows on windy days, and how fast rain and snow fall.
- `STYLE_W` (in the cars section): how common each kind of car is.

To try a particular season or weather, add it to the address, for example `index.html?season=winter&weather=snow`. Weathers: `sun`, `showers`, `rain`, `fog`, `wind`, `snow`, `frosty`.

## Sound

Voices and sounds: [elevenlabs.io](https://elevenlabs.io). The credit also shows on the title screen and the win card. Every spoken line and most sounds are recorded clips in `assets/`. Each one falls back to a sound made in the browser (or the device's own voice) if a clip can't load, for example when the page is opened straight from disk. The crossing's tick-tick, the freewheel clicks, the splash through a puddle, the little "ding" for a stop done right and the duckling peeps are always made in the browser. There's no background music, so the sirens and the crossing beeper are easy to hear.

Sound knobs, in the sound section of the script:

- `CLIP_VOL` and `VOICE_VOL`: how loud the sound effects and the spoken lines are (0 to 1).
- `CLIP_TRIM`: per-clip volume trims that even out the clips, which ElevenLabs made at different levels (measured in the browser). Lower a number if a sound is too loud.
- `ASSET_V`: bump it after replacing any file in `assets/`, so phones don't keep the old one.
- `USE_CLIPS`: set it to `false` to hear only the browser-made sounds.

## Audio credits

Every clip was made on **2026-10-18** with the ElevenLabs **Starter** (paid) plan, so it may be used commercially. The clips are here only as the game's own sounds: they are not licensed to anyone else, and none of the audio is covered by any licence that may later be put on this game's code. All of it was made by AI (ElevenLabs), in a stock voice; no real person's voice was used. Terms checked on 2026-10-18 (ElevenLabs Terms of Use, last updated 2026-10-09; the voice model and the sound effects model, including its loop option, are not marked beta).

- **Spoken lines** (`assets/say-*.mp3`, 44 clips): voice "Jessica - Playful, Bright, Warm" (a stock ElevenLabs voice), model Eleven Multilingual v2, stability 0.5, style 0.2, speed 0.95. The exact text of each line is in `LINES` in the script: 8 "Let's ride to …" intros, 8 "Hooray! You made it to …!" endings, the prompts at the stops (flag, ducks, bell, kerb, "Look left, right, and left again!", "Left!", "Right!", red man, green man, cars, driveway, bus, siren, light, "Back on your bike!", "Off you go!") and 10 "Whoops! …" lines.
- **Sound effects** (`assets/sfx-*.mp3`, 13 clips): ElevenLabs Sound Effects. The bicycle bell, a gentle car horn, a duck quack, a dog bark, bus doors, a cartoon "whoops" slide whistle, a rewind whirr, children cheering, a short win fanfare, pigeons flapping off, a car engine starting, and looping sirens for the fire engine (hi-lo) and the ambulance.
