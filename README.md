# Wood work on the house

A single web page for checking a carpenter's quote. The job replaces the gables, fascia, soffits, gutters and downpipes on our house in Lille Skensved.

The quote is a list of materials and quantities. That's hard to picture, and hard to check. This page puts the house in 3D, from the floor plan and photos, so you can see each part of the job and compare what was quoted with what the house actually needs.

**Open it:** open `index.html` in a browser. There's no build step and nothing to install. If GitHub Pages is turned on for this repo, it also works from there.

## What's on the page

- **A 3D model you can rotate.** Switch between **Today** and **After the work**, or jump to a camera view (entrance, garden, east gable, west gable, above). Click a part on the house, or in the list beside it, to see the material, quantity and price the quote gives for it. **Gable colour** shows the gables in each of the four HardiePlank colours (white, light grey, anthracite grey, black); the dark band, fascia and soffit stay black.
- **Does the quote match the house?** My estimate for each line of the quote next to the quoted amount, each with a verdict: *Matches*, *Generous*, *Not listed* or *Ask*. Sliders for the roof pitch, the overhang depths and the fascia height update both the table and the model.
- **Materials and prices.** Everything in quote 2, with an estimated split of the labour by task.
- **Work plan.** The 12 working days in the order the quote lists them.
- **Questions to ask before signing.** Eight questions, each with a Danish line ready to paste into a reply.
- **Photos.** Nine photos of the house, each with a note on what it shows that matters for the job. Click one to enlarge it.

## The quote in short

| | Quote 1 | Quote 2 (on the page) |
|---|---|---|
| Gutters | Rheinzink zinc, 39 m, 16,602 kr. | Plastmo no. 12 black steel, 36.9 m, 18,705 kr. |
| Taking away old materials | We do it ourselves (3,200 kr. deducted) | Same |
| Scaffolding | Not mentioned | Free, we were told, but it isn't in writing |
| **Total** | **86,571 kr.** | **88,674 kr.** |

### What to raise before signing

- **Free scaffolding** needs to be in writing.
- **The gables will look different.** HardiePlank goes on horizontally, while today's boards are vertical.
- **Gable colour is free to choose.** The quote says black, but all four HardiePlank wood-texture colours cost 105 kr. per board at Davidsen, the same price the quote uses (70 × 105 = 7,350 kr.).
- **Gutter fittings.** The new gutters hang in front of the fascia, where they're easier to clean and keep water off the wood. Today they're hidden behind it, and the soffit has rotted. The 66 konsoljern in the quote are the brackets that hold the gutters, so check they're the kind that screw onto the fascia. Not listed: inner corner pieces (the roof has two inner corners), downpipe clips, and more than 3 joiners.
- **"75 m" of overhang and fascia** looks high. The plan gives about 62–65 m.
- **The dark band above the brickwork** isn't mentioned in the quote.
- **The roof is asbestos cement.** It isn't part of the job, but the new fascia and gutters go on right at its edge, so the sheets mustn't be cut, drilled or broken. We take the old materials away ourselves, so ask whether any of them contain asbestos too: that has to be wrapped and handed in separately.

## How the measurements were made

- **The footprint is measured from the floor plan.** Main wing 16.34 × 7.92 m. The living-room wing is 5.84 m wide and sticks out 3.47 m to the south. The 2.0 × 3.5 m covered terrace east of it has a post at its corner and sits under the same roof.
- **The roof pitch (about 30°) and the overhang depths (about 0.7 m at the eaves, 0.6 m at the gables) are guesses from the photos.** They affect the gable area and the number of HardiePlank boards most. Measure them and set the sliders to get better numbers.

## Files

```
index.html   the whole page: layout, styles, 3D model, quote data
photos/      the nine photos, resized to 1100 px, with location data removed
```

The page loads [three.js](https://threejs.org/) r128 from the jsDelivr CDN, so the 3D model needs an internet connection.

## Changing things

Everything is in `index.html`:

- `P` holds the house dimensions from the floor plan, in metres.
- `S` holds the starting values for the sliders (pitch, eave overhang, gable overhang, fascia rows) and the starting gable colour.
- `COLOURS` holds the four HardiePlank colours. The hex values are on-screen guesses, because Davidsen doesn't publish colour codes. Replace them if you get official ones.
- `COMP` holds each part of the job: name, material, quantity, price and notes.
- `PHOTOS` lists the photos and their captions.

You can link straight to a view and a part, for example `index.html#view=garden&mode=today&sel=gutters`, or to a gable colour with `#colour=lysgraa` (`hvid`, `lysgraa`, `antracit`, `sort`).
