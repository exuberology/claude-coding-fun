# Rando Commando

A Mario Kart randomizer that works on a computer or a phone. It's one static page (`index.html`) with no build step.

## How it works

- Pick 2–8 players (2 is the default) and press **Rando Commando It**.
- Each player gets a random **Racer, Kart, Tires and Glider**, listed in that order.
- No two players in a round share a pick, unless a list has fewer entries than there are players.
- Picks are not repeated across rounds until every option in a list has been used. After that, the list is reshuffled and the cycle starts again. Each list runs on its own cycle.
- Each round also draws 2–10 random **Power-Ups** with no repeats inside the round. Power-Ups can repeat between rounds.
- Every round, and how far each list is through its cycle, is saved in the browser's local storage. Both survive a refresh. **Clear memory** resets them.

## Your lists

The app loads `mario-kart.csv` on startup. You can replace that file with your own lists, or use **Upload CSV** inside the app. An uploaded file is saved in that browser.

The CSV has one column per list. Columns can have different lengths:

```csv
Racers,Karts,Tires,Gliders,Power-Ups
Mario,Standard Kart,Standard,Super Glider,Banana
Luigi,Pipe Frame,Monster,Cloud Glider,Green Shell
```

It also accepts a two-column `Category,Name` layout, with one item per row.

## Hosting

Turn on GitHub Pages (Settings → Pages → deploy from a branch) to get a URL that works on every device. Saved rounds stay in each device's own browser.

To run it locally: `python3 -m http.server`, then open http://localhost:8000.
